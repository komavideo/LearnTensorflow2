[Tensorflow]数据预处理 之 统一数组维度
===================================

## 知识点

* 使用keras的数据预处理函数pad_sequences统一数组维度

## 官网

https://www.tensorflow.org/api_docs/python/tf/keras/preprocessing/sequence/pad_sequences

## 实战演习

~~~python
import numpy as np
import pprint as pp
from tensorflow.keras.preprocessing.sequence import pad_sequences

comment1 = [1,2,3,4]
comment2 = [1,2,3,4,5,6,7]
comment3 = [1,2,3,4,5,6,7,8,9,10]

x_train = np.array([comment1, comment2, comment3], dtype=object)
print(), pp.pprint(x_train)

# 左补0，统一数组长度
x_test = pad_sequences(x_train)
print(), pp.pprint(x_test)

# 左补255，统一数组长度
x_test = pad_sequences(x_train, value=255)
print(), pp.pprint(x_test)

# 右补0，统一数组长度
x_test = pad_sequences(x_train, padding="post")
print(), pp.pprint(x_test)

# 切取数组长度, 只保留后3位
x_test = pad_sequences(x_train, maxlen=3)
print(), pp.pprint(x_test)

# 切取数组长度, 只保留前3位
x_test = pad_sequences(x_train, maxlen=3, truncating="post")
print(), pp.pprint(x_test)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
