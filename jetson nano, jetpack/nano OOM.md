Nano RAM is only 4G, plus Swap 4G. It's easy to encounter Out Of Memory issue. Here are some solutions to reduce OOM issues.

- turn of Graphic UI

	- [ubuntu关闭图形用户界面 - Google 搜尋](https://www.google.com/search?q=ubuntu%E5%85%B3%E9%97%AD%E5%9B%BE%E5%BD%A2%E7%94%A8%E6%88%B7%E7%95%8C%E9%9D%A2&rlz=1C1GCEU_zh-TWTW892TW892&oq=ubuntu%E5%85%B3%E9%97%AD%E5%9B%BE%E5%BD%A2%E7%94%A8%E6%88%B7%E7%95%8C%E9%9D%A2&aqs=chrome..69i57.43748j0j7&sourceid=chrome&ie=UTF-8)
	- [Ubuntu18.04 关闭和开启图形用户界面_执念如此Arcon的博客-CSDN博客_ubuntu18.04关闭图形界面](https://blog.csdn.net/happy_lucky52/article/details/82626901)
	- [玩转Jetson Nano（六）安装caffe_beckhans的博客-CSDN博客_jetson nano安装caffe | OOM关闭图形显示介面](https://blog.csdn.net/beckhans/article/details/89393280)

    ```shell
	# turn off Graphic UI
	sudo systemctl set-default multi-user.target
	sudo reboot

	# turn on Graphic UI
	sudo systemctl set-default graphical.target
	sudo reboot
    ```

- Use CPU to replace GPU

	- [解决TensorFlow GPU版出现OOM错误_lzhero的博客-CSDN博客](https://blog.csdn.net/weixin_42007359/article/details/84634600)


    ```shell
    # Do not use GPU for prediction, only use CPU for prediction, because generally CPU memory is larger than GPU memory.

    import os
    os.environ["CUDA_VISIBLE_DEVICES"] = ""

     # The quotation marks are filled with the serial number of the GPU. When it is not filled, it means that the GPU is not used.
    ```


- Tensorflow GPU config

    - [Use a GPU  |  TensorFlow Core](https://www.tensorflow.org/guide/gpu)
    - [Limiting GPU memory growth](https://www.tensorflow.org/guide/gpu#limiting_gpu_memory_growth)

    ```python
    # show the function was executed in GPU or CPU
	tf.debugging.set_log_device_placement(True)

	gpus = tf.config.list_physical_devices('GPU')
	if gpus:
	  # Restrict TensorFlow to only use the first GPU
	  try:
	    tf.config.set_visible_devices(gpus[0], 'GPU')
	    logical_gpus = tf.config.list_logical_devices('GPU')
	    print(len(gpus), "Physical GPUs,", len(logical_gpus), "Logical GPU")
	  except RuntimeError as e:
	    # Visible devices must be set before GPUs have been initialized
        print(e)

    # dynamic memory allocatino
    gpus = tf.config.experimental.lst_physical_devices('GPU')
    for gpu in gpus:
        tf.config.experimental.set_memory_growth(gpu, True)

    # fixed memory size
    gpus = tf.config.experimental.lst_physical_devices('GPU')
    if gpus:
        tf.config.experimental.set_virtual_device_configuration(gpus[0], [tf.config.experimental.VirtualDeviceConfiguration(memory_limit=1024*2)])
    ```