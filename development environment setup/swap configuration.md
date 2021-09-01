### Swap configuration

- use Nano default zram 2G of four 512 MB partitions.

- plug `jtop → memory → swap enable`, will add a new /swfile 2G.　[🖺](https://github.com/tingkts/Nvidia-Jetson-Nano/blob/main/assets/jtop%20%E2%86%92%204MEM%20%E2%86%92%20Swap.png)

&emsp;the final sawp configuration as [here](https://github.com/tingkts/Nvidia-Jetson-Nano/blob/main/assets/swap%20size%204G.png), 4G swap size is enough.

&emsp;Ref:
</br>&emsp;&emsp; - [Course > Getting Started with AI on Jetson Nano > Setting up your Jetson Nano > Introduction and Setup](https://courses.nvidia.com/courses/course-v1:DLI+S-RX-02+V2/courseware/b2e02e999d9247eb8e33e893ca052206/63a4dee75f2e4624afbc33bce7811a9b/?child=first)&emsp;[➚](../assets/nvidia%20course%20swap%20settings.png)
</br>&emsp;&emsp; - [JetsonHacksNano/installSwapfile: Install a swap file on the NVIDIA Jetson Nano Developer Kit. This should help with memory pressure issues.](https://github.com/JetsonHacksNano/installSwapfile/blob/master/installSwapfile.sh)