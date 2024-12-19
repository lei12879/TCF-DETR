# Multi-scale Token-Channel Fusion Transformer for Enhanced Small Object Detection

This code is based on [RT-DETRv2](https://github.com/lyuwenyu/RT-DETR/tree/main/rtdetrv2_pytorch).
## Setup
```
pip install -r requirements.txt
```
##  Usage
### Data Download
All datasets can be downloaded from the following links. 

[VisDrone2019](https://github.com/VisDrone/VisDrone-Dataset.git)

[TinyPerson](https://universe.roboflow.com/chris-d-dbyby/tinyperson)

[Cityscapes](https://drive.google.com/drive/folders/1mRrJT-CjVwNbQ6iRt4VdZguXrH9iJx9i) 
### Training 
#### Training  on the VisDrone dataset
```
python tools/train.py -c configs\rtdetrv2\tcfdetr_r18vd_visdrone.yml
```
####  Training  on the TinyPerson dataset
```
python tools/train.py -c configs\rtdetrv2\tcfdetr_r18vd_tinyperson.yml
```
####  Training  on the Cityscapes dataset
```
python tools/train.py -c configs\rtdetrv2\tcfdetr_r18vd_cityscape.yml
```
##  Testing
```
python tools/train.py -c path/to/config -r path/to/checkpoint --test-only
```
### Train custom data

set `remap_mscoco_category: False`. This variable only works for ms-coco dataset.
