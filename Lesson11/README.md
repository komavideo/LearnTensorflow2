数组的广播
=========

## 知识点

* 使用tf.broadcast_to进行数组广播

## 实战演习

~~~python
import tensorflow as tf
import numpy as np

a = tf.constant([1, 2, 3])
print(a)

x = 1
print(a + x)

b = tf.broadcast_to(a, [3, 3])
print(b)

x = 10
print(b * x)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
