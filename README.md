# Skin Diseases Image Classification
### About
This project is related to the course with the main goal is to processing the image and building the model to classify skin disease infecting people based on image. The skin diseases types which available on dataset from Kaggle have 8 (eight) types in total.

### Constributor
- Anisya Niken A. N.

### Datasets
Source of dataset: [Kaggle](https://www.kaggle.com/datasets/subirbiswas19/skin-disease-dataset) 

Contains of 1159 images, 8 class.

Classes:
- Bacterial Infections- cellulitis
- Bacterial Infections- impetigo
- Fungal Infections - athlete -foot
- Fungal Infections - nail-fungus
- Fungal Infections - ringworm
- Parasitic Infections - cutaneous-larva-migrans
- Viral skin infections - chickenpox
- Viral skin infections - shingles

Data loaded and preprocessed:
- ImageDataGenerator from TensorFlow to enrich and generalize images, besides we do direct split train dan test set here

### Models
- Transfer Learning: MobileNetV2
- Sequential
- Conv2D layer
- Pooling layer
- Dense layer

Model save into certain formats:
- SavedModel
- TensorFlow Lite
- Tensorflow.js

### Training
Dataset is splitted into training and testing set in portion of 80:20. We use testing set as validation set while monitoring the model training. The model is trained by Adam optimizer and Categorical Crossentropy with the callbacks and class weight.

### Evaluation
The model reachs out the accuracy until 98% for training set and 95% for testing set.

### Recommendation
- Data preparation: Combine multiple datasets from Kaggle to create a larger dataset with over 10,000 samples. Besides, don't forget to check for inconsistent image resolutions in the dataset by displaying or inspecting the shape of images.
- Preventing Overfitting: Add Dropout layers in your model to reduce the likelihood of overfitting; use Weight Decay (L2 Regularization) to keep model weights small and prevent overfitting; perform Cross-Validation to ensure the model generalizes well to new data.
