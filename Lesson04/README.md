变量运行在哪里？
=============

## 知识点

* 注意定义变量时的设备区别

## 实战演习

~~~python
import os
os.environ['TF_CPP_MIN_LOG_LEVEL'] = '3'
os.system("cls")

import tensorflow as tf

################################
# 定义变量后看设备
a = tf.Variable(1)
b = tf.Variable(10.)

print("-" * 40)
print("a.device:", a.device, a) # CPU
print("b.device:", b.device, b) # GPU

################################
# 定义Tensor后看设备
x1 = tf.constant(100)
x2 = tf.constant(1000.)

print("-" * 40)
print("x1.device:", x1.device, x1) # CPU
print("x2.device:", x2.device, x2) # CPU

################################
print("-" * 40)

# CPU+CPU
ax1 = a + x1
print("ax1.device:", ax1.device, ax1) # GPU

# CPU+GPU
bx2 = b + x2
print("bx2.device:", bx2.device, bx2) # GPU

################################
# 指定GPU设备定义Tensor
gpu_a = tf.identity(a)
gpu_x1 = tf.identity(x1)

print("-" * 40)
print("gpu_a.device:", gpu_a.device, gpu_a)
print("gpu_x1.device:", gpu_x1.device, gpu_x1)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
