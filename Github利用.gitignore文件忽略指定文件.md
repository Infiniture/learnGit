## Github利用.gitignore文件忽略指定文件

> **.gitignore**：目的是忽略指定类型的文件或者某个文件夹；

- 步骤：

  - 新建`.gitignore`文件；
  - 输入要忽略的文件（可用通配符）；

- `.gitignore`文件实例：

  - `.a`	# 忽略所有.a结尾的文件；
  - `!lib.a` # lib.a除外；
  - `/TODO` # 仅忽略项目根目录下的TODO文件，不包括subdir/TODO；
  - `build/` # 忽略build/目录下的所有文件；
  - `doc/*.txt` # 忽略doc/notes.txt但不包括doc/server/arch.txt；

- 如果遇到配置完成后没有生效，是因为`.gitignore`只能忽略那些原来没有被track的文件，如果某些文件已经被纳入了版本管理中，则修改`.gitignore`是无效的，解决方法是先把本地缓存删除（改成未track状态），然后再提交：

  ```git
  git rm -r --cached .
  git add .
  git commit -m 'xxx'
  ```

- Github上`.ignore`文件集合
  - [.gitignore](https://github.com/github/gitignore/)