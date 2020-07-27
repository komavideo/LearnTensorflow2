浅析Dense层
==========

## 知识点

* 全连接层Dense的参数

## 实战演习

~~~python
import tensorflow as tf

###################################################
# Dense: y=wx+b
rows = 1
net = tf.keras.layers.Dense(1) # 一个隐藏层，一个神经元
net.build((rows, 1)) # 每个训练数据有1个特征
print("net.w:", net.kernel) # 参数个数
print("net.b:", net.bias) # 和Dense数一样

"""
"""
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
