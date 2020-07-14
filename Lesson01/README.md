自动求导
==========

## 知识点

* 使用tf.GradientTape对函数进行求导

## 官网

https://www.tensorflow.org/api_docs/python/tf/GradientTape

## 实战演习

```
公式：
f(x)=x^n

微分(导数)：
f'(x)=n*x^(n-1)

例：
y=x^2
微分(导数)：
dy/dx=2x^(2-1)=2x
```

## 代码示例

```python
import tensorflow as tf

x = tf.constant(10.)

with tf.GradientTape() as tape:
    tape.watch([x])
    y=x**2

dy_dx = tape.gradient(y, x)
print(dy_dx)
>tf.Tensor(20.0, shape=(), dtype=float32)
```

## 课程文件

https://github.com/komavideo/LearnTensorflow2

## 小马视频频道

http://komavideo.com
