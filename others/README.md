Python2 and Python3 are not compatible

Tensorflow1 and TensorFlow2 are not compatible

TensorRT versions are not compatible

</br>



</br>

---

</br>

*< Misc. >*

- Check if NVIDIA GPU&ensp;:&ensp;  `lspci | grep -i nvidia`

- List packages&ensp;:

   ```shell
    dpkg -l | grep *package name*
    dpkg -L *package name*
   ```

- List Camera support format &ensp;:

   ```shell
    sudo apt-get install v4l-utils
    v4l2-ctl --list-formats-ext
   ```

</br>

---

</br>


*< [NVIDIA NGC](https://ngc.nvidia.com/catalog) >*

- [https://ngc.nvidia.com/setup](https://ngc.nvidia.com/setup)
- [https://ngc.nvidia.com/setup/api-key](https://ngc.nvidia.com/setup/api-key)
- [https://ngc.nvidia.com/setup/installers/cli](https://ngc.nvidia.com/setup/installers/cli)

- [https://ngc.nvidia.com/catalog/containers](https://ngc.nvidia.com/catalog/containers)

 ```shell
    $ docker login nvcr.io
    Username: $oauthtoken
    Password:czBwZGc2ZDFkdnI4ZzJsbGo1b3BrbW9mbG46ZGNjOTBiNGEtNzMzMy00Y2Q3LWIyMDQtN2RiYzZmM2MyYzEy

    # "sudo" is must !!
    $ sudo docker pull nvcr.io/nvidia/tensorflow:21.06-tf1-py3
 ```
&emsp;&ensp;[NGC Nano images](https://ngc.nvidia.com/catalog/containers?orderBy=scoreDESC&pageNumber=0&query=nano&quickFilter=containers&filters=)

&emsp;&ensp; ⚠️ Only the Docker image of Getting start is for Nano. Other NGC images, especially the docker image of tf-trt, are not build arm 64, and fail to start on Nano.

- [Download Docker And Start JupyterLab | S-RX-02 课程页面 | Deep Learning Institute](https://courses.nvidia.com/courses/course-v1:DLI+S-RX-02+V2/courseware/b2e02e999d9247eb8e33e893ca052206/63a4dee75f2e4624afbc33bce7811a9b/?activate_block_id=block-v1%3ADLI%2BS-RX-02%2BV2%2Btype%40sequential%2Bblock%4063a4dee75f2e4624afbc33bce7811a9b)

</br>

 Ref:

- Guide :
    - [Docker 入门教程 - 阮一峰的网络日志](https://www.ruanyifeng.com/blog/2018/02/docker-tutorial.html)
    - [Nvidia-NGC容器配置全過程+ssh配置+鏡像定時備份 - 台部落](https://www.twblogs.net/a/5d6dc164bd9eee541c33bfee)
    - [NVIDIA NGC镜像使用笔记](https://blog.csdn.net/womenrendeme/article/details/106873170?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522162625278016780261968614%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=162625278016780261968614&biz_id=0&utm_medium=distribute.wap_search_result.none-task-blog-2~all~baidu_landing_v2~default-1-106873170.wap_first_rank_v2_rank_v29&utm_term=ngc+image&spm=1018.2118.3001.4450)

 - Issue :
    - [How to fix docker: Got permission denied issue - Stack Overflow](https://stackoverflow.com/questions/48957195/how-to-fix-docker-got-permission-denied-issue)
    - [Failed to run tensorrt docker image on Jetson Nano](https://forums.developer.nvidia.com/t/failed-to-run-tensorrt-docker-image-on-jetson-nano/123483/3)

- Docker commad :

    - [history-docker.txt](../assets/history-docker.txt)
    - [ngc docker startup error.txt](../assets/ngc%20docker%20startup%20error.txt)
