# Determination of formation rock type
This is a simple project, which
identifies shale and sandstone zones by using well log data

**Input** : Well Logs used as input are :
- GR -> Gama Ray log
- SP -> Spontaneous Potential
- Rt & Rxo -> Resistivity logs
- DEN -> Density log
- SONIC -> Sonic log
- CNL -> Neutron log
- DIP -> Dipmeter log

1509 data points were splitted into 2 groups: 
- Training dataset : 1000
- Test dataset : 509

Source of data is one of the well logs in this kaggle datastet: [Link](www.kaggle.com/josephdano/oil-field-reservoir-contour-pvt-well-test/)

**Output** : Mudlogging data displayed as 1 or 0,
- 1 indicates **Shale**
- 0 indicates **Sandstone**


### Methodalogy

Used pytorch to develop a feedforward neural network with one hidden layer, which has 7 nodes.

Activation funtion of hidden layer is ReLU\.
Readout layer has sigmoid func to convert output data into binary 0/1 outputs.

The loss function is Binary Cross Entropy (BCELoss), which is for binary outputs (0 or 1).

