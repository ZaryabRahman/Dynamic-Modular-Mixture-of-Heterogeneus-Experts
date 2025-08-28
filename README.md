# Dynamic-Modular-Mixture-of-Heterogeneus-Experts


# Official Implementation for "One Model, Many Architectures: A Dynamic Modular Mixture of Heterogeneous Experts"

**Authors:** Zaryab Rahman1, Fakhrud Din1, Shah Khalid1, and Ayman Qahmash2 
**Affiliation:** University of Malakand, Chakdara, Pakistan  
**Journal Submission:** *Under Review at Scientific Reports (Nature Portfolio)*

---

## Abstract
*The Mixture-of-Experts (MoE) paradigm has emerged as a key strategy for scaling large models efficiently by activating only a
sparse subset of their parameters. However, existing MoE models typically rely on a pool of homogeneous experts, which
can limit their ability to capture the diverse structural priors needed for complex tasks. In this work, we introduce the Dynamic
Modular Mixture of Heterogeneous Experts (DMMoE), a novel architecture that combines sparsity with true architectural
specialization. Our model features a pool of structurally diverse experts (e.g., convolutional, attention-based, and recurrent) and
learns a dynamic routing mechanism to select a sparse combination of them for each input token. We conduct a comprehensive
empirical validation across multiple domains. First, we show that DMMoE achieves performance competitive with dense
baselines on single-modality vision and language tasks with up to 24% fewer computational FLOPs. Second, on a challenging
Visual Question Answering (VQA) task, we demonstrate that the model learns an intelligent, modality-aware routing policy,
assigning image and text tokens to different architectural specialists within a single forward pass. Finally, our investigation into
the model’s generalization capabilities reveals a nuanced picture. On in-domain tasks, DMMoE demonstrates remarkable data
efficiency, achieving 89.97% accuracy on 20-shot AG News with pre-trained experts. However, in a true cross-domain setting,
we observe a clear case of negative transfer, highlighting the challenges of knowledge reuse across disparate tasks. Crucially,
we show that even during this negative transfer, DMMoE’s dynamic routing mechanism successfully adapts by identifying and
suppressing irrelevant experts, demonstrating intelligent architectural control.*

---

## Code Overview
This repository provides the official **PyTorch** implementation to reproduce the findings presented in our **submitted manuscript**.  
The implementation is organized into **two primary Jupyter Notebooks**, each focusing on a specific experimental domain.

---

## Repository Structure

- **`DMMoE_CIFAR10_Benchmark.ipynb`**  
  Implements and benchmarks our proposed **DMMoE** model on the **CIFAR-10** dataset.  
  Includes comparative experiments with:
  - Homogeneous MoE (MLP experts only)
  - Dense Vision Transformer  
  Also contains the **Load Balancing Loss** implementation, essential for stable MoE training.

- **`DMMoE_Analysis_and_Applications.ipynb`**  
  Provides advanced analytical experiments showcasing the unique capabilities of our model:  
  - **VQA Multimodal Routing Analysis** (Figure 4)  
  - **Few-Shot Learning Baselines**  
  - **Transfer Learning & Expert Utilization Analysis** (Figure 5)

---

## Reproducibility

### Running Experiments
1. Open the desired notebook.
2. Execute cells sequentially.  
3. Datasets (CIFAR-10, SVHN, AG_NEWS, IMDb) are automatically downloaded via helper functions.  

Each notebook contains detailed **Markdown annotations** explaining the purpose and relevance of each code block.

### A Note On Reproducibility
A Note on Reproducibility: Due to the stochastic nature of router initialization in few-shot training, individual runs may produce slightly different but comparable results. For instance, the notebook's AG News fine-tuning run may yield an accuracy around 90.14%, while the canonical result reported in the manuscript from our official experiments is 89.97%.

---

## Data Availability
All datasets used are **publicly available** and automatically handled by our scripts.  
The **full source code** for all experiments is contained within this repository.

---

## Citation
Will be added after publishing. 





