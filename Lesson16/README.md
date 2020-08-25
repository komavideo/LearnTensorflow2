最大最小的索引位置
================

## 知识点

* Tensorflow中最大最小的索引位置的取得函数
  + tf.argmax
  + tf.argmin

## 实战演习

~~~python
import tensorflow as tf
import numpy as np

def log(prefix="", val=""):
    print(prefix, val, "\n")

# 定义一个随机数组
a = tf.random.uniform((3,10), minval=0, maxval=10, dtype=tf.int32)
log("a", a)

# 取最大索引位置数组，通常用于取得模型预测结果
b = tf.argmax(a, axis=1)
log("a数组axis=1的最大值索引位置：", b)

# 取最小索引位置数组
b = tf.argmin(a, axis=1)
log("a数组axis=1的最小值索引位置：", b)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
