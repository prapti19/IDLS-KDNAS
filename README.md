# IDLS-KDNAS

## Description

This project revolves around KD-NAS( Knowledge Distillation with Neural Architecture Search), and how KDNAS is a much cheaper process in terms of compute and time to get comparable accuracy as SOTA NAS models.


## Completed project milestones
1. Train a teacher model for CIFAR-10 and get the best accuracy
2. Experiment with various search spaces and search strategies in NAS, to get the best student architecture in terms of time and compute.
3. Retrain the student with the best architecture
4. Do Knowledge Distillation from teacher to student
5. Replicate Step 1-4 with modifications for CIFAR-100

## Code Structure

The Repository is organised as follows:
1. [requirements.txt](requirements.txt) has all the dependencies for setting up the environment
2. The [notebooks](notebooks) folder has 3 notebooks for CIFAR-10 and CIFAR-100 respectively:
 - teacher: to train teacher model. Resnet101 for CIFAR10 and VITB16_224 for CIFAR-100
 - DARTS-search: to search the best search space, from DARTS strategy and then retrain with best architecture to get best student model
 - Knowledge_Distillation: load best teacher and student model and then do response-based KD 




## Instructions to run
1. ``` pip install -r requirements.txt ```
2. For any dataset run the notebooks in the following sequence: train_teacher -> DARTS_search -> Knowledge_Distillation


## Results

<img width="672" alt="CIFAR10_AccVsTime" src="https://github.com/prapti19/IDLS-KDNAS/assets/29619950/0247fef6-fa58-496c-b7ec-778acf22b6ba">
<img width="672" alt="CIFAR100_AccVsTime" src="https://github.com/prapti19/IDLS-KDNAS/assets/29619950/fbe5349d-33a5-400a-8588-33ee65599b12">
<img width="782" alt="NAS_Search_Space" src="https://github.com/prapti19/IDLS-KDNAS/assets/29619950/c30b295a-4782-4bdd-aea0-3e382694c1fc">


