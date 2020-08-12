2范数的计算 - tf.norm
====================

## 知识点

* 使用tensorflow提供的2范数函数计算向量

## 2范数定义

平方和开根号

## 实战演习

~~~python
import tensorflow as tf
import numpy as np

def log(prefix="", val=""):
    print(prefix, val, "\n")

# 2范数：平方和开根号
a = tf.fill([1,2], value=2.)
log("a:", a)
b = tf.norm(a) # 计算a的范数
log("a的2范数b:", b)

# 计算验证
a = tf.square(a)
log("a的平方:", a)

a = tf.reduce_sum(a)
log("a平方后的和:", a)

b = tf.sqrt(a)
log("a平方和后开根号:", b)

# a = tf.range(10, dtype=tf.float32)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
