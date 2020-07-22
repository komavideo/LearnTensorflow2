用用均方误差函数 MSE
==================

## 知识点

* 都说MSE好用，咱们也来用用

## 实战演习

~~~python
import tensorflow as tf

rows = 1
out = tf.random.uniform([rows,10])
print("out:", out)
print("预测值：", tf.math.argmax(out, axis=1), "\n")

y = tf.range(rows)
print("y:", y, "\n")

y = tf.one_hot(y, depth=10)
print("y_one_hot:", y, "\n")

loss = tf.keras.losses.mse(y, out)
print("row loss", loss, "\n")

loss = tf.reduce_mean(loss)
print("总体损失：", loss, "\n")
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
