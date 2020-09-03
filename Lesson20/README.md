TopK值取得
==========

## 知识点

* Tensorflow中 top_k() 函数的使用

## 实战演习

~~~python
import tensorflow as tf
import numpy as np

def log(prefix="", val=""):
    print(prefix, val, "\n")

#################################################
# 2维数组定义
a = tf.random.uniform([3,5], maxval=10, dtype=tf.int32)
log("a", a)
# a tf.Tensor(
# [[1 2 5 8 7]
#  [6 1 4 3 9]
#  [5 9 6 5 5]], shape=(3, 5), dtype=int32) 

#################################################
# 取数组每行前3位
b = tf.math.top_k(a, k=3, sorted=True)
# 前3位数值
log("b", b.values)
# 前3位数值索引
log("b", b.indices)

# b tf.Tensor(
# [[8 7 5]
#  [9 6 4]
#  [9 6 5]], shape=(3, 3), dtype=int32) 
# b tf.Tensor(
# [[3 4 2]
#  [4 0 2]
#  [1 2 0]], shape=(3, 3), dtype=int32) 
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
