# Readme
This project is the final project for the NCHU 2024 Fall semester Computer Vision course and is uploaded by Chiang Chen-Han(江承翰). The goal of this project is to train a MobileNetV3 model for the Brain Tumor MRI Dataset, looking for a possibility of using portable devices to recognize medical images.  
  
The training consist of 5 runs on freezed and unfreezed model, each run uses 5-Fold cross validation, with 6 epochs of training for each fold.
  
本專案是中興大學2024年秋 電腦視覺的期末專題。本專題旨在使用Brain Tumor MRI資料集訓練一個MobileNetV3模型，以探討使用行動裝置來辨識醫學影像的可行性。  
訓練由5次獨立的訓練組成，分別使用凍結與無凍結模型。每次訓練使用5-Fold交叉訓練，每個Fold各6個epoch。

### Meaning of freezed and unfreezed model(定義凍結模型與無凍結模型)
- Freezed model: The model replaced the classification layers of MobileNetV3 with a 4 class linear classification layer. Only the weights of the linear classification layers are modified during training, other weights of the model (feature extraction parts) are freezed and won't be modified.
- Unfreezed model: The model is identical to freezed model, only all the weights of the model will be modified (fine-tuned) during training.
  
- 凍結模型: 本專案將MobileNetV3模型的分類層改為4種類別的分類器。在凍結模型中，只有分類器的權重會在訓練中被更新，其餘權重(特徵提取部分)都被凍結。
- 無凍結模型: 跟凍結模型相同，但所有的權重都會在訓練中被更新。

## Dataset(資料集)
The `Training` and `Testing` directory are the testing and training dataset from the Brain Tumor MRI Dataset on Kaggle. You can also download them from [here](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset).  
  
`Training`跟`Testing`目錄是Kaggle上Brain Tumor MRI Dataset中的資料。可以在[此連結](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)中下載。

## Tensorboard files
The training process is logged via `Tensorboard logger` in pytorch-lightning. Note that there's only 1 log data for each run, so using relative option in tensorboard when viewing the log is advised.
  
資料的訓練過程有使用pytorch-lightning中的`Tensorboard logger`所紀錄。注意每一次獨立訓練中只有1份log data。建議打開Tensorboard中的relative選項方便瀏覽。

## Program files(程式檔)
`CV_Final_freezed.ipynb` and `CV_Final_unfreezed.ipynb` are the training programs for the freezed model and unfreezed model, respectively.
  
`CV_Final_freezed.ipynb`與`CV_Final_unfreezed.ipynb`分別是凍結模型與無凍結模型的訓練程式。

## CV期末專題.pdf and CV期末專題.pptx
These 2 files are the description of the project (written in Traditional Chinese).
  
此兩個檔案是本專案的中文說明。