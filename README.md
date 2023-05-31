# ML-adversarial-scratch-MLP

## Purpose:
Create a Machine Learning model that classifies the sex of faces (male or female) and attempt to disrupt the accuracy of the model via adversarial images using small markings. 

## Methods:
Sourced facial images primarily from **kaggle.com** and worked in Jupyter Notebooks for project development. \
Faces are classified as "Male" or "Female" for training. \
Adversarial images add 3 simple dots below the eye. Dots are placed dynamically below the left or right eye, never in the same place--pixel-wise. While not visually hidden, it is easier for observation and is all the same to the model. 

## Model:
A 3-hidden-layer deep-learning model was used for this task. \
All layers feature Sigmoid for Binary Cross Entropy Loss. \

## Results:
**The model achieved an overall 96% accuracy, reduced to as low as 83% accuracy.** \
| Percent Adversarial Images (%) | Accuracy |
|--------------------------------|----------|
| 0                              | 0.96     |
| 1.25                           | 0.89     |
| 2.5                            | 0.83     |
| 5                              | 0.87     |

## Discussion:
While the base model obtains a very high accuracy when recognizing faces for a simple neural network, its accuracy can clearly be manipulated with adversarial images. 
As adversarial images are added to the dataset, accuracy decreases, if unstable. However, there is a global reduction in accuracy, proving that adversarial images can adversly affect the performance of the model.
