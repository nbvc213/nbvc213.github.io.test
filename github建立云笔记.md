#### GitHub建立云笔记

一般来说，本地仓库的建立通过克隆的方式完成，即克隆GitHub仓库到本地仓库。参数 `-b` 用来指定分支 `main`。

```
git clone -b main git@github.com:username/repository.git
```

> [!WARNING]
>
> 如果不使用上述方式建立本地仓库，之后将本地仓库同步到GitHub时会拒绝合并。
>
> ```
> fatal: refusing to merge unrelated histories
> ```

#### 上传本地仓库到GitHub仓库

打开命令提示符，使用`cd`命令跳转到本地仓库的目录下（该目录下有 `.git` 文件夹）。

使用如下命令，将当前目录下的文件提交（commit）到暂存区。

```
git add <file>	//添加单个文件到暂存区。
git add .		//添加当前目录下的所有文件到暂存区。
git add --help	//查看git add命令的所有可用参数
```

使用如下命令，提交暂存区的所有更改到本地仓库。`first commit` 为提交内容的描述，可以随意填写。

```
git commit -m "first commit"
```

添加名为 `origin` 的远程仓库，远程仓库的URL地址可以自行设置，这里是 `git@github.com:nbvc213/Notes.git`。

```
git remote add origin git@github.com:nbvc213/Notes.git
```

将本地仓库的 `main` 分支推送到远程仓库 `origin` 中的 `main` 分支。

```
git push origin main
```

