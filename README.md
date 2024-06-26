README

# EMC

A Robust Windows Malware Classification Refinement for Concept Drift.


## Update after Rebuttal
FPR for all MalwareBazaar experiment (TABLE III)
|    Model     |    FPR    |
| :----------: | :-------: | 
|  ResNet-50   |    3.31   |
|    VGG-16    |    3.22   |
| Inception-V3 |    4.98   |
|    IMCFN     |    2.88   |
|   CBOW+MLP   |    1.73   |
|   MalConv    |    3.99   |
|    MAGIC     |   15.34   |
| Word2Vec+KNN |    7.08   |
|     MCSC     |    5.11   |
|     EMC      |    0.82   |

FPR for all MalwareDrift experiment (pre-drift in TABLE IV)
|    Model     |    FPR    |
| :----------: | :-------: | 
|    IMCFN     |   15.89   |
|   MalConv    |   29.33   |
|   CBOW+MLP   |   17.71   |
|    MAGIC     |   15.50   |
| Word2Vec+KNN |   22.31   |
|     MCSC     |   28.44   |
|     EMC      |   18.68   |

FPR for all MalwareDrift experiment (post-drift in TABLE IV)
|    Model     |    FPR    |
| :----------: | :-------: | 
|    IMCFN     |   60.44   |
|   MalConv    |   79.58   |
|   CBOW+MLP   |   92.31   |
|    MAGIC     |   74.14   |
| Word2Vec+KNN |   59.97   |
|     MCSC     |   61.08   |
|     EMC      |   37.77   |

P-values between each pair of works 
| Model | ResNet-50 | VGG-16 | Inception-V3 | IMCFN | MalConv | CBOW+MLP | MAGIC | Word2Vec+KNN | MCSC | EMC |
| :---: | :-------: | :-----: | :-----------: | :----: | :------: | :-------: | :----: | :-----------: | :---: | :--: |
| ResNet-50 | N/A | 0.03402367 | 0.00018063 | 0.00018165 | 0.00018165 | 0.00018165 | 0.00018165 | 0.00018165 | 0.00018063 | 0.00018165 |
| VGG-16 | 0.03402367 | N/A | 0.00018165 | 0.00018267 | 0.00066660 | 0.00018267 | 0.00018267 | 0.00018165 | 0.00018267 | 0.00018267 |
| Inception-V3 | 0.00018063 | 0.00018165 | N/A | 0.00018165 | 0.00018165 | 0.00018165 | 0.00018165 | 0.00018063 | 0.00018165 | 0.00018165 |
| IMCFN | 0.00018165 | 0.00018267 | 0.00018165 | N/A | 0.00018267 | 0.00018267 | 0.00018267 | 0.00018165 | 0.00018267 | 0.00018267 |
| MalConv | 0.00018165 | 0.00066660 | 0.00018165 | 0.00018267 | N/A | 0.00018267 | 0.00018267 | 0.00018165 | 0.00018267 | 0.00018267 |
| CBOW+MLP | 0.00018165 | 0.00018267 | 0.00018165 | 0.00018267 | 0.00018267 | N/A | 0.00018267 | 0.00018165 | 0.00018267 | 0.00018267 |
| MAGIC | 0.00018165 | 0.00018267 | 0.00018165 | 0.00018267 | 0.00018267 | 0.00018267 | N/A | 0.00018165 | 0.00018267 | 0.00018267 |
| Word2Vec+KNN | 0.00018165 | 0.00018065 | 0.00018063 | 0.00018165 | 0.00018165 | 0.00018165 | 0.00018165 | N/A | 0.00018165 | 0.00018267 |
| MCSC | 0.00018063 | 0.00018267 | 0.00018165 | 0.00018267 | 0.00018267 | 0.00018267 | 0.00018267 | 0.00018165 | N/A | 0.00018165 |
| EMC | 0.00018165 | 0.00018267 | 0.00018165 | 0.00018267 | 0.00018267 | 0.00018267 | 0.00018267 | 0.00018165 | 0.00018267 | N/A |

Specific experiment results to calculate p-values:

my_classifier = [0.9912, 0.9923, 0.9934, 0.9951, 0.9921, 0.9858, 0.9835, 0.9877, 0.9902, 0.9875]#EMC

classifier_1 = [0.9683, 0.9645, 0.9655, 0.9677, 0.9656, 0.9643, 0.9635, 0.9659, 0.9642, 0.9655]#ResNet

classifier_2 = [0.9656, 0.9624, 0.9649, 0.9651, 0.9623, 0.9643, 0.9633, 0.9645, 0.9638, 0.9611]#VGG

classifier_3 = [0.9573, 0.9545, 0.9566, 0.9547, 0.9567, 0.9556, 0.9568, 0.9566, 0.9555, 0.9558]#Inception

classifier_4 = [0.9747, 0.9744, 0.9738, 0.9727, 0.9739, 0.9710, 0.9705, 0.9722, 0.9731, 0.9732]#IMCFN

classifier_5 = [0.962, 0.9618, 0.9611, 0.9605, 0.9607, 0.9609, 0.9606, 0.9615, 0.9617, 0.9591]#MalConv

classifier_6 = [0.98, 0.9779, 0.9788, 0.9798, 0.9797, 0.9794, 0.9787, 0.9791, 0.9782, 0.9783]#CBOW+MLP

classifier_7 = [0.8745, 0.8539, 0.8637, 0.8449, 0.8458, 0.8669, 0.8538, 0.8612, 0.8522, 0.8499]#MAGIC

classifier_8 = [0.9379, 0.9368, 0.9358, 0.9371, 0.9362, 0.9358, 0.9370, 0.9377, 0.9372, 0.9369]#Word2Vec+KNN

classifier_9 = [0.947, 0.946, 0.9458, 0.9461, 0.9455, 0.9423, 0.9438, 0.9429, 0.9422, 0.9425]#MCSC


## Setup

* `IDA Pro`: >= 7.5
* `pytorch`==1.7.0 
* `cudatoolkit`=11.1
* `datasets`==1.18.3
* `transformers`==4.16.2
* `tensorboard`==2.8.0

## Dataset

The dataset `MalwareBazaar` `MalwareDrift` and label files `MalwareBazaar_Labels.csv` `MalwareBazaar_Labels.csv` used in this paper and code come from the following paper.

\[FSE2021\] [A Comprehensive Study on Learning-Based PE Malware Family Classification Methods.](https://dl.acm.org/doi/abs/10.1145/3468264.3473925)

Dataset:<https://github.com/MHunt-er/Benchmarking-Malware-Family-Classification>


## Experimental Settings

|    Model     | Optimizer | Learning Rate | Batch Size |                     Input Format                      |
| :----------: | :-------: | :-----------: | :--------: | :---------------------------------------------------: |
|  ResNet-50   |   Adam    |     1e-3      |     64     |                  224*224 color image                  |
|    VGG-16    |    SGD    |    5e-6**     |     64     |                  224*224 color image                  |
| Inception-V3 |   Adam    |     1e-3      |     64     |                  224*224 color image                  |
|    IMCFN     |    SGD    |    5e-6***    |     32     |                  224*224 color image                  |
|   CBOW+MLP   |    SGD    |     1e-3      |    128     |       CBOW: byte sequences; MLP: 256*256 matrix       |
|   MalConv    |    SGD    |     1e-3      |     32     |                  2MB raw byte values                  |
|    MAGIC     |   Adam    |     1e-4      |     10     |                         ACFG                          |
| Word2Vec+KNN |     -     |       -       |     -      | Word2Vec: Opcode sequences; KNN distance measure: WMD |
|     MCSC     |    SGD    |     5e-3      |     64     |                   Opcode sequences                    |
|     EMC      |   Adam    |     5e-5      |     12     |                Orient-opcode sequences                |

Early Stopping Patience: 10


## Useage (Update after Rebuttal)

Download Dataset

Download the MalwareBazaar_Labels.csv and MalwareDrift_Labels.csv from [Benchmarking-Malware-Family-Classification
](https://github.com/MHunt-er/Benchmarking-Malware-Family-Classification/tree/main/Datasets)

Download the samples from [MalwareBazaar website](https://bazaar.abuse.ch/api/) according to their hash names.


Disassembly (On Windows System)

Put the `auto_opcode.py`  `opcode_extraction.py` in the IDA Pro working directory. 

Put the raw malware binary files in the `pefile_dir` and run
```
python auto_opcode.py
```

Feature Process (On Linux System)

Put the output of `auto_opcode.py` in the `folder_path`(modify in opc_trans_sen.py) and run
```
python opc_trans_sen.py
```

Model Training and Validation (On Linux System)

Put the training and verification feature vectors processed by `opc_trans_sen.py` under path `traindir` `valdir`, and run
```
python main_FeatDe.py
```

