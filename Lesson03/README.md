定义变量和常量
============

## 知识点

* 定义变量
* 定义常量

## 实战演习

~~~python
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '3'
os.system("cls")

import tensorflow as tf

################################
# 定义变量
a = tf.Variable(1)
b = tf.Variable(1.)
c = tf.Variable([1.])
d = tf.Variable(1., dtype=tf.float32)

print("-" * 40)
print(a)
print(b)
print(c)
print(d)

# print(a+b)  # error:类型不匹配
print(b+c)    # 注意这里是Tensor类型
print(b+c[0]) # 注意这里是Tensor类型

################################
# 定义Tensor
x1 = tf.constant(1)
x2 = tf.constant(1.)
x3 = tf.constant([1.])
x4 = tf.constant(1, dtype=tf.float32)

print("-" * 40)
print(x1)
print(x2)
print(x3)
print(x4)

print(x2+x3[0])
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
