
### TensorRT

- [Documentation Archives :: NVIDIA Deep Learning TensorRT Documentation](https://docs.nvidia.com/deeplearning/tensorrt/archives/index.html)

- [NVIDIA/TensorRT: TensorRT is a C++ library for high performance inference on NVIDIA GPUs and deep learning accelerators.](https://github.com/NVIDIA/TensorRT)
    - [NVIDIA/TensorRT at 7.1.3](https://github.com/NVIDIA/TensorRT/tree/7.1.3)

        - [TRT 7.1.3 C++ API](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/api/c_api/index.html)
        - [TRT 7.1.3 Python API](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/api/python_api/index.html)

- [Working with tensorflow](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/developer-guide/index.html#working_tf)

</br>

- TensorRT support model format :

||DL Framework|ONNX support ?|TensorRT supported model format|
| :-----| :----: |:----: |:----: |
|Google|TensorFlow|No|UFF|
|Facebook|Caffe2|Yes|native support, no conversion required |
||PyTorch|Yes|ONNX |
|Microsoft|CNTK|Yes|ONNX |
|Amazon|MXNet|?|ONNX |

</br>

 - Nouns and parameters

|||
| :-----| :---- |
|Latency (延遲)|Refers to the time it takes to perform an operation|
|Throughput (吞吐量)|In unit time, the number of operations that can be performed|

|||
| :-----| :---- |
|maxBatchSize|Indicates the maximum batch size optimized by TensorRT&emsp;_<*1>_|
|maxWorkspaceSize|Indicates the maximum space (bytes) that can be used by any layer in the network|

&emsp;_<*1>_ &emsp; e.g. total 600 train images, batch size 8 &nbsp;—→ &nbsp;75 batches. One cycle runs 8 images (a batch), for a total of 75 cycles (batches).

</br>

- TRT Engine Serialization

```
    TRT Engine ←——→ .trt file
            Serialize
            Deserialize

    ▪ Not cross-platform
    ▪ Also cannot cross TensorRT version
```

</br>

- Refs :
    - [TensorRT 介紹與安裝教學. TensorRT 是 Nvidia 提出的深度學習推論平台，能夠在 GPU… | by 李謦伊 | 謦伊的閱讀筆記 | Medium](https://medium.com/ching-i/tensorrt-%E4%BB%8B%E7%B4%B9%E8%88%87%E5%AE%89%E8%A3%9D%E6%95%99%E5%AD%B8-45e44f73b25e)
    - [TensorRT(1)-介绍-使用-安装 | arleyzhang](https://arleyzhang.github.io/articles/7f4b25ce/)

</br>
</br>

#### TensorRT samples
- [Sample Support Guide :: NVIDIA Deep Learning TensorRT Documentation](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/sample-support-guide/index.html)

- [trtexec](https://docs.nvidia.com/deeplearning/sdk/tensorrt-developer-guide/index.html#trtexec)


- UFF

|  |  |
| :-----| :---- |
| C++ | [sampleUffMNIST](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/sample-support-guide/index.html#mnist_uff_sample) |
||[sampleUffSSD](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/sample-support-guide/index.html#uffssd_sample)|
||[sampleUffFasterRCNN](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/sample-support-guide/index.html#sampleufffasterrcnn)|
| Python | [uff_ssd](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/sample-support-guide/index.html#uff_ssd) |
||[uff_custom_plugin](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/sample-support-guide/index.html#uff_custom_plugin)|

&emsp;&emsp;[UFF Converter](https://docs.nvidia.com/deeplearning/tensorrt/api/python_api/uff/uff.html)

&emsp;&emsp;[Graph Surgeon](https://docs.nvidia.com/deeplearning/tensorrt/api/python_api/graphsurgeon/graphsurgeon.html)

</br>

- ONNX

|  |  |
| :-----| :---- |
| C++ | [sampleOnnxMNIST](https://docs.nvidia.com/deeplearning/tensorrt/sample-support-guide/index.html#onnx_mnist_sample) |
|  | [sampleDynamicReshape](https://docs.nvidia.com/deeplearning/tensorrt/sample-support-guide/index.html#sample-dynamic-reshape) |
| Python | [introductory_parser_samples](https://docs.nvidia.com/deeplearning/tensorrt/sample-support-guide/index.html#introductory_parser_samples) |
||[yolov3_onnx](https://docs.nvidia.com/deeplearning/tensorrt/sample-support-guide/index.html#yolov3_onnx)|
||[onnx_packnet](https://docs.nvidia.com/deeplearning/tensorrt/sample-support-guide/index.html#onnx_packnet)|

&emsp;&emsp;[ONNX GraphSurgeon](https://github.com/NVIDIA/TensorRT/tree/master/tools/onnx-graphsurgeon)

</br>
</br>

---

</br>

👉&ensp;[NGC TensorRT Container](https://ngc.nvidia.com/catalog/containers/nvidia:tensorrt)</br></br>
👉&ensp;[TensorRT Windows 10 Installattion](./TensorRT%20Windows10%20installation.md)