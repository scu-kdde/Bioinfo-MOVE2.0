# MOVE
This repository contains the source code for our paper 
*Cross-view contrastive representation learning approach to predicting DTIs via integrating multi-source information*.

This is a major-value-added extension of our paper “MOVE: Integrating Multi-source Information
for Predicting DTI via Cross-view Contrastive Learning”, which
was a regular paper of the IEEE BIBM 2022 Conference. 
In this work, we propose an end-to-end model named MOVE, to integrate multi-source information for predicting DTI via cross-view contrastive
learning. MOVE extracts information from the sequence view and
the network view, then utilizes a fusion module with auxiliary
contrastive learning to facilitate the fusion of representations.
We make an improvement in introducing the new content of “Downstream Task Interface” in this paper.


## Environment:  

  python:3.7.6  
  
  torch:1.4.0  
  
  scikit-learn:0.22.1  
  
  pandas:1.0.1  
  
  numpy:1.18.1  

  
## start:  
Drug-Target Interaction Prediction(MOVE2.0):

`python main.py`       

Drug Classification(Drug_jackknife):

`python main_multilabel.py`      

Target(Protein) Classification(Target_classify):

`python main.py` 

## Baselines:  
### For DTI Task:

For all models, we ran 10-fold cross-validation tests on all positive pairs and a set of randomly sampled negative pairs, whose number was the same as many as that of positive samples. For each fold, a randomly chosen subset of 90% positive and negative pairs was used as training data, and the remaining 10% positive and negative pairs were held out as the test set. The final performance of the model takes the average of the 10-fold results. We repeated five times on this basis.

CMF: We adopt the implementations in  CMF from the publicly available code (https://github.com/hansaimlim/wiZAN/tree/master/PyDTI) with default parameter settings.

MultiDTI: We adopt the implementations in MultiDTI from the publicly available code (https://github.com/Deshan-Zhou/MultiDTI/) with default parameter settings, but didn’t adopt oversampling.

TransformerCPI: We adopt the implementations in TransformerCPI from the publicly available code (https://github.com/lifanchen-simm/transformerCPI) with default parameter settings.

MolTrans: We adopt the implementations in MolTrans from the publicly available code (https://github.com/kexinhuang12345/moltrans) with default parameter settings.

HampDTI: We adopt the implementations in HampDTI from the publicly available code (https://github.com/MacroHongZ/HampDTI) with default parameter settings.

DTINet: We adopt the implementations in DTINet from the publicly available code (https://github.com/luoyunan/DTINet) with default parameter settings.

NeoDTI: We adopt the implementations in NeoDTI from the publicly available code (https://github.com/FangpingWan/NeoDTI) with default parameter settings.

HAS: We report the results from their original paper because the code is unavailable.

### For Protein classification task:

For all models, we ran a 10-fold cross-validation test on our constructed
dataset. For each fold, a randomly chosen subset of 90% of samples was used as the training set, and the remaining 10% of samples were held out as the test set. The final performance of the model takes the average of the 10-fold results.

CNN, LSTM, ResNet, Transformer: We adopt the implementations from the publicly available code (https://github.com/DeepGraphLearning/PEER_Benchmark) with default parameter settings.

HeCo: We adopt the implementations in HeCo from the publicly available code (https://github.com/liun-online/HeCo) with default parameter settings.

DMGI: We adopt the implementations in DMGI from the publicly available code (https://github.com/pcy1302/DMGI) with default parameter settings.

### For Drug classification task:

In order to make a fair comparison with previous methods, we have utilized the same dataset employed by these methods for our experiments and also tested the experimental results with the jackknife.

For other models, we report the results from their original paper.