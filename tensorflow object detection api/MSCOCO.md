
[COCO - Common Objects in Context](https://cocodataset.org/#home)

[cocodataset/cocoapi](https://github.com/cocodataset/cocoapi)

[cocodataset.org/#download](https://cocodataset.org/#download)

</br>

MS COCO dataset
- usage :
    - train / validation
    - test

- category :

    - object detection 物件辨識
    - segmentation 目標分隔
    - caption 圖像標題
    - keypoint 人體關節點

- tool :
    - [cocoapi](https://github.com/cocodataset/cocoapi)
    - [FiftyOne](https://fiftyone.ai/)

</br>

```
Install python cocoapi :

    clone cocoapi github, https://github.com/cocodataset/cocoapi

    ▪ pip install cython

    ▪ enter cocoapi/PythonAPI

    ▪ python setup.py build_ext --inplace

    ▪ python setup.py build_ext install

    if cython build error, try to install Microsoft Visual C++ 14.0(≥)
```


</br>

Ref.

- [CVDF - Common Visual Data Foundation](http://www.cvdfoundation.org/)

- [ImageNet](https://www.image-net.org/)&ensp;:&ensp;the  another known image recognition dataset

</br>

- [【教學】從COCO Dataset中提取所需的類別資料 - Jason Chen's Blog](https://jason-chen-1992.weebly.com/home/coco-dataset)

- [(一) COCO Python API - 使用篇_Right here, Code is Magic-CSDN博客](https://blog.csdn.net/gzj2013/article/details/82385164)

- [COCO数据集的标注格式 - 知乎](https://zhuanlan.zhihu.com/p/29393415)