# chexpert_dataset_pytorch
```CheXpert``` is a large dataset of chest X-rays and competition for automated chest x-ray interpretation, which features uncertainty labels and radiologist-labeled reference standard evaluation sets. It consists of 224,316 chest radiographs of 65,240 patients, where the chest radiographic examinations and the associated radiology reports were retrospectively collected from Stanford Hospital. Each report was labeled for the presence of 14 observations as positive, negative, or uncertain. We decided on the 14 observations based on the prevalence in the reports and clinical relevance.

For the 14-disease prediction using CheXpert, download down sampled resolution 11GB (CheXpert-v1.0-small) dataset. Link for the download dataset as following: ```shorturl.at/ikABD```

In this dataset, you are provided a large number of Chest X-ray dataset to classify. The train.csv file provides the ground truth and metadata for the images in the train folder. For each image, we have age, sex, view of X-ray image (Frontal or Lateral), and the label of 14 classes. However, the label is not binary, we have the label -1 standing for undetermined, 1 for positive, and 0 for negative. Your task is finding a way to deal with that problem.

<p align="left">
<img src = "https://github.com/wasay530/chexpert_dataset_pytorch/blob/1b5c7e42319063f0d99d60b8ca523cf180bff619/Pict.png" title= "Dataset training csv" width="800" height="300" alt>
</p>

### Steps for Training CheXpert dataset for the Prediction of 14-diseases:
- Download CheXpert dataset.
- Import libraries
- Read dataset
- Split dataset (train 70%, validation 20%, test 10%)
- Build and train baseline model
- Implement dataset loader
- Define model (DenseNet121)
- Check GPU availability
- Create model & get number if trainable parameters
- Define loss function, optimizer, and learning rate scheduler
- Compute AUROC-score
- Train each epoch
- Evaluate model

### Conclusion
I presented in project a comprehensive approach for building a high-precision computer-aided diagnosis system for common thoracic diseases classification from CheXpert dataset. I investigated almost every aspect of the task including data cleaning, network design, training, and ensembling using PyTorch.
