### [TensorRT Installation Guide](https://docs.nvidia.com/deeplearning/tensorrt/archives/tensorrt-713/install-guide/index.html)

- [NVIDIA TensorRT 7.x Download](https://developer.nvidia.com/nvidia-tensorrt-7x-download)

- [TensorRT-7.1.3.4.Windows10.x86_64.cuda-11.0.cudnn8.0.zip](https://developer.nvidia.com/compute/machine-learning/tensorrt/secure/7.1/zips/TensorRT-7.1.3.4.Windows10.x86_64.cuda-11.0.cudnn8.0.zip)




[NVIDIA CUDA Toolkit Release Notes](https://docs.nvidia.com/cuda/cuda-toolkit-release-notes/index.html)

[cuDNN Archive](https://developer.nvidia.com/rdp/cudnn-archive)






e.g.

- [Nvidia GeForce GTX 1050 Ti](https://www.nvidia.com/content/DriverDownload-March2009/confirmation.php?url=/Windows/471.41/471.41-desktop-win10-64bit-international-dch-whql.exe&lang=us&type=TITAN)
- [CUDA Toolkit 11.0 Download](https://developer.nvidia.com/cuda-11.0-download-archive?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exenetwork)







</br>
</br>

⚠️ TensorRT 7.1.3 Windows 10 installation doesn't include Python API, so Python API isn't supported in Windows 10.

[![Alt Text](../assets/TensorRT%20Windows%2010%20python%20api%20isn't%20supported.PNG "Image Title (optional)")](https://docs.nvidia.com/deeplearning/tensorrt/install-guide/index.html#installing-pip "Link Title (optional)")



</br>

Refs:

- [Windows 安装tensorrt - 简书](https://www.jianshu.com/p/120897d69dca)
- [Win10 安裝 CUDA、cuDNN 教學. 上一篇有介紹如何在 Ubuntu 安裝 CUDA、cuDNN，本篇將要來介紹… | by 李謦伊 | 謦伊的閱讀筆記 | Medium](https://medium.com/ching-i/win10-%E5%AE%89%E8%A3%9D-cuda-cudnn-%E6%95%99%E5%AD%B8-c617b3b76deb)
- [Win10中CUDA、cuDNN的安装与卸载_Sophia_fez的博客-CSDN博客_如何卸载cudnn](https://blog.csdn.net/XunCiy/article/details/89070315)

</br>

---

</br>

#### __Summary of installation steps__ :
</br>

1. Confirm what version of TensorRT to install</br>e.g. [TensorRT-7.1.3.4.Windows10.x86_64.cuda-11.0.cudnn8.0.zip](https://developer.nvidia.com/compute/machine-learning/tensorrt/secure/7.1/zips/TensorRT-7.1.3.4.Windows10.x86_64.cuda-11.0.cudnn8.0.zip)



2. Check the Nvidia GPU model installed on the PC, and update the driver first.</br>
Then query the corresponding CUDA version supported.

3. Download CUDA installation file, double click to install.</br>
⭐ Please note! You must select "Custom Installation", and then only check the "CUDA" you want to install, and don't check other options.</br>&ensp;&ensp;&ensp;Avoid the installation progress being aborted by other non-CUDA package installation failures.

&emsp; &emsp; &emsp; ➥　Must to see the UI of the successful installation, then confirm whether the CUDA path was added into the environment variables.　


4. Select the cuDNN version corresponding to the TensorRT and CUDA versions. </br>Download and decompress the cuDNN zip file, and copy all files to the CUDA directory by directory.

5. Decompress TensorRT-*.*.*.*.Windows10.x86_64.cuda-*.*.cudnn*.*.zip.</br>Place it anywhere you decide called `<tensorrt>`.

    - Add `<tensorrt>/lib` into environment variable。
    - Copy the DLL libraries of `<tensorrt>/lib` into `<cuda>/bin`.



</br>

_< ALL DONE >_

</br>

Verify whether the installation successful :

- enter python console, import tensorflow,</br>
check if there is any abnormal error messages.</br>
If it is correct, you will see the corresponding cuda, cudnn dll is loaded.</br>
&emsp;&nbsp;&nbsp; ![avatar](../assets/cuda%20cudnn%20dll%20loaded.png)


</br>

- Open sampleMNIST by Visual Studio.</br>
Follow the guide to add TensorRT header/library path,</br>
Compile it,</br>
If the build is successful, sample_mnist.exe will be generated,</br>
Finally, execute it in the console.


