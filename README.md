# bayesian_uncertainty
This is a joint research project for the Irving Center for Cancer Dynamics/Azizi Lab, Columbia University.
A paper draft is listed in PDF form above, for the quickest summary. 
In this project I build a statistical inference ML pipeline for classifying gene expressions in high-dimensional genome datasets. This is from my position as research assistant at the Azizi Lab for Computational Cancer Biology at Columbia University. Work done in the Google Cloud Platform running PyTorch. The dataset (cells of the adult human heart) contains 18641 cells, each with 26662 genes, totaling ~497 million data points. Implements VAE's to denoise and unpack uncertainty in the gene expression levels of each gene and each gene group. 

VAEBatchEnsemble.py implements HyperBatchEnsemble on a Tensorflow Convolutional VAE to test the baseline effectiveness of HBE on a vanilla VAE. 
SCVI BatchEnsemble.ipynb is a beginning notebook for implementing HBE on the SCVI VAE. Source code for HBE from Uncertainty Baselines. 
Expression_Tests.ipynb runs sampling on 9 gene markers from the fibroblast, smooth muscle, and myeloid cell groups from SCVI training data. Key results from Expression_Tests are shown in SCVI Experimentation.PDF. Plots reveal behavior of these key gene markers over many initializations of SCVI. SCVI training data for 36 initializations found on Azizi Lab GCP: instances/detests (https://console.cloud.google.com/ai-platform/notebooks/list/instances?project=azizilab-aml). 
Statistics.ipynb shows further summary statistics for the 9 key gene markers. 

High level overview of HBE as a method is included in BatchEnsemble Overview. 
For details: @MaxDGU 

Hyper BatchEnsemble Paper: https://arxiv.org/abs/2006.13570 HBE Code: https://github.com/google/uncertainty-baselines
SCVI paper: https://www.nature.com/articles/s41592-018-0229-2.epdf?author_access_token=5sMbnZl1iBFitATlpKkddtRgN0jAjWel9jnR3ZoTv0P1-tTjoP-mBfrGiMqpQx63aBtxToJssRfpqQ482otMbBw2GIGGeinWV4cULBLPg4L4DpCg92dEtoMaB1crCRDG7DgtNrM_1j17VfvHfoy1cQ%3D%3D SCVI Code: https://github.com/YosefLab/scvi-tools
