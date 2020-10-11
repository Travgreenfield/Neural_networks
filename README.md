# Neural Networks Challenge

An analysis of charitable contributions and their predicted success utilizing a variety of neural network parameters.

## Preprocessing

### DataFrame Manipulation

Split out the "IS_SUCCESSFUL" column to serve as our lable, keeping the rest of the columns (minus NAME and EID) to serve as our features.

### Encoding

Used hot encoding to break up our 7 categorical columns. The only two that required binning were APPLICATION_TYPE and CLASSIFICATION. A threshold of <100 and <300 were used respectively which resulted in relatively even buckets outside of the most frequent choice in both which greatly outweighed the other categories.

## Model 1 Summary and Results

Inputs: 45 to match the number of variable columns utilized
Nodes: 45 as well -- meeting the minimum needed with our first model
Hidden Layers: 2, the first using a 'relu' activation function and the second using a sigmoid that would help distinguish our 0-1 binary output.
Epochs: A relatively modest 50 to start to get an initial idea of the computing power and time needed for the model.

### Results
Loss: 0.5520957708358765, Accuracy: 0.7278134226799011

~2.3% under target goal

## Updates

Epochs from 50 up to 300

## Model 2 Results

Loss: 0.5584732890129089, Accuracy: 0.7300291657447815

Not a huge improvement although closer to our goal of 75% accuracy.

## Updates

Added an additional hidden layer with another 'relu' activation formula consisting of 10 neurons.
Dropped the epochs from 300 back down to 100

## Model 3 Results

Loss: 0.5558417439460754, Accuracy: 0.7297959327697754

Dropped a bit in accuracy although not significantly.

## Final analysis

Not quite 75%, although we did see some improvement over the inital model by adding on additional layers in addition to providing the model with more epochs to initiate over.

Next steps: a deeper analysis of the individual variables may be needed here. For example, leveraging institutional knowledge to drop input that may not be having an impact. Additionally, that would allow us to increase the amount of neurons, hidden layers, and epochs without taking a hit to computational resources.
