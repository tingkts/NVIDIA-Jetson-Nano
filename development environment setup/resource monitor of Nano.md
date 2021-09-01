Nano no [nvidia-smi](https://developer.nvidia.com/nvidia-system-management-interface), the alternative solutions are,

- use `tegrastats | grep GR3D` to print GPU loading&ensp;[➚](https://blog.csdn.net/wc996789331/article/details/90901666?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-3.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-3.control)

- `jtop` of `jetson-stats`&ensp;[➚](https://blog.csdn.net/biubiubiu617/article/details/107984931)

    ```shell
    # install / upddate
    pip install jetson-stats
    pip install -U jetson-states

    jtop
    jetson_release
    ```
- [top](https://man7.org/linux/man-pages/man1/top.1.html)
- [free](https://man7.org/linux/man-pages/man1/free.1.html)

