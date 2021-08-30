[TensorFlow Model Garden](https://github.com/tensorflow/models)

[Tensorflow Object Detection API](https://github.com/tensorflow/models/tree/master/research/object_detection)

</br>

⚠️ tf model needs to correspond to tf version

- [tf 2.3.0 model zoo](https://github.com/tensorflow/models/blob/v2.3.0/research/object_detection/g3doc/detection_model_zoo.md)

- [在Jetson Nano上配置Tensorflow Object Detection API_疯花正猫的博客-CSDN博客](https://blog.csdn.net/qq_19647107/article/details/118912404?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522162798333616780261929193%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=162798333616780261929193&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_v2~rank_v29-2-118912404.first_rank_v2_pc_rank_v29&utm_term=Nano+%2BObject+detection&spm=1018.2226.3001.4187)


</br>
↬&ensp;TF model format :

- TF1 :
    - [Frozen graph](https://stackoverflow.com/questions/60974077/how-to-save-keras-model-as-frozen-graph)
- TF2 :
    - [Checkpoint](https://www.tensorflow.org/guide/checkpoint)
    - [Saved model](https://www.tensorflow.org/guide/saved_model)


</br>
↬&ensp;Examples :

- [models/research/object_detection/colab_tutorials/](https://github.com/tensorflow/models/tree/master/research/object_detection/colab_tutorials)
- [tensorflow-object-detection-api-tutorial](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/auto_examples/index.html)


</br>

↬&ensp;Pre-trained models :

&emsp;http://download.tensorflow.org/models/object_detection/faster_rcnn_inception_v2_coco_2018_01_28.tar.gz

&emsp;http://download.tensorflow.org/models/object_detection/tf2/20200711/faster_rcnn_inception_resnet_v2_640x640_coco17_tpu-8.tar.gz

&emsp;http://download.tensorflow.org/models/object_detection/tf2/20200711/faster_rcnn_inception_resnet_v2_1024x1024_coco17_tpu-8.tar.gz


</br>

↬&ensp;Ref :

- [Object Detection APi物件辨識分類器實作-採用TensorFlow (CPU) 在Windows 10上 | by Qingyang Wu | Medium](https://medium.com/@9821343/object-detection-api%E7%89%A9%E4%BB%B6%E8%AD%98%E5%88%A5%E5%88%86%E9%A1%9E%E5%99%A8%E5%AF%A6%E4%BD%9C-%E6%8E%A1%E7%94%A8tensorflow-cpu-%E5%9C%A8windows-10%E4%B8%8A-83d73065f27f)&ensp;[↗](https://github.com/yanggreen/TensorFlow-ODAPi-on-Windows-10)

- [Ubuntu 2 種安裝 protobuf 的方法 | ShengYu Talk](https://shengyu7697.github.io/ubuntu-protobuf/)

  ```
  sudo apt-get install libprotobuf-dev
  sudo apt-get install protobuf-compiler
  ```

