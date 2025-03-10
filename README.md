# Unsupervised Face Super-Resolution via Integrating Faithful 3D Facial Priors

## Installation

Clone this repo.
```bash
git clone https://github.com/han265/Faith3D-FSR.git
cd Faith3D-FSR/
```

Create the anaconda environment by
```bash
conda env create -f environment.yml
```


## Dataset Preparation

The test sets and training sets can be directly downloaded [here](https://pan.baidu.com/s/1vzpveUTS7SMMEqmvJpD5Sw?pwd=uyh4). After unzipping, put the `data` folder in the root directory.

## Pre-trained Model Preparation

The pre-trained model can be directly downloaded [here](https://pan.baidu.com/s/1vzpveUTS7SMMEqmvJpD5Sw?pwd=uyh4). After unzipping, put the `pretrained` folder in the root directory.

## Inference Using Pretrained Model

Once the dataset and pretrained models are prepared, super-resolution results can be got by

```bash
python run.py --config experiments/test_ffhq_sr.yml
```

The results will be saved at `./results/test_results/`.

## Train New Models

To train the new model, you need to put your own high-resolution and low-resolution face images into `./data/train/high` and `./data/train/low`, respectively, and then
```bash
python run.py --config experiments/train_ffhq_sr.yml
```
The models will be saved at `./results/weights`

## Evaluiton

Please refer to the [IQA-PyTorch](https://github.com/chaofengc/IQA-PyTorch) and [pytorch-fid](https://github.com/mseitzer/pytorch-fid). 

The code is released for academic research use only.
