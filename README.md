# Kagge-FOG
This is an overview page for my participation in Kaggle "Parkinson's Freezing of Gait Prediction" competition
https://www.kaggle.com/competitions/tlvmc-parkinsons-freezing-gait-prediction

This competition was a machine learning challenge for labeling time series. The main goal was detecting Parkinson's disease by processing three axis accelerometers readings. We had a training dataset of manually labeled readings to learn from and the task was to label new data. The data consisted of individual files with 100Hz or 128Hz time series from three axis accelerometers attached to patient's backs. We had to label every time slice of those series as one of "walking", "turning" or "trying to walk" freezing of gait events or label them free of those.

# Analysing steps
https://www.kaggle.com/code/vrbaryshev/locating-steps-wavelets-step-rate-feature
In this public notebook I've tried to split the whole movement process into individual steps and calculate dynamic "step rate" feature. I've used wavelet spectrum approach to detect steps and achieved verifiable results. This notebook was recieved well by the community with a silver medal and as many forks as upvotes.

# 1D onvolutional network group approach
[https://www.kaggle.com/code/ernestglukhov/parkinson-s-fog-prediction-by-practicum](https://www.kaggle.com/code/ernestglukhov/practicum-final-1d-cnn-solution)
In this public notebook we offered a group solution for the machine learning challenge where we used 1D convolutional network to tackle the problem. We were quite confident and happy with our results right until the final test day: we confidenly aimed for a silver medal. Regrettably, all convolutional networks performed poorly on the final day when the public test data was substituted with the private test data.

# My private 1D convolutional network approach
https://github.com/VRBarysh/Kagge-FOG/blob/main/Kagge_FOG.ipynb
Here I've tried my own convolutional network approach as an alternative to the group solution. I've utilized a simpler network than we had in a group file, but I've tried to combine two different training datasets in one large dataset to have more data to teach my model on. Initially, we had two datasets with one consisting of scripted lab tests performed by patients and the other consisting of patient's everyday life recorded my three axis accelerometers. Naturally, those datasets had widely different time constraints and had different framerates. So here I attemped to standardize the data and use all of it for training one universal model as an alternative for having two separate models for separate datasets. I've also removed all of the unnecessary padding and file splitting that we had in our group code. Regrettably, I wasn't succesful in improving our final score by teaching one large model instead of two, so we proceeded with the group approach.
