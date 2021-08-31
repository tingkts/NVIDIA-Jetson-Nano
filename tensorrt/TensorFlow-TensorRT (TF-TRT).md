### TF-TRT

- [Accelerating Inference In TF-TRT User Guide](https://docs.nvidia.com/deeplearning/frameworks/tf-trt-user-guide/index.html)

- [tensorflow/tensorrt: TensorFlow/TensorRT integration](https://github.com/tensorflow/tensorrt)

#### logging

- [tf-trt official page](https://docs.nvidia.com/deeplearning/frameworks/tf-trt-user-guide/index.html#debug-tools)

```
	TF_CPP_VMODULE=segment=2,convert_graph=2,convert_nodes=2,trt_engine=1,trt_logger=2 python …


	TF_CPP_MIN_LOG_LEVEL=2 python …
	TF_CPP_MIN_VLOG_LEVEL=2 python ...

```

- [tf-trt GTC-April2021-How-to-use-ResNetV2-FP16](https://github.com/tensorflow/tensorrt/blob/master/tftrt/examples/presentations/GTC-April2021-How-to-use-ResNetV2-FP16.ipynb)

```
    import os

    os.environ["TF_CPP_VMODULE"]="trt_engine_utils=2,trt_engine_op=2,convert_nodes=2,convert_graph=2,segment=2,trt_shape_optimization_profiles=2,trt_engine_resource_ops=2"

```

- [tf object detection tutorial example](https://tensorflow-object-detection-api-tutorial.readthedocs.io/en/latest/auto_examples/index.html)

```
	importos
	os.environ['TF_CPP_MIN_LOG_LEVEL']='2'

    tf.get_logger().setLevel('ERROR')
```