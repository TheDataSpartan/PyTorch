# PyTorch
This repository contains the notebooks that utilizes PyTorch.

# Notes:

### Changing the Shape of a PyTorch Tensor

#### weights.reshape(a, b) 
will return a new tensor with the same data as weights with size (a, b) sometimes, and sometimes a clone, as in it copies the data to another part of memory.

#### weights.resize_(a, b) 
returns the same tensor with a different shape. However, if the new shape results in fewer elements than the original tensor, some elements will be removed from the tensor (but not from memory). If the new shape results in more elements than the original tensor, new elements will be uninitialized in memory. Here I should note that the underscore at the end of the method denotes that this method is performed in-place. Here is a great forum thread to read more about in-place operations in PyTorch.

#### weights.view(a, b) 
will return a new tensor with the same data as weights with size (a, b). It doesn't mess with the data in memory. If you tried to get a new size, a new shape for your tensor with a different number of elements, it'll return an error. This ensure that you will always get the same number of elements when you change the shape of your weights. 

# Helpful Resources:
1. http://web.cs.ucdavis.edu/~yjlee/teaching/ecs289g-winter2018/Pytorch_Tutorial.pdf
2. https://cise.ufl.edu/~xiaoyong/materials/pytorch_tutorial.pdf
