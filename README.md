Create a rdkit environment that directly contains rdkit:

**conda create -c conda-forge -n ddiffusion rdkit=2023.03.2 python=3.9**

**conda activate ddiffusion**

****************************************************************************

Check that this line does not return an error:

**python3 -c 'from rdkit import Chem'**

****************************************************************************

Install graph-tool (https://graph-tool.skewed.de/):

**conda install -c conda-forge graph-tool=2.45**

****************************************************************************

Check that this line does not return an error:

**python3 -c 'import graph_tool as gt'**

****************************************************************************

Install the nvcc drivers for your cuda version. For example:

**conda install -c "nvidia/label/cuda-11.8.0" cuda**

****************************************************************************

Install a corresponding version of pytorch, for example:

**pip3 install torch==2.0.1 --index-url https://download.pytorch.org/whl/cu118**

****************************************************************************

Install other packages using the requirement file:

**pip install -r requirements.txt**

****************************************************************************

Run:

**pip install -e .**

****************************************************************************

Navigate to the ./src/analysis/orca directory and compile orca.cpp:

**g++ -O2 -std=c++11 -o orca orca.cpp**

****************************************************************************

To run the code on qm9 dataset:

**python3 main.py dataset=qm9**

****************************************************************************

For visualising the Results:

It will ask you to create the account on w&b(wandb.ai), else if you have an existing account you can use the same.
Create an API key on the w&b and paste the key in the terminal
