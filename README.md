# FGAS
Chang Liu, **Zhong Yuan***, Baiyang Chen,Hongmei Chen, and Dezhong Peng, [Fuzzy granular anomaly detection using Markov random walk](MFGAD_code/2023-FGAS.pdf), Information Sciences, vol. 646, no. 119400, 20 July 2023, DOI: [10.1016/j.ins.2023.119400](https://doi.org/10.1016/j.ins.2023.119400). (Code)

## Abstract
Fuzzy information granulation is an important mathematical model in the theory of granular computing that can effectively handle fuzzy or uncertain information. To address the deficiencies of existing anomaly detection techniques that are mainly suitable for certainty data, this study proposes an anomaly detection method based on fuzzy granules. This method uses the fuzzy information granulation model as a unified framework to gradually develop a fuzzy granular anomaly detection method for calculating the anomaly score of each sample. First, the fuzzy granular distance is defined by fusing single-attribute fuzzy granules to represent the dissimilarity between two samples. Second, a matrix is constructed using the fuzzy granular distance between the samples as the state transition matrix of the Markov random walk. Anomalies in the dataset are then detected using the stationary distribution generated by iterative calculations. Finally, the fuzzy granular anomaly score for each object is obtained by normalizing the stationary
distribution. Experiments are conducted on public datasets to compare the proposed method with some state-of-the-art anomaly detection methods. The results indicate that the proposed method is effective. The code is publicly available online at [https://github .com/BElloney/FGAS](https://github.com/BElloney/FGAS).

## Usage
You can run Demo_FGAS.m or FGAS.py:
```
clc;
clear all;
format short

load Example.mat

Dataori=Example;

trandata=Dataori;
trandata=normalize(trandata,'range');

sigma=0.6;
anomaly_score=FGAS(trandata,sigma)

```
You can get outputs as follows:
```
anomaly_score =
   0.1390
    0.0539
    0.3785
    0.0011
    0.3655
         0
    0.4530
    1.0000
    0.1325
    0.1692
```

## Citation
If you find FGAS useful in your research, please consider citing:
```
@article{liu2023fuzzy,
  title={Fuzzy granular anomaly detection using Markov random walk},
  author={Liu, Chang and Yuan, Zhong and Chen, Bai Yang and Chen, Hong Mei and Peng, De Zhong},
  journal={Information Sciences},
  volume={646},
  pages={119400},
  year={2023},
  doi={10.1016/j.ins.2023.119400},
  publisher={Elsevier}
}
```
