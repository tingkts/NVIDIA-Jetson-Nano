↬&ensp;What's the shape of input/output&ensp;[➚](https://blog.csdn.net/pmj110119/article/details/94739765)

```
In keras, data is expressed in the form of tensors.
When dynamic characteristics are not considered, but only shape is considered,
tensors can be understood in a matrix-like manner.

e.g
         [[1],[2],[3]]                                   The shape of this tensor is (3,1)
         [[[1,2],[3,4]],[[5,6],[7,8]],[[9,10],[11,12]]]  The shape of this tensor is (3,2,2)
         [1,2,3,4]                                       The shape of this tensor is (4,)


input_shape: the shape of the tensor. From the front to the back corresponds to the dimension from the outside to the inside.
input_length: represents the length of the sequence, which can be understood as how many samples there are
input_dim: represents the dimension of the tensor, (it is easy to understand, the input_dim of the previous 3 examples are 2, 3, 1)

Through the two parameters input_length and input_dim, the shape of the tensor can be determined directly.

A common usage: only input_dim=32 is provided, indicating that the input is a 32-dimensional vector, which is equivalent to a first-order tensor with 32 elements, and its shape is (32,). Therefore, input_shape=(32,)
```

op `transpose`

```
    origin shape H W C    —— transpose —→    C H W
         (index) 0 1 2                       2 0 1

    origin_shape.transpose(2,0,1)
```

</br>

↬&ensp;For pre-trained models, some information needs to be checked,</br>
 </br>&emsp;－&ensp;What's the algorithm, MobileNet, ResNet, …
 </br>&emsp;－&ensp;What's the AI framework, tensorflow, keras, pytorch, caffe, …
 </br>&emsp;－&ensp;What's the shape of input, output ?
 </br>&emsp;&emsp;&emsp; ▪ input pre-processing ? Image, resize, reshape, normalization, …
 </br>&emsp;&emsp;&emsp; ▪ output post-processing ?
 </br>&emsp;－&ensp;the special layer, op used ?
 </br>&emsp;－&ensp;the dataset, label file ?
 </br>&emsp;－&ensp;the model config file ?