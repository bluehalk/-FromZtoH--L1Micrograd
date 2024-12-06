
## [From Zero To Hero] #1 Micrograd 

This is a replica of the **Micrograd Project** by **karpathy**, **with some helpful Chinese comments and extended demos for better understanding.** For the video tutoril, please see https://www.youtube.com/watch?v=VMj-3S1tku0

Fundamentally, **the neural network(NN) are just mathematical expressions.** They take the input data and weights as input, with the mathematical expressions, the output is your predictions of your NN.

But backpropagation is much general, it dosen't care about the NN at all. And for simplicity, we do not take n-dimensional tensors that widely use in modern NN as the input, because none of the math changes. This is purely for efficiency. So in purpose of learning chain-rule and backpropagation, I don't think it's pedagogically useful to be dealing with tensors from scratch.

There're two main files:

i. build a tensor type
We construct a class called `Value`. It contains attributes of grad, data, which is similar to `tensor`. You can learn basic chain-rule, and build your own backpropagation in this file. 

ii. from tensor to MLP training
We construct `Module`, `Neuron`, `Layer`, `MLP` classes, which you can better understand the relationship between the atomic building blocks and the entire neural network. Also, it provides a clear demonstration for you to feel how parameters updated through gradients affect the final loss.
