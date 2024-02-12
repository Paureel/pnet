# Pnet
Implementation of P-Net as a flexible deep learning tool to generate insights from genetic features.

Current pytorch implementation in revision.

## Model
Pnet uses the Reactome hierarchical graph as underlying structure to reduce the number of connections in a fully connected feed forward neural network. The sparse layers connect only known pathways. This limits the number of parameters to be learnt in a meaningful way and facilitate learning via gradient descent and leads to more generalizable models. 

## Installation
Clone the github repository and navigate into it. Create the conda environment with ```conda env create -f pnet.yml```, activate it with ```conda activate pnet``` and run ```pip install -e . ``` to install the package locally.

To check successful installation run ```python test/test_data_loader.py``` which will verify basic import and file structure. For further functional testing see the [testing notebook](https://github.com/vanallenlab/pnet/blob/main/notebooks/testing.ipynb)

## Usage
Detailed sepcific usage examples are provided in the [notebooks](https://github.com/vanallenlab/pnet/tree/main/notebooks). Generally the network structure expects gene level data for each sample (e.g. read counts, CNA indication etc.). different data modalities can be concatenated as a dictonary and passed to the pnet_loader object. A good starting place to familiarize yourself with the usage of pnet is this [example notebook](https://github.com/vanallenlab/pnet/blob/main/notebooks/SKCM_purity.ipynb)
