# Git简介
### 安装Git
- 在Windows上使用Git，可以从Git官网直接[下载安装程序](https://git-scm.com/downloads)，（网速慢的同学请移步[国内镜像](http://mirrors.ustc.edu.cn/)），然后按默认选项安装即可。
- 安装完成后，在开始菜单里找到"Git"->"Git Bash"，蹦出一个类似命令行窗口的东西，就说明Git安装成功。
- 安装完成后，还需要最后一步设置，在命令行输入：
```Git Bash
    $ git config --global user.name "Your name"
    $ git config --global user.email "email@example.com"
```
    - **注意：此处填写的用户名和邮箱须是你注册GitHub的用户名和邮箱**
    - `git config`命令的`--global`参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址。

### 创建版本库
- 版本库又名仓库，英文名**repository**，你可以简单理解成一个目录，这个目录里面的所有文件都可以被Git管理起来，每个文件的修改，删除，Git都能跟踪，以便任何时刻都可以追踪历史，或者在将来某个时刻可以“还原”。
- 选择一个合适的地方，创建一个空目录：
```Git Bash
    $ mkdir learnGit
    $ cd learnGit
    $ pwd
```
- `pwd`命令用于显示当前目录
- 通过`git init`命令把这个目录变成Git可以管理的仓库：
```Git Bash
    $ git init
```
- 瞬间Git就把仓库建好了，而且是一个空的仓库（empty Git repository），可以发现当前目录下多了一个`.git`的目录，这个目录是Git来跟踪管理版本库的。
- 若没有看到`.git`目录，则是因为这个目录默认是隐藏的，用`ls -ah`或者`ls -a`命令就可以看见。
- 所有的版本控制系统，只能跟踪文本文件的改动，比如TXT文件
网页、所有的程序代码等等，Git也是。而图片、视频这些二进制文件，虽然也能由版本控制系统管理，但没法跟踪文件的变化，只能把二进制文件每次改动串起来，比如：图片从100KB改成了120KB，但具体改动了啥，版本控制系统不知道。
- **MicrosoftWord**是二进制格式，因此，版本控制系统是没法跟踪Word文件的改动的，如果要真正使用版本控制系统，就要以纯文本方式编写文件。
- 强烈建议使用标准的UTF-8编码，所有语言使用同一种编码，既没有冲突，又被所有平台所支持。
- 把一个文件放到Git仓库只需要两步：
    - `$ git add xxx.txt`
    - `$ git commit -m "本次提交说明"`
- Unix的哲学是“没有消息就是好消息”