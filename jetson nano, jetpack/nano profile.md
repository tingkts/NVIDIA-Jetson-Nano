
Ubuntu

```shell
ting@ting-desktop:~$ lsb_release -a
No LSB modules are available.
Distributor ID:	Ubuntu
Description:	Ubuntu 18.04.5 LTS
Release:	18.04
Codename:	bionic

```

JetPack

![avatar](https://github.com/tingkts/Nvidia-Jetson-Nano/blob/main/assets/nano%20profile%20-%20jetpack.png)


GPU

```
2021-08-13 14:20:48.536539: I tensorflow/core/common_runtime/gpu/gpu_device.cc:1742] Found device 0 with properties:
pciBusID: 0000:00:00.0 name: NVIDIA Tegra X1 computeCapability: 5.3

lspci
00:02.0 PCI bridge: NVIDIA Corporation Device 0faf (rev a1)

lshw
```


ref:
- [Jetson Nano - GPU Memory usage monitoring - Jetson & Embedded Systems / Jetson Nano - NVIDIA Developer Forums](https://forums.developer.nvidia.com/t/jetson-nano-gpu-memory-usage-monitoring/109656)
