张量排序
========

## 知识点

* 张量数值排序：tf.sort
* 张量索引排序：tf.argsort

## 实战演习

~~~python
import tensorflow as tf
import numpy as np

def log(prefix="", val=""):
    print(prefix, val, "\n")

#################################################
# 声明数组a
a = tf.random.shuffle(tf.range(10))
log("a", a)
# a tf.Tensor([8 2 0 5 7 9 3 1 4 6], shape=(10,), dtype=int32) 

#################################################
# 升序排列
b = tf.sort(a, direction="ASCENDING")
log("b", b)
# 降序排列
b = tf.sort(a, direction="DESCENDING")
log("b", b)
# b tf.Tensor([0 1 2 3 4 5 6 7 8 9], shape=(10,), dtype=int32) 
# b tf.Tensor([9 8 7 6 5 4 3 2 1 0], shape=(10,), dtype=int32) 

#################################################
# 升序排列，返回索引位置
b = tf.argsort(a, direction="ASCENDING")
log("b", b)
# 降序排列，返回索引位置
b = tf.argsort(a, direction="DESCENDING")
log("b", b)
# b tf.Tensor([2 7 1 6 8 3 9 4 0 5], shape=(10,), dtype=int32) 
# b tf.Tensor([5 0 4 9 3 8 6 1 7 2], shape=(10,), dtype=int32) 

#################################################
# 按索引位置b, 从数组a中收集数据
c = tf.gather(a, b)
log("c", c)
# c tf.Tensor([9 8 7 6 5 4 3 2 1 0], shape=(10,), dtype=int32) 
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
