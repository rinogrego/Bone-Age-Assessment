# Bone Age Assessment

## Project Definition
A class project to determine the impact of gender variable for predicting bone age given an X-ray hand bone image.

In this project, my group compared the performance between two scenarios each with two different models as follow:

## Dataset
The data is downloaded from kaggle competition: https://www.kaggle.com/c/bone-age-regression/data. The data consisted of images and csv files which contain information about the images.

<div align="middle">
    <img src="sample_data\10000.png" height="224" width="224"/> &nbsp; &nbsp;
    <img src="sample_data\10001.png" height="224" width="224"/> &nbsp; &nbsp;
    <img src="sample_data\10002.png" height="224" width="224"/>
</div>

For this project, due to lack of computational resources we only used 5000 observations, with 2500 for each gender (male and female).

## Experiment
We are using a fixed hyperparameter set that applies to all the models.
| Hyperparameter | Value |
| --- | --- |
| Epoch | 30 |
| Learning Rate | 0.001 |
| Batch Size | 32 |
| Optimizers | Adam |
| Evaluation Method | MAE |

As for the models, in total we are using 4 different models for 2 scenarios, created using Keras, where the model takes image as input with shape 224x224x3. Each pixel of the image is rescaled by 1/255 before being fed into the model.
### Scenario 1: One-input CNN model (image)
- Custom CNN model with 32-64-128-256-512 Convolution layers each separated by 2x2 MaxPooling2D layers + 2 FC layers each with 2048 neurons
- VGG19 with imagenet weights + 2 FC layers each with 2048 neurons

### Scenario 2: Multi-input CNN model (gender variable + image)
- Custom CNN model that takes 2 input with 32-64-128-256-512 Convolution layers each separated by 2x2 MaxPooling2D layers + 2 FC layers each with 2048 neurons. The gender variable is connected to 2 64-neurons FC layers before concatenated with CNN layer.
- VGG19 model that takes 2 input with imagenet weights + 2 FC layers each with 2048 neurons. The gender variable is connected to 2 64-neurons FC layers before concatenated with CNN layer.

## Results
Our group are running the model for 5 times with the average results displayed in the table below:
| Custom Model | VGG19 |
| --- | --- |
| ..±.. | ..±.. |
| ..±.. | ..±.. |

Detailed Results
| Attempt | Custom Model | VGG19 |
| --- | --- | --- |
| 1 | .. | .. |
| 2 | .. | .. |
| 3 | .. | .. |
| 4 | .. | .. |
| 5 | .. | .. |

## Conclusion
...

## Future Works
For future works we suggest to 
-   do the same experiment with:
    - different pre-trained models such as ResNet, MobileNet, DenseNet, etc. or by using models developed specifically for this particular problem by other researchers
    - more data
    - with hyperparameter tuning
- always use gender variable for building a bone age regression model to achieve better performance
