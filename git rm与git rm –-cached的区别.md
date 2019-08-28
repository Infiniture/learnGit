### git rm与git rm –-cached的区别

- 当我们需要删除`暂存区`上的文件，并且工作区也不需要这个文件，可以使用

    ```git
    git rm file_path
    ```

- 当我们需要删除`暂存区`上的文件，但本地又需要使用，只是不希望这个文件被版本控制，可以使用

    ```git
    git rm --cached file_path
    ```

