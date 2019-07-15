# Git简介
### 安装Git
- 在Windows上使用Git，可以从Git官网直接[下载安装程序](https://git-scm.com/downloads)，（网速慢的同学请移步[国内镜像](http://mirrors.ustc.edu.cn/)），然后按默认选项安装即可。
- 安装完成后，在开始菜单里找到"Git"->"Git Bash"，蹦出一个类似命令行窗口的东西，就说明Git安装成功。
- 安装完成后，还需要最后一步设置，在命令行输入：
    ```Git Bash
    git config --global user.name "Your name"
    git config --global user.email "email@example.com"
    ```
    **注意：此处填写的用户名和邮箱须是你注册GitHub的用户名和邮箱**
    - `git config`命令的`--global`参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址。