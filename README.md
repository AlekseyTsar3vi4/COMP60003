# COMP60003 - Advanced Topics in Cyber Security

### Assignment 1 - Creating and Analysing Synthetic Authentication Data Using Distribution Techniques

## Overview

This project involves creating a **synthetic dataset** to simulate authentication requests and analysing it against the **LANL authentication dataset**. The synthetic dataset adheres to the following requirements:

- **Features**:
  - **Username**: Five characters, starting with a letter followed by a year (e.g., `A1985`).
  - **Computer ID**: Two uppercase letters and two digits (e.g., `LG01`).
  - **Connection Time**: Spanning `00:00:00` to `23:59:59`.
  - **IP Address**: Generated using weighted private subnets.
  - **Labels**: Binary (`A` for Accept, `D` for Deny) assigned using a normal distribution.
- **Specifications**:
  - **200 unique users** accessing **50 computers**.
  - **1,500 authentication requests** over 24 hours.

Statistical validation and comparative analysis are performed to ensure fidelity with real-world data patterns.

---

## Repository Structure

```plaintext
COMP60003/
├── Main_Code_for_Assignment.ipynb    # Synthetic dataset generation
├── LANL_dataset.ipynb                # LANL dataset analysis
├── lanl-auth-dataset-1-00.csv        # LANL dataset sample
├── README.md
```

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Python 3.x
- Required libraries: `numpy`, `pandas`, `matplotlib`, `seaborn`, `scipy`

To install dependencies, run the following command:

```bash
pip install numpy pandas matplotlib seaborn scip
```
## Usage

### Synthetic Dataset:

- Open `Main_Code_for_Assignment.ipynb` in Jupyter Notebook or Google Colab.
- Run all cells to generate the dataset and visualisations.

### LANL Dataset Analysis:
- Place `lanl-auth-dataset-1-00.csv` in the working directory.
- Open `LANL_dataset.ipynb`
- Run all cells to process and visualise the LANL dataset.
### Output:
- The synthetic dataset is saved as:
`synthetic_authentication_data_<timestamp>.csv`

## Features
### Synthetic Dataset:
- **Usernames**: Uniform distribution ensures equal likelihood for all combinations.
- **Computer IDs**: Binomial-like distribution replicates shared resource usage.
- **Connection Times**: Exponential distribution biases activity towards working hours.
- **IP Addresses**: Generated using weighted Poisson distribution.
- **Labels**: Normal distribution with time-sensitive thresholds.
### Validation:
- **Chi-Square Test**: Ensures statistical randomness of labels.
- **Visualisations**: Bar charts and histograms compare synthetic and real datasets.
## Code Access
- [Main_Code_for_Assignment.ipynb](https://colab.research.google.com/drive/1SaIKnq21O8Q_WypeTKN4iqibbC6OgYPT): Synthetic dataset generation.
- [LANL_dataset.ipynb](https://colab.research.google.com/drive/1-x8Jqxj_3uvuJ_JNbU0Z5eVNQqHy8Zy1): LANL dataset analysis.
## References
- LANL Dataset: Unified Host and Network Dataset 2017
- Boutros, F. et al. (2022). SFace: Privacy-friendly and accurate face recognition using synthetic data. arXiv-CS.CV.
- Hwang, H. et al. (2020). ElderSim: A synthetic data generation platform for human action recognition in eldercare applications. arXiv-CS.CV.

For a complete reference list, see the report.

---
## Contact
For queries or feedback, contact Alexei Gaicovschi at g028335l@student.staffs.ac.uk.
