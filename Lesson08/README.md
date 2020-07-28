维度变换之reshape
================

## 知识点

* 使用tf.reshape方法变化数组维度

## 实战演习

~~~python
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '3'
os.system("cls")

import tensorflow as tf
import numpy as np

# 10张彩色图片
a = tf.random.normal([10,28,28,3])
print(a)
print(a.shape) # 形状
print(a.ndim)  # 维度

b = tf.reshape(a, [10, 784, 3])
print(b)
print(b.shape) # 形状
print(b.ndim)  # 维度

c = tf.reshape(a, [10, -1, 3])
print(c)
print(c.shape) # 形状
print(c.ndim)  # 维度

d = tf.reshape(a, [10, 784*3])
print(d)
print(d.shape) # 形状
print(d.ndim)  # 维度

e = tf.reshape(a, [10, -1])
print(e)
print(e.shape) # 形状
print(e.ndim)  # 维度
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
