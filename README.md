# Dynamic-Modular-Mixture-of-Heterogeneus-Experts




Official Implementation for "One Model, Many Architectures: A Dynamic Modular Mixture of Heterogeneous Experts"
Authors: Zaryab Rahman, Dr. Fakhruddin Ali
Affiliation: University of Malakand, Chakdara, Pakistan
Journal Submission: Scientific Reports (Nature Portfolio)
Abstract
(TODO: Copy and paste the complete abstract of your paper here. This is crucial as it provides an immediate summary of your work's contribution.)
Code Overview
This repository contains the official PyTorch implementation and experimental notebooks for our paper. The code is organized to allow for full reproducibility of our key findings.
The primary contributions demonstrated in this code are:
The implementation of our novel Dynamic Modular Mixture of Heterogeneous Experts (DMMoE) architecture.
Benchmarking experiments on CIFAR-10 comparing DMMoE to homogeneous MoE and dense baselines.
In-depth analysis of the model's emergent capabilities, including modality-aware routing and transfer learning.
Repository Structure
The code is organized into two main Jupyter Notebooks, each corresponding to a distinct set of experiments:
DMMoE_CIFAR10_Benchmark.ipynb: Contains the code to reproduce the main benchmarking results on the CIFAR-10 dataset, comparing our model against homogeneous and dense baselines. This notebook also includes our implementation of the essential Load Balancing Loss.
DMMoE_Analysis_and_Applications.ipynb: Contains the code for the advanced analytical experiments presented in the paper, including:
The VQA Multimodal Routing Analysis (Figure 4).
The Few-Shot Learning Baselines.
The core Transfer Learning and Expert Utilization Analysis (Figure 5).
Setup and Installation
To run these experiments, you will need a Python environment with the necessary dependencies. A CUDA-enabled GPU is highly recommended for reasonable training times.
1. Clone the Repository
code
Bash
git clone https://github.com/YourUsername/Your-Repository-Name.git
cd Your-Repository-Name
(Note: Replace YourUsername/Your-Repository-Name with your actual GitHub URL)
2. Create a Python Environment
We recommend using Conda or a virtual environment to manage dependencies.
code
Bash
# Using Conda
conda create -n dmmoe python=3.9
conda activate dmmoe

# Or using venv
python -m venv dmmoe_env
source dmmoe_env/bin/activate
3. Install Dependencies
All required libraries are listed in the requirements.txt file.
code
Bash
pip install -r requirements.txt
(Note: Ensure you have created the requirements.txt file by running pip freeze > requirements.txt from your activated project environment.)
Running the Experiments
The experiments are self-contained within the Jupyter Notebooks.
Start a Jupyter Server: From the root of the cloned repository, run:
code
Bash
jupyter notebook
or
code
Bash
jupyter lab
Navigate and Run:
To reproduce the main CIFAR-10 benchmark, open and run the cells in DMMoE_CIFAR10_Benchmark.ipynb. The notebook is set up to run the main DMMoE experiment by default. The baseline experiments are included but commented out.
To reproduce the analytical and application-focused experiments, open and run the cells in DMMoE_Analysis_and_Applications.ipynb.
The notebooks have been structured with Markdown cells to explain each step of the process. All datasets (CIFAR-10, SVHN, AG_NEWS, IMDb) will be downloaded automatically by the helper functions in the code.
Data Availability
The datasets used in this study are all publicly available and will be downloaded automatically by the scripts within the notebooks.
CIFAR-10: https://www.cs.toronto.edu/~kriz/cifar.html
SVHN: http://ufldl.stanford.edu/housenumbers/
AG_NEWS & IMDb: Sourced from standard repositories as detailed in the notebooks.
The source code is fully available in this GitHub repository.
Citation
If you find our work useful in your research, please consider citing our paper.
(This section will be updated with the full citation once the paper is published.)
code
Code
@article{Rahman2025DMMoE,
  author    = {Rahman, Zaryab and Ali, Fakhruddin},
  title     = {One Model, Many Architectures: A Dynamic Modular Mixture of Heterogeneous Experts},
  journal   = {Scientific Reports},
  year      = {2025},
}
