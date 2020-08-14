最大最小平均值的计算
=================

## 知识点

* tensorflow中最大最小平均值的计算

## 实战演习

~~~python
import tensorflow as tf
import numpy as np

def log(prefix="", val=""):
    print(prefix, val, "\n")

a = tf.range(12, dtype=tf.float32)
a = tf.reshape(a, (4,3))
log("a数组:", a)

b = tf.reduce_min(a)
log("a数组最小值:", b)
b = tf.reduce_max(a)
log("a数组最大值:", b)
b = tf.reduce_mean(a)
log("a数组平均值:", b)

b = tf.reduce_min(a, axis=0)
log("a数组axis=0最小值:", b)
b = tf.reduce_max(a, axis=0)
log("a数组axis=0最大值:", b)
b = tf.reduce_mean(a, axis=0)
log("a数组axis=0平均值:", b)

b = tf.reduce_min(a, axis=1)
log("a数组axis=1最小值:", b)
b = tf.reduce_max(a, axis=1)
log("a数组axis=1最大值:", b)
b = tf.reduce_mean(a, axis=1)
log("a数组axis=1平均值:", b)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
