# Design and Analysis of H∞ and μ-Synthesis-Based Attitude Controllers for an Underactuated Quadrotor

A complete report is provided in the repository. Below are instructions to run MATLAB code blocks in Jupyter Notebook for reproducibility and interactive analysis.

---

## 1. Check Supported Python Versions for MATLAB Engine**
Before installation, verify which Python versions are compatible with your MATLAB installation:

1. Navigate to the MATLAB root folder:
   ```
   cd /usr/local/MATLAB/R20XXx/extern/engines/python
   ```
3. Open setup.py and check the _supported_versions variable. Example (MATLAB 2019):
    ```
    _supported_versions = ['2.7', '3.6', '3.7']  # Python versions supported
    ```
## 2. Install a Supported Python Version
Use pyenv or conda to install the correct Python version or just download it from its official website. Example for Python 3.7:
  ```
  conda create -n matlab_env python=3.7
  conda activate matlab_env
  ```
## 3. Set Up a Virtual Environment
Isolate dependencies to avoid conflicts:
  ```
  python -m venv matlab_venv
  source matlab_venv/bin/activate  # Linux/Mac
  matlab_venv\Scripts\activate     # Windows
  ```
## 4. Install Requirements
### 4.1 MATLAB Engine API for Python
Install the MATLAB Engine API from the MATLAB folder:
  ```
  cd /usr/local/MATLAB/R20XXx/extern/engines/python
  python setup.py install
  ```
### 4.2 Jupyter and Dependencies
Install Jupyter and the MATLAB kernel:
  ```
  pip install jupyter, ipykernel, matlab_kernel
  pip install -r requirements.txt # If yoy're cloning this repository
  ```
## 5. Run Jupyter Notebook with MATLAB Kernel
1. Launch Jupyter Notebook:
   ```
   jupyter notebook
   ```
2. Create a new notebook and select the MATLAB kernel.

3. Run MATLAB code interactively:
   ```
   % Example: H∞ Controller Synthesis
   G = tf(1, [1 2 1]);
   K = hinfsyn(G, 1, 1);
   bode(K);
   ```
   
4. Run notebook from this repository
   ```
   cd /"Robust Control"/
   jupyter notebook notebook.ipynb
   ```
