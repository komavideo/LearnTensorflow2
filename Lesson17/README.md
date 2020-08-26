数组比较
========

## 知识点

* Tensorflow中数组的比较

## 实战演习

~~~python
import tensorflow as tf
import numpy as np

def log(prefix="", val=""):
    print(prefix, val, "\n")

a = tf.random.uniform((1,10), minval=0, maxval=10, dtype=tf.int32)
b = tf.random.uniform((1,10), minval=0, maxval=10, dtype=tf.int32)

log("a:", a)
log("b:", b)

# a,b数组比较
log("a==b", a==b)
# 相同元素输出
log(a[a==b])
# 相同元素索引位置输出
log(tf.where(a==b))
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
