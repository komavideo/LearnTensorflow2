机器(深度)学习开发环境搭建
======================

## 知识点

* 搭建本地开发环境
* Google Colaboratory

## 官网

https://www.tensorflow.org

## 实战演习

~~~bash
# 虚拟环境创建
$ python3 -m venv _pml_
$ source _pml_/bin/activate
$ python -m pip install --upgrade pip
$ python -m pip install --upgrade setuptools
$ pip list
# 安装库
$ pip install tensorflow
$ pip install matplotlib seaborn
$ pip install Pillow opencv-python opencv-contrib-python
$ pip install scikit-learn
$ #pip install numpy pandas # 已包含
# linux only
$ sudo apt install python3-tk
~~~

## 训练测试

### main.py

```python
import numpy as np
import tensorflow as tf
from tensorflow.keras.layers import Flatten, Dense, Dropout
import matplotlib.pyplot as plt

def run():
    ds = tf.keras.datasets.mnist

    (train_x, train_y), (test_x, test_y) = ds.load_data()
    print("train_x.shape:", train_x.shape, ", train_y.shape:", train_y.shape)
    print("test_x.shape:", test_x.shape, ", test_y.shape:", test_y.shape)

    # 正規化
    train_x = tf.keras.utils.normalize(train_x)
    test_x = tf.keras.utils.normalize(test_x)

    # one-hot
    train_y = tf.keras.utils.to_categorical(train_y)
    test_y = tf.keras.utils.to_categorical(test_y)
    print("train_y.shape:", train_y.shape, ", test_y.shape:", test_y.shape)

    model = tf.keras.Sequential()

    # 模型定义（玄学）
    model.add(Flatten(input_shape=[28, 28]))
    model.add(Dense(1000, activation="relu"))
    model.add(Dense(10, activation="softmax"))

    # 模型概要
    model.summary()

    # 编译模型
    model.compile(
        loss=tf.keras.losses.categorical_crossentropy,
        optimizer=tf.keras.optimizers.Adam(learning_rate=0.001),
        metrics=["accuracy"]
    )

    # 训练模型参数
    history = model.fit(train_x, train_y, validation_data=(
        test_x, test_y), epochs=1, batch_size=128)

    score = model.evaluate(test_x, test_y, batch_size=128)
    print("训练评价分数:", score)

    result = model.predict(test_x, batch_size=128)
    print("原始值：", np.argmax(test_y[:20], axis=1))
    print("预测值：", np.argmax(result[:20], axis=1))

run()
```

## 小马视频频道

http://komavideo.com
