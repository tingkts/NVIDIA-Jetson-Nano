### Install TensorFlow in Jetson Platform
- [NVIDIA Deep Learning Frameworks Documentation](https://docs.nvidia.com/deeplearning/frameworks/index.html)

    - [Framework Containers Support Matrix](https://docs.nvidia.com/deeplearning/frameworks/support-matrix/index.html)

    - [TensorFlow compatibility with NVIDIA containers and Jetpack](https://docs.nvidia.com/deeplearning/frameworks/install-tf-jetson-platform-release-notes/tf-jetson-rel.html#tf-jetson-rel)







- [Installing TensorFlow For Jetson Platform](https://docs.nvidia.com/deeplearning/frameworks/install-tf-jetson-platform/index.html)

    - [Official TensorFlow for Jetson Nano!](https://forums.developer.nvidia.com/t/official-tensorflow-for-jetson-nano/71770)

    - [Index of /compute/redist/jp/v45/tensorflow](https://developer.download.nvidia.com/compute/redist/jp/v45/tensorflow/)


    ```python

    // tf 1.5
	pip3 install --extra-index-url https://developer.download.nvidia.com/compute/redist/jp/v45 tensorflow==1.15.5+nv21.6

    // tf 2
    pip3 install --extra-index-url https://developer.download.nvidia.com/compute/redist/jp/v45 tensorflow==2.3.1+nv20.12
	pip3 install tensorflow-2.5.0+nv21.6-cp36-cp36m-linux_aarch64.whl

    ```

    🏁 Verify if tensorflow is installed successfully

    ```python

    python -c "import tensorflow as tf;print(tf.reduce_sum(tf.random.normal([1000, 1000])))"

	$ python
	>>> import tensorflow as tf
	>>> print(tf.__version__)
    1.15.0

    $ python
    >>> import tensorflow as tf # 如果沒有噴Error就代表安裝成功！
    >>> print(tf.add(1, 2))
    ```


    🏁 Install other dependencies

    ```python
    pip install scipy
    pip install pandas
    pip install sklearn
    pip install keras
    pip install opencv-python
    pip install matplotlib
    ```



    <p align="right">✍ The above python/pip point to python3.6/pip3.6</p>
