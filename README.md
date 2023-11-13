# Assignment 2 
# CNNc-for-Image-Classification

# Plant Seedlings Categorized using CNNs for Image Classification![https://github.com/CythizaBK/CNNc-for-Image-Classification/tree/main]

# 1.Prepare data
Downloading plant-seedlings-classification.zip to /content
100% 1.68G/1.69G [00:15<00:00, 117MB/s]
100% 1.69G/1.69G [00:15<00:00, 117MB/s]

# 2.Import python package¶

# 3.Hyperparameter definition¶
img_height = 224
img_width = 224
batch_size = 8

# 4.Data processing pipeline：
Generate dataset：
num_classes=12
len(image_datasets)=4750
len(image_datasets),len(train_set),len(val_set)=(4750, 4000, 750)
image_datasets[0][0].shape, image_datasets[0][1]=(torch.Size([3, 224, 224]), 0)
Generate dataloader
b_img_rgb batch shape: torch.Size([8, 3, 224, 224])
train_labels batch shape: torch.Size([8])
## 4.1. Implementation of data preparation and enhancement
Data set overview: The data set used comes from kaggle's plant seedling classification competition and contains 4750 multi-category images. To unify the model input, the resolution of all images was adjusted to 224x224 pixels. The data set is divided into a training set of 4000 images and a validation set of 750 images.
## 4.2.Data enhancement
In order to improve the model generalization ability, a series of preprocessing and data enhancement operations were performed using the PyTorch framework, including random rotation (±5 degrees), random horizontal flipping, and normalization of the image[10].
Data loading: Use PyTorch's DataLoader class to batch load and randomly shuffle the order of images. The batch size is set to 8 and the images are organized into tensors of shape [8, 3, 224, 224].
## 4.3. Data partitioning and standardization
Randomly divided 80% of the training set and 20% of the test set, and used DataLoader for batch processing to improve training efficiency.

# 5.Determine CPU GPU device

# 6.Training and evaluation loop

# 7.Model CNN
accuracy ：0.763 

# 8.Model resnet18¶
accuracy ：0.824 

## The Classification report of Model resnet18 ¶was accidentally deleted during re-translation. Its original Classification report can be found in the "8.Model resnet18" chapter in the Chinese version code file [ https://github.com/CythizaBK/CNNc-for-Image-Classification/blob/main/Plant_Classification_CNNs_Chinese.ipynb]  in this folder.

# 9. Model swin_transformer
accuracy : 0.896 

# 10.Model vgg13
accuracy : 0.883

# 11. Three models fusion efficientnet+resnet+swinTransformer¶
accuracy : 0.935

# 12. Fusion model parameter tuning:
## 12.1.Integrate model training and parameter tuning-add attention mechanism
accuracy : 0.944 

## 12.2.Integrate model training and parameter tuning-modify MLP and other hyperparameters
accuracy : 0.959
































# I'm very sorry. I have submitted an extension request for Assignment 2 in October.
