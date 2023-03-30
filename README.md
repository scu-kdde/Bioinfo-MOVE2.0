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


## environment:  

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
