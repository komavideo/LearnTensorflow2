矩阵转置 - transpose
====================

## 知识点

* 矩阵转置：transpose

## 实战演习

~~~python
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '3'
os.system("cls")

import tensorflow as tf
import numpy as np

#####################################################
# 矩阵转置
a = tf.range([12])
a = tf.reshape(a, [4,3])
print(a)

b = tf.transpose(a) # 行列交换
print(b)

# 1张4x4像素的彩色图片
a = tf.random.uniform([4,4,3], minval=0, maxval=10, dtype=tf.int32)
print(a)

# 指定变换的轴索引
b = tf.transpose(a, perm=[0,2,1])
print(b)

# 把刚才的b再变换回来
c = tf.transpose(b, perm=[0,2,1])
print(c)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
