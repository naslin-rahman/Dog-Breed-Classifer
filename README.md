# Dog-Breed-Classifer
We train (or fine-tune) a few different Convolutional neural network (CNN) models to classify 7
dog breeds (Bernese Mountain Dog, Border Collie, Chihuahua, Golden Retriever, Labrador Retriever, Pug, Siberian Husky). We also investigate their dataset bias and cross-dataset performances

## DataSets
We modify two different datasets: [Standard Dog Dataset](https://www.kaggle.com/datasets/jessicali9530/stanford-dogs-dataset) and 
[Dog Breed Images](https://www.kaggle.com/datasets/eward96/dog-breed-images)

### Task 2: Simple CNN
I used the following specifications for my network:
* Convolutional layer 16 filters of size 3x3
* Batch normalization
* Convolutional layer 16 filters of size 3x3
* Batch normalization
* Max Pooling (2x2)
* Convolutional layer 32 filters of size 3x3
* Batch Normalization
* Convolutional layer 64 filters of size 3x3
* Max Pooling
* Dropout (0.5)
* Fully connected (32)
* DropOut

I used Stochastic Gradient Descent as my optimizer, RELU as my activation function and cross-entropy as my cost function. 

### Task 3: Resnet18 (not pre-trained) model on DBI
We use the ResNet18 model from pyTorch for the classification of the images in the DBI dataset. We then test on the entire SDD dataset.

### Task 4: Pretrained ResNet18, ResNet34, and ResNeXt32 on DBI
We use the pre-trained models ResNet18, ResNet34, and ResNeXt32 and
fine-tune the input/output layers on DBI training data. We find the accuracy on DBI test dataset, and also the entire SDD dataset.

[Resources](https://medium.com/@ankitvashisht12/classifying-dog-breed-using-pytorch-abc9f3c5128a)
