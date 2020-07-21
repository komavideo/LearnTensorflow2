生成数据
==========

## 知识点

* 使用Tensorflow中提供的类似numpy的功能生成数据

## 实战演习

~~~python
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '3'
os.system("cls")

import tensorflow as tf
import numpy as np

a = np.ones(12)
print(a)
a = tf.convert_to_tensor(a)
print(a)

a = tf.zeros(12)
print(a)

a = tf.zeros([4,3])
print(a)

a = tf.zeros([4,6,3])
print(a)

b = tf.zeros_like(a)
print(b)

a = tf.ones(12)
print(a)

a = tf.ones_like(b)
print(a)

a = tf.fill([3,2], 10.)
print(a)

a = tf.random.normal([12])
print(a)

a = tf.random.normal([4,3])
print(a)

a = tf.random.truncated_normal([3,2])
print(a)

a = tf.random.uniform([4,3], minval=0, maxval=10)
print(a)

a = tf.random.uniform([12], minval=0, maxval=10, dtype=tf.int32)
print(a)

a = tf.range([12], dtype=tf.int32)
print(a)
b = tf.random.shuffle(a)
print(b)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
