##  Remote Debugging

### PyCharm - Python


- PyCharm remote interpreter (PyCharm Professional only)
    - [PyCharm ssh - Google 搜尋](https://www.google.com/search?q=PyCharm+ssh&sxsrf=ALeKk03qXICh1lVCLXT7ZDY_Vrs-ZY5fMg:1626924487112&source=lnt&tbs=lr:lang_1zh-CN%7Clang_1zh-TW&lr=lang_zh-CN%7Clang_zh-TW&sa=X&ved=2ahUKEwi3o4WB3vXxAhXmDaYKHTXWDAsQpwV6BAgCECA&biw=1712&bih=793)
    - [教程 | 一步步從零開始：使用PyCharm和SSH搭建遠端TensorFlow開發環境 - IT閱讀](https://www.itread01.com/content/1550109065.html)

- [PyCharm debug with arguments](https://www.google.com/search?q=pycharm+debug+with+arguments&sxsrf=ALeKk00uUrW4eG4sA7Dt0YPqeQOQUDXtiQ:1626942497241&source=lnt&tbs=lr:lang_1zh-CN%7Clang_1zh-TW&lr=lang_zh-CN%7Clang_zh-TW&sa=X&ved=2ahUKEwisn_iMofbxAhWUPZQKHUg-B14QpwV6BAgBECA&biw=1858&bih=977)
    - [pycharm在需要输入命令行参数时如何调试 | 个人博客](https://tanjuntao.github.io/2019/04/30/pycharm%E5%9C%A8%E9%9C%80%E8%A6%81%E8%BE%93%E5%85%A5%E5%91%BD%E4%BB%A4%E8%A1%8C%E5%8F%82%E6%95%B0%E6%97%B6%E5%A6%82%E4%BD%95%E8%B0%83%E8%AF%95/)




### Visual Studio Code - C/C++

1. Install VSCode extension

    - Local VSCode

        - Install Extension of [Remote SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh),
        [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote)vscode-remote-extensionpack)

    - Remote VSCode

        - Install Extensiton of [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)

2. In local VSCode, execute remote SSH connection by UI "Remote SSH: Connect to Host"

3. In remote VSCode, build your target program by gcc or makefile, confirm option "-g" appends in the build flags.

4. In remote VSCode, execute gdbserver of the target program

    ```shell
        # 14399: is the port, can be arbitrarily specified
        # test: is the target program built
        ./gdbserver :14399 test
    ```

5. In local VSCode, edit ["luncher.json"](.\assets\9dae3bba5fb86f6094a62e925ac43a7b.jpg)

    ```json
        “program”： target program in the remote linux system
        “miDebuggerPath” : gdb path in the remote linux system
        “miDebuggerServerAddress”： IP/port in the remote linux system
    ```

6. In local VSCode, add breakpoints and start debugging.

ref:
- VSCode extensions:
    - [vscode配置遠端開發環境並遠端除錯執行C++程式碼的教程_程式設計_程式人生](https://www.796t.com/article.php?id=17651)
    - [vscode C++远程调试运行（学习C++用）_C 语言_脚本之家](https://www.jb51.net/article/184037.htm)

- VSCode configuration:
    - [vscode remote gdb debug- CSDN搜索](https://so.csdn.net/so/search?q=vscode%20remote%20gdb%20debug&t=&u=)
    - [vscode remote 第三方库_VS Code与GDB Server远程调试_weixin_39608479的博客-CSDN博客](https://blog.csdn.net/weixin_39608479/article/details/109981248?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522162987288116780357240795%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=162987288116780357240795&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v29_ecpm-2-109981248.first_rank_v2_pc_rank_v29&utm_term=vscode+remote+gdb+debug&spm=1018.2226.3001.4187)
    - [VSCode GDB调试配置_bingyu的博客-CSDN博客](https://blog.csdn.net/bingyu9875/article/details/94745028?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522162987288216780271544950%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=162987288216780271544950&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~baidu_landing_v2~default-1-94745028.first_rank_v2_pc_rank_v29&utm_term=vscode+remote+gdb+debug&spm=1018.2226.3001.4187)
