# Gravitational-Wave-Detection
Example code used for deep learning methods in detecting gravitational waves with synthetic data.

The data used in the google colab cosists of 300,000, 2 second segments of strain data found in an interferometer. Half of the strain data has characteristic gravitational waves added to them corresponding to slow rotation (SR), fast rotation (FR), and no rotation (NR) core colapse supernovae (CCSN). 

The noise and signal data is stacked and assigned corresponding classification target to noise and signal being 0 and 1. These are then split into training and validation sets.

The architecture used consited of a 1-D convultion network. Using 3 convolution layers and 3 pooling layers that then condense into 2 full connected layers. This produces a binary classification probability that the network will use to determine the acurracy of the prediction given the correct classifcation target.   

After training the model, the model is then tested using the validation data. This returns the accuracy of identifing if a signal was purely noise, or had a gravitational wave signal. SInce this is a binary classification, the accuracy of one result is only important. This also returns a ROC curve of true positive vs. false positive rates.
