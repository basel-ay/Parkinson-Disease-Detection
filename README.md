# Parkinson-Disease-Detection

# **Introduction**

What is Parkinson's Disease?

Parkinson's disease (PD), or simply Parkinson's is a long-term degenerative disorder of the central nervous system that mainly affects the motor system. The symptoms usually emerge slowly and, as the disease worsens, non-motor symptoms become more common. The most obvious early symptoms are tremor, rigidity, slowness of movement, and difficulty with walking,but cognitive and behavioral problems may also occur. Parkinson's disease dementia becomes common in the advanced stages of the disease. Depression and anxiety are also common, occurring in more than a third of people with PD. Other symptoms include sensory, sleep, and emotional problems. The main motor symptoms are collectively called "parkinsonism", or a "parkinsonian syndrome

![](https://camo.githubusercontent.com/be21545deabab1e7257c04182b631f6f34ebae4b/68747470733a2f2f7061726b696e736f6e736e65627261736b612e6f72672f77702d636f6e74656e742f75706c6f6164732f323032302f30332f50442d4d414e2d31303234783532322e706e67)

While Parkinson’s disease cannot be cured, early detection along with proper medication can significantly improve symptoms and quality of life, making it an important topic for research especially in the creation of new diagnostic tools.

A 2017 study by Zham et al. found that it was possible to detect Parkinson’s by asking the patient to draw a spiral and then track:

 1. Speed of drawing
 2. Pen pressure

The researchers found that the drawing speed was slower and the pen pressure lower among Parkinson’s patients — this was especially pronounced for patients with a more acute/advanced forms of the disease.

We’ll be leveraging the fact that two of the most common Parkinson’s symptoms include tremors and muscle rigidity which directly impact the visual appearance of a hand drawn spiral and wave.

The variation in visual appearance will enable us to train a computer vision + machine learning algorithm to automatically detect Parkinson’s disease.



The dataset itself consists of images and is pre-split into a training set and a testing set, consisting of:

Spiral: training, and testing

Wave: training, and testing

![](https://camo.githubusercontent.com/454ee9a31a3b087992584258f97b5b4a77d87dc7/68747470733a2f2f7079696d6167657365617263682e636f6d2f77702d636f6e74656e742f75706c6f6164732f323031392f30342f6465746563745f7061726b696e736f6e735f646174617365742e6a7067)

**Approach**

Although Deep learning with Convolutional Neural networks seems to be the best approach for this computer vision problem, we have a limited amount of training data and we cannot apply data augmentation as it will lead to a distortion of the results. With this in mind we will rather apply the Histogram of Oriented Gradients Image Descriptor with an ensemble method i.e., Random Forest Classifier and Xgboost

Datasets and Notebook on Kaggle : https://www.kaggle.com/basel99/parkinson-s-disease-detection
