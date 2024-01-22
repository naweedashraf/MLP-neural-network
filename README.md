# MLP neural network implementation
you can build your MLP neural network by creating an instance of `neuralNetwork`.

## Parameters:
### layers
an array specifying the number of layers and the number of neurons in each layer.

### activation
activation function used for hidden layers.<br>
you can pass `sigmoid`, `relu` and `linear` values.

### output_activation (optional, default = 'sigmoid')
activation function used for output layer.<br>
you can pass `sigmoid`, `relu` and `linear` values.

### learning_rate (optional, default = 0.1)
the learning rate at which the neural network will be trained.

### epochs (optional, default = 100)
number of epochs to train the neural network.


## Methods 
### train
trains the neural network.<br>
requires x and y data arrays.

### pred
predicts output of given data.<br>
requires x data array.

## Attributes
### weights
returns weights of the neural network.

### bias
returns biases of the neural network.

### targets
returns the output of each layer in the neural network including input and output layers.

## Example
```
model = neuralNetwork([2,1],'sigmoid','linear',learning_rate = 0.1, epochs = 100)

data = np.array([
  [-2, -1],  # Alice
  [25, 6],   # Bob
  [17, 4],   # Charlie
  [-15, -6], # Diana
])

all_y_trues = np.array([
  [1], # Alice
  [0], # Bob
  [0], # Charlie
  [1], # Diana
])

model.train(data,all_y_trues)
```