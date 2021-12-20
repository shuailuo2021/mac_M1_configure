# Mac M1安装miniconda

## 1、下载

官网链接：[Miniconda — Conda documentation](https://docs.conda.io/en/latest/miniconda.html#system-requirements)

![截屏2021-12-20 下午8.07.50](/Users/shuailuo/Desktop/Typora/截屏2021-12-20 下午8.07.50.png)



## 2、安装

打开 `iTerm2` 终端应用程序或 `Terminal.app`，在下载的安装包所在路径运行以下命令：

```
sh Miniconda3-latest-MacOSX-arm64.sh
```

之后按enter--三下空格--输入yes--按enter--输入yes

```
# 激活配置
source ~/.zshrc
```

```
# 检测是否安装成功
conda -V
```

```
若出现command not found之类的命令，可能是需要配置环境变量
如：
zsh: command not found: conda

解决方法：
(1) vim ~/.zshrc,没有该文件的话，自动创建一个；
(2) .zshrc中添加export PATH=/Users/liyuying/miniconda3/bin:$PATH,
    /Users/###/miniconda3/bin 为miniconda的安装路径；
(3) source ~/.zshrc
```



## 3、从 macOS 中完全删除 `Miniconda`

- ##### 打开 `iTerm2` 终端应用程序或 `Terminal.app`。

- ##### 使用以下命令删除整个 `Miniconda` 安装目录。

  ```bash
  rm -rf ~/miniconda
  ```

- ##### `bash_profile` 也可以进一步编辑以从用户的 PATH 环境中删除 `Miniconda` 目录。

  ```bash
  vim ~/.bash_profile
  ```

- ##### 隐藏的文件和文件夹可以选择性地从主目录中进一步删除。

  ```bash
  rm -rf ~/.condarc ~/.conda ~/.continuum
  ```



## 4、