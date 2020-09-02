2维张量排序
==========

## 知识点

* 2维张量数值排序：tf.sort
* 2维张量索引排序：tf.argsort

## 实战演习

~~~python
import tensorflow as tf
import numpy as np

def log(prefix="", val=""):
    print(prefix, val, "\n")

#################################################
# 声明2维数组a
a = tf.random.uniform([3,5], maxval=10, dtype=tf.int32)
log("a", a)
# a tf.Tensor(
# [[2 5 8 0 4]
#  [1 7 2 4 5]
#  [6 0 2 5 0]], shape=(3, 5), dtype=int32) 

#################################################
# 升序排列
b = tf.sort(a, axis=1, direction="ASCENDING")
log("b", b)
# 降序排列
b = tf.sort(a, axis=1, direction="DESCENDING")
log("b", b)
# b tf.Tensor(
# [[0 2 4 5 8]
#  [1 2 4 5 7]
#  [0 0 2 5 6]], shape=(3, 5), dtype=int32) 
# b tf.Tensor(
# [[8 5 4 2 0]
#  [7 5 4 2 1]
#  [6 5 2 0 0]], shape=(3, 5), dtype=int32) 

#################################################
# 升序排列，返回索引位置
b = tf.argsort(a, axis=1, direction="ASCENDING")
log("b", b)
# 降序排列，返回索引位置
b = tf.argsort(a, axis=1, direction="DESCENDING")
log("b", b)
# b tf.Tensor(
# [[3 0 4 1 2]
#  [0 2 3 4 1]
#  [1 4 2 3 0]], shape=(3, 5), dtype=int32) 
# b tf.Tensor(
# [[2 1 4 0 3]
#  [1 4 3 2 0]
#  [0 3 2 1 4]], shape=(3, 5), dtype=int32) 
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
