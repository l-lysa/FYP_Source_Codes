A. Execution Guide - Tools (version), Libraries and Links

1. Programming Language:
- Python 3.10+
Link: https://www.python.org/downloads/

2. Required Tools:
- PyTorch (torch, torchvision)
- NumPy
- scikit-learn
- matplotlib
- tqdm
- timm (PyTorch Image Models)

3. Installation:
You can install all required libraries using the following command: pip install torch torchvision numpy scikit-learn matplotlib tqdm timm

4. For GPU acceleration, follow the official PyTorch installation page based on your CUDA version: https://pytorch.org/get-started/locally/
-------------------------------------------------------------------------------------------------------------------------------------------
B. Public dataset

The CASIA-B dataset can be downloaded from the website: http://www.cbsr.ia.ac.cn/english/Gait%20Databases.asp

1. Scroll down until you see the blue box to download the Dataset B (628M).
2. Click on the Dataset B (628M) and it will start downloading.
3. If the download fail as it shows insecure download blocked, just press "Keep" and it will download successfully.
4. After downloading, locate the zip files and extract the dataset.
-------------------------------------------------------------------------------------------------------------------------------------------
C. Data Preprocessing

To generate the Gait Energy Image (GEI) using the raw silhouette downloaded from the website above:
We manually run each ipynb files based on the conditions in the folder (GEI Dataset - Generate GEI from Raw Silhouette)
*The conditions is stated in the Project structure below
-------------------------------------------------------------------------------------------------------------------------------------------
D. Experiment Execution

Modify the dataset path to match your path accordingly to ensure that it can be executed without error.
-------------------------------------------------------------------------------------------------------------------------------------------

Project Structure:
This repository contains experiments and datasets related to GEI (Gait Energy Image) generation and pre-trained Vision Transformer (ViT) model. Below is the detailed structure of the folders and files.

Folder Structure - 3 Experiments and 1 GEI dataset:
1. Experiment 1
- ViT-NM+NM.ipynb: Jupyter notebook for the NM training and testing.

2. Experiment 2
- ViT-NM,CL,BG+BG.ipynb: Jupyter notebook for ViT with NM, CL, BG training and BG testing.
- ViT-NM,CL,BG+CL.ipynb: Jupyter notebook for ViT with NM, CL, BG training and CL testing.
- ViT-NM,CL,BG+NM.ipynb: Jupyter notebook for ViT with NM, CL, BG training and NM testing.

3. Experiment 3
- ViT-NM,CL,BG+NM,CL,BG.ipynb: Jupyter notebook for ViT with NM, CL, BG training and testing.

4. GEI Dataset - Generate GEI from Raw Silhouette:
This folder contains scripts for generating GEI from raw silhouette data, organized into different subsets.

There are a total of 9 GEI Generation Scripts:
- GEI_NM,CL,BG.ipynb: Generates GEI for the following subsets:
  nm-01, nm-02, nm-03, nm-04
  cl-01
  bg-01

- GEI_NM,CL,BG_all.ipynb: Generates GEI for an extended dataset:
  nm-01, nm-02, nm-03, nm-04, nm-05, nm-06
  cl-01, cl-02
  bg-01, bg-02

- GEI_nm_organised.ipynb: Generates GEI for NM subsets only:
  nm-01, nm-02, nm-03, nm-04, nm-05, nm-06

- GEI_TEST_BG2.ipynb: Generates GEI for BG test subset:
  bg-02

- GEI_TEST_CL2.ipynb: Generates GEI for CL test subset:
  cl-02

- GEI_TEST_NM5,6.ipynb: Generates GEI for NM test subsets:
  nm-05, nm-06

- GEI_TRAIN_BG1.ipynb: Generates GEI for BG training subset:
  bg-01

- GEI_TRAIN_CL1.ipynb: Generates GEI for CL training subset:
  cl-01

- GEI_TRAIN_NM1-4.ipynb: Generates GEI for NM training subsets:
  nm-01, nm-02, nm-03, nm-04
