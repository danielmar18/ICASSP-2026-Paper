# ICASSP-2026-Paper
This repository contains data used for figures and analysis presented in a paper submission to ICASSP 2026.

Using the MobileNetV2 and VisionTransformer (ViT-b16) through PyTorch and the [ImageNet Validation set](https://www.kaggle.com/datasets/titericz/imagenet1k-val), experiments pertaining to the relationship between JPEG's quality factor (QF) values and resulting prediction accuracy were conducted and the data recorded to .csv files. Two different batch-sizes were used, 1 and 50, with the former giving image-level data and the latter class-level data thanks to the sequential nature of the dataset and absence of data shuffling. Experiments were conducted on QF values between 50 and 98.

Directory names in this repository indicate which model were used to generate the data within them. The data has been compressed into zip files due to the sheer size of data source. Zip-file names denote the batchsize used for its data, while filenames within the directories (once unzipped) denote the QF value used for the experiment.

The data fields recorded were batch ID, average batch bitrate (in bits per pixels or BPP), and average batch prediction accuracy (which is either 0 or 1 for batchsize 1). **The files contain no headers or index columns**, with the structure being the following:

|Batch ID| Avg. BPP| Avg. Acc.|
|---|---|---|

So files using batch size 50 will look similar to:

|| | |
|---|---|---|
|0|1.96|0.92...|
|1|1.29|0.86...|
|...|...|...|

while files using batch size 1 will look similar to:

|| | |
|---|---|---|
|0|1.62|0.0...|
|1|1.74|1.0...|
|2|2.61|0.0...|
|...|...|...|


## Change Log
|Date|Changes|
|---|---|
|**13/09/2025**|Repository created and data uploaded|
