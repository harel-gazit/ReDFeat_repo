# ReDFeat


This repository code for multimodal feature ReDFeat. [&#34;RedFeat: Recoupling detection and description for multimodal feature learning&#34;](https://arxiv.org/abs/2205.07439)

## Requirements

The code is build on Pytorch 1.10 and Korina 0.6.2. Later version should also be compatible.

## Build

Clone the repository to your workplace by
```bash
git clone --recurse-submodules -j8 git@github.com:harel-gazit/ReDFeat_repo.git
```

## Datasets

Manually download the OSdataset from one of the links below:

https://drive.google.com/file/d/1hgtj56HUlGSFbl5K1Sw16tKLx6rGXDbT/view?usp=sharing or https://pan.baidu.com/s/17dbmuuVqgoYzkmw7Qg92tQ 提取码：bkro

Clone the zips or the folders into our repository as
```
Multimodal Feature Evaluation
└── VIS-SAR
       ├── OSdataset.zip
       ...
```
Run build.py in child folders as
```
python VIS_SAR/build.py
```

## Training

run 

```bash
python train.py --image_type=VIS_IR --name=IR
```

The major parameters include:

**image_type**: type of modal (VIS_SAR)

**name**: name of checkpoint

**datapath**: path for training data

## Evaluation

Evaluation codes for feature extraction, matching and transform estimation are included in [mutilmodal_feature_evaluation benchmark](https://github.com/ACuOoOoO/Multimodal_Feature_Evaluation):

**extract_ReDFeat.py**: extract ReDFeat for three types of modals.

**match.py**: reproduce feature matching experiments in the paper.

**reproj.py**: reproduce image registration experiments in the paper.
