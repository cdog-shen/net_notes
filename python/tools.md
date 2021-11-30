# python有关的tools

- ## conda

- ### 介绍

    conda是一个包和环境管理器，你可以使用conda来分割不同的python版本以及其中所安装的软件包，并将他们打包成一个个不同的环境，可供调用

- ### Anconda 和 Miniconda

    两者都是基于conda的包管理工具，看名字就可以看出来，mini是精简版，所有程序包都需要自己安装；An是内含有一些用得到的基础包（它认为你能用到的）

    个人推荐安装miniconda，可以自己随意定制环境

    ***在 Windows 上，会随 Anaconda 一起安装一批应用程序：***

  - Anaconda Navigator，它是用于管理环境和包的 GUI

  - Anaconda Prompt 终端，它可让你使用命令行界面来管理环境和包

  - Spyder，它是面向科学开发的 IDE

- ### install
  
    conda正如pip，都是包管理工具，所以也应该有一个软件源，安装好conda后的第一件事就是更新源

    ***清华源***

    ```sh
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    conda config --set show_channel_urls yes
    #最后进行更新
    conda upgrade --all
    ```

- ### Package mangement

    作为一个包管理工具，conda的用法比较像apt-get

    安装包

    ```shell
    conda install (packagename)[==version]
    ```

    移除包

    ```shell
    conda remove/uninstall (packagename)[==version]
    ```

    查询包

    ```shell
    conda search (packagename)
    ```

    查看当前环境下已安装的包

    ```shell
    conda list
    ```

    更新包

    ```shell
    conda update (packagename)
    ```

    但别忘了conda对于python的特殊作用，构建虚拟环境

    创建一个新的虚拟环境

    ```shell
    conda create -n (env_name)
    conda create --name (env_name)
    #在conda中创建虚拟环境时可以指定python版本
    conda create --name py39 python=3.9
    #使用特定包来创建环境
    conda create -n bs beautifulsoup4
    ```

    创建完虚拟环境，必须启用才能够使其生效

    ```shell
    #start
    conda activate env_name
    #stop
    conda deactivate env_name
    #info,当前环境会用 * 标出
    conda info -envs
    ```
