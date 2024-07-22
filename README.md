
# FPGA-Integration-with-Quantum-Computing.

This project explores the integration of Field-Programmable Gate Arrays (FPGAs) with Quantum Computing. The aim is to leverage the reconfigurable hardware capabilities of FPGAs to enhance the performance and efficiency of quantum algorithms. The project includes the development of FPGA modules, interfacing protocols, and demonstration of quantum algorithm acceleration using FPGA hardware.


## Appendix

### A. Glossary
- **FPGA (Field-Programmable Gate Array)**: A type of reconfigurable hardware that can be programmed to perform a wide range of tasks, allowing for high performance and flexibility.
- **Quantum Computing**: A field of computing focused on the development of computers based on the principles of quantum mechanics, which can potentially solve certain problems much faster than classical computers.
- **Quantum Algorithm**: An algorithm that runs on a quantum computer and utilizes quantum mechanical phenomena such as superposition and entanglement.
- **Interfacing Protocols**: The methods and standards used to allow communication and interaction between different hardware and software components.

### B. References
1. [Nielsen, M. A., & Chuang, I. L. (2010). Quantum Computation and Quantum Information. Cambridge University Press.](https://www.cambridge.org/us/academic/subjects/physics/quantum-physics-quantum-information-and-quantum-computation/quantum-computation-and-quantum-information-10th-anniversary-edition)
2. [Koch, D. (2016). FPGA-Based Implementation of Signal Processing Systems. Springer.](https://www.springer.com/gp/book/9783319274752)

### C. Additional Resources
- [Qiskit Documentation](https://qiskit.org/documentation/)
- [Intel FPGA Documentation](https://www.intel.com/content/www/us/en/products/docs/programmable/fpga.html)
- [Xilinx FPGA Resources](https://www.xilinx.com/support/documentation-navigation/design-hubs.html)

### D. Acknowledgments
We would like to thank all contributors and collaborators who provided valuable insights and support for this project. Special thanks to the Quantum Computing research community for their foundational work and ongoing innovations.





## Installation 

**1.**  Download [miniconda](https://docs.anaconda.com/miniconda/) and [visual studio](https://code.visualstudio.com/download).

**2.** Once **miniconda** and **visual Studio** have been installed, choose the Search option and select >>>`Anaconda Prompt (miniconda3)`.

## **Creating an environment with commands**

1. To create an environment:

```python
conda create --name <my-env>
```
Replace `<my-env>` with the name of your environment.

2. When conda asks you to proceed, type `y`:

```python
proceed ([y]/n)?
```
This creates the myenv environment in /envs/. No packages will be installed in this environment.

3. To activate conda environment:

```python 
conda activate <my-env>
```
4. Install `pip` :

```python 
conda install pip
```
5. Install `qiskit` :

```python
pip install qiskit
```
6. Install `matplotlib` :

```python
pip install matplotlib
```
7. Install `qiskit_ibm_runtime` :

```python
pip install qiskit_ibm_runtime
```
8. Install `pylatexenc` :

```python
pip install pylatexenc
```
**3.** Launch Visual Studio Notebook, choose Jupyter notebook for the new file type.

#### Select Kernal<<< Python Environment <<< `<my-env>`

**4.** Code in that notebook - QiskitRuntimeServices

```python
import qiskit
```
```python
qiskit.__version__
```
 Go to [quantum.ibm.com](https://quantum.ibm.com/) and register to gain access of IBM Quantum Platform's  API Token.

 ![ibm](https://github.com/user-attachments/assets/6e7a5470-2ca7-4b23-ad44-8899246b7234)


```python
from qiskit_ibm_runtime import QiskitRuntimeService

# Save the account
QiskitRuntimeService.save_account(channel='ibm_quantum', token='<API Token>')

# Load the account
service = QiskitRuntimeService()
```
To check account_info :

```python
from qiskit_ibm_runtime import QiskitRuntimeService

# Load the IBM Quantum Experience account
service = QiskitRuntimeService()

# Check and print the details of the currently loaded account
account_info = service.active_account()
print("Active account details:", account_info)
```
If the error looks like this :
**AccountAlreadyExistsError: 'Named account (default-ibm-quantum) already exists. Set overwrite=True to overwrite.'**

1. 
```python
from qiskit_ibm_runtime import QiskitRuntimeService

# Save the account with overwrite=True to update the existing credentials
QiskitRuntimeService.save_account(channel='ibm_quantum', token='<NEW-API Token>', overwrite=True)

# Load the IBM Quantum Experience account
service = QiskitRuntimeService()

# Now you can use the `service` object to interact with the IBM Quantum services
print(service.backends())  # List available backends
```
2. 
```python
from qiskit_ibm_runtime import QiskitRuntimeService

# Load the IBM Quantum Experience account
service = QiskitRuntimeService()

# Check and print the details of the currently loaded account
account_info = service.active_account()
print("Active account details:", account_info)
```





## Contact Us :
### Contact Information
For any questions or further information, please contact:
- **Project Lead:** [Your Name] - [your.email@example.com]
- **GitHub Repository:** [GitHub Link](https://github.com/yourusername/FPGA-Integration-with-Quantum-Computing)
