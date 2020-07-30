数组的合并
==========

## 知识点

* 使用tf.concat, tf.stack, tf.unstack合并拆分数组

## 实战演习

~~~python
import tensorflow as tf

####################################################
# 数组合并
# tf.concat
a = tf.zeros([2,4,3])
b = tf.ones([2,4,3])

print(a)
print(b)

# 0轴合并，4,4,3
c = tf.concat([a,b], axis=0)
print(c)

# 1轴合并，2,8,3
c = tf.concat([a,b], axis=1)
print(c)

# 2轴合并，2,4,6
c = tf.concat([a,b], axis=2)
print(c)

# 扩充一维，例如把多个图片放入一个大数组中 -> 2,2,4,3
c = tf.stack([a,b], axis=0)
print(c)

# 降低维数，拆分数组
m, n = tf.unstack(c, axis=0)
print(m)
print(n)
~~~

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
