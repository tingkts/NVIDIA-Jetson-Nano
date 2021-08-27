## Getting Start with Nano

- [NVIDIA Jetson Nano Developer Kit | NVIDIA Developer](https://developer.nvidia.com/embedded/jetson-nano-developer-kit)

- [Jetson Modules | NVIDIA Developer](https://developer.nvidia.com/embedded/jetson-modules)

- [Getting Started With Jetson Nano Developer Kit | NVIDIA Developer](https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit)　[↗course](https://courses.nvidia.com/courses/course-v1:DLI+S-RX-02+V2/)　[↗video](https://www.youtube.com/watch?v=uvU8AXY1170&t=711s)

- [Jetson Download Center | NVIDIA Developer](https://developer.nvidia.com/embedded/downloads#?search=Jetson%20Nano%20Developer%20Kit%20User%20Guide)

- [NVIDIA JetPack Documentation](https://docs.nvidia.com/jetson/jetpack/index.html)

- [JetPack SDK | NVIDIA Developer](https://developer.nvidia.com/embedded/jetpack#install)

- [Jetson AI Courses and Certification | NVIDIA Developer](https://developer.nvidia.com/embedded/learn/jetson-ai-certification-programs#course_outline)


### Nano power supply

- [DC power supply](.\assets\DC%20power%20supply.jpg)

- USB cable of micro USB ─ type A, 5V ≥2.1A power supply at least

### Swap configuration

- use Nano default zram 2G of four 512 MB partitions.

- plug `jtop → memory → swap enable`, will add a new /swfile 2G.　[🖺](.\assets\jtop%20→%204MEM%20→%20Swap.png)　[🖺](.\assets\swap%20size%204G.png)

&emsp;the final sawp configuration as below, 4G swap size is enough.