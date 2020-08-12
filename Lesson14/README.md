1范数的计算 - tf.norm
====================

## 知识点

* 使用tensorflow提供的1范数函数计算向量

## 1范数定义

所有值的绝对值之和

## 实战演习

~~~python
import tensorflow as tf
import numpy as np

def log(prefix="", val=""):
    print(prefix, val, "\n")

# 定义一个数组
a = tf.range(12, dtype=tf.float32)
a = tf.reshape(a, (4,3))
a = a - 5
log("a:", a)

# 1范数：所有值的绝对值之和
b = tf.norm(a, ord=1)
log("a的1范数b:", b)
print(tf.reduce_sum(tf.abs(a)))

# 指定计算轴：axis=0
b = tf.norm(a, ord=1, axis=0)
log("a的axis=0的1范数b:", b)

# 指定计算轴：axis=1
b = tf.norm(a, ord=1, axis=1)
log("a的axis=1的1范数b:", b)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
