## Image Classification for Cattle CVD Detection via Retina Images
Objective: Create an image classification model to identify cardiovascular disease
 (CVD) in cattle using retina images.

 ### Dataset description
 
The dataset contains 1,118 RGB retinal images captured using the Optomed Smartscope digital fundus camera, each with a resolution of 1536x1152 pixels in JPG format. These images were collected from the right and left eyes of 100 cattle, of which 52 were diagnosed with Cardiovascular Disease (CVD) and 48 were non-CVD. The dataset is organized into two categories: non-CVD, labeled as "0," comprising 527 images, and CVD, labeled as "1," comprising 591 images.
#### Dataset link - 
https://www.kaggle.com/datasets/animalbiometry/cvd-vs-noncvd-retinal-images-of-cattle
![11](https://github.com/user-attachments/assets/ab0a3300-3694-4ccc-8bbd-144f8d7e01d7)

### Methodology
1. Data Prepocessing - The dataset consisted of retinal images of cattle, categorized as healthy and unhealthy. These images were resized to 224x224 pixels to ensure compatibility with deep learning models. To increase the diversity of the dataset, data augmentation techniques such as rotation, zooming, shifting, and flipping were applied. The dataset was then divided into two parts: 80% for training and 20% for validation.
2. Model Selection and training - Three different models were trained: a custom Convolutional Neural Network (CNN), VGG16, and ResNet18. Among these models, ResNet18 demonstrated the best performance, achieving the highest accuracy on both the training and validation sets.
3. Evaluation Metrics - The models were evaluated on the validation dataset using several metrics, including accuracy, confusion matrix, classification report, and AUC-ROC. The confusion matrix was plotted to visually assess the classification accuracy for the healthy and unhealthy categories. Additionally, the ROC curve was generated, and the AUC-ROC score was computed to evaluate the model’s ability to distinguish between the two classes effectively.
   ![21](https://github.com/user-attachments/assets/e3fe6957-bdae-4efb-8d3c-070f29b5da40)
### Results and Evaluation Scores
Classification report:- 
![31](https://github.com/user-attachments/assets/a3a883ac-db72-42db-bfad-b3eb7a648355)
Confusion Matrix:-
![41](https://github.com/user-attachments/assets/d90824cb-f5cd-4147-91b3-078fc7e8eac3)
AUC-ROC Curve:-
![51](https://github.com/user-attachments/assets/737a9227-60b7-4a31-884f-7372bf99f41e)

### Challenges and Solutions
Challenge 1:
When the model was trained using the custom CNN and VGG16, the training and validation accuracy were very low (around 0.53). This showed that the models were not able to tell the difference between healthy and unhealthy images.

Solution:
The problem was solved by using ResNet18, which gave much better results and a validation accuracy of 0.9. The deeper architecture of ResNet18 helped the model better recognize the differences between healthy and unhealthy images.

Challenge 2:
Another challenge was overfitting, where the model did well on the training data but struggled with the validation data.

Solution:
To solve this, data augmentation techniques like rotation, zooming, shifting, and flipping were used to make the training data more varied. This helped the model perform better on new, unseen images.
