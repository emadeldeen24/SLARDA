# Self-supervised Autoregressive Domain Adaptation for Time Series Data (SLARDA) [[Paper](https://arxiv.org/abs/2111.14834)]
#### *by: Mohamed Ragab, Emadeldeen Eldele, Zhenghua Chen, Min Wu, Chee Keong Kwoh, and  Xiaoli Li*
#### This paper has been accepted for publication in the [IEEE Transactions on Neural Networks and Learning Systems (TNNLS)](https://ieeexplore.ieee.org/document/9804766) (Impact Factor: 14.255).

## Abstract
<img src="SLARDA_1.PNG" width="1000">
Unsupervised domain adaptation (UDA) has successfully addressed the domain shift problem for visual applications. Yet, these approaches may have limited performance for time series data due to the following reasons. First, they mainly rely on the large-scale dataset (i.e., ImageNet) for the source pretraining, which is not applicable for time-series data. Second, they ignore the temporal dimension on the feature space of the source and target domains during the domain alignment step. Last, most of the prior UDA methods can only align the global features without considering the fine-grained class distribution of the target domain. To address these limitations, we propose a Self-supervised autoregressive Domain Adaptation (SLARDA) framework. In particular, we first design a self-supervised learning module that utilizes forecasting as an auxiliary task to improve the transferability of the source features. Second, we propose a novel autoregressive domain adaptation technique that incorporates temporal dependency of both source and target features during domain alignment. Finally, we develop an ensemble teacher model to align the class-wise distribution in the target domain via a confident pseudo labeling approach.
Extensive experiments have been conducted on three real-world time series applications with 30 cross-domain scenarios. Results demonstrate that our proposed SLARDA method significantly outperforms the state-of-the-art approaches for time series domain adaptation.

## Requirmenets:
- Python3.x
- Pytorch==1.7
- Numpy
- Sklearn
- Pandas
- mat4py (for Fault diagnosis preprocessing)

### A- Download the dataset from this following links
    - MFD: https://mb.uni-paderborn.de/en/kat/main-research/datacenter/bearing-datacenter/data-sets-and-download
    - HAR: https://archive.ics.uci.edu/ml/datasets/OPPORTUNITY+Activity+Recognitio
    - SSC:https://sleepdata.org/datasets/shhs, https://physionet.org/content/sleep-edf/1.0.0/
### B-  Add dataset to the framework
1- Add the data files in the following format:

    - Each domain splitted to train, val, test files
    - name the domains using small letters, i.e., a, b, c,...
    - Each sample has the following dict format: 
        - samples = data['samples']
        - labels = data['labels']
### Running the model 

1- from args:
    - Select the domain adaptation method as 'SLARDA'
    - Select your target dataset: Paderborn_FD, HAR, EEG
    - Select the corresponding based model: CNN_SL_bn, CNN_Opp_HAR_SL, EEG_M_SL

2- Run 'train_CD.py' script

## Citation
If you found this work useful for you, please consider citing it.
```
@article{slarda_tnnls,
  author={Ragab, Mohamed and Eldele, Emadeldeen and Chen, Zhenghua and Wu, Min and Li, Haoliang and Kwoh, Chee-Keong and Li, Xiaoli},
  journal={IEEE Transactions on Neural Networks and Learning Systems}, 
  title={Self-supervised Autoregressive Domain Adaptation for Time Series Data}, 
  year={2022},
  volume={},
  number={},
  pages={},
  doi={}}
```

## Contact
For any issues/questions regarding the paper or reproducing the results, please contact me.   
Mohamed Ragab    
School of Computer Science and Engineering (SCSE),   
Nanyang Technological University (NTU), Singapore.   
Email: mohamedr002{at}e.ntu.edu.sg   
