维度变换之 expand_dims, squeeze
==============================

## 知识点

* 数组升维：expand_dims
* 数组降维：squeeze

## 实战演习

~~~python
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '3'
os.system("cls")

import tensorflow as tf
import numpy as np

a = tf.range([24])
# a = tf.reshape(a, [4,6])
print(a)
print(a.shape)
print(a.ndim)

# 增加一个维度，相当于[1,2,3]->[[1,2,3]]
b = tf.expand_dims(a, axis=0)
print(b)
print(b.shape)
print(b.ndim)

# 减少维度，相当于[[1,2,3]]->[1,2,3]
c = tf.squeeze(b, axis=0)
print(c)
print(c.shape)
print(c.ndim)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
