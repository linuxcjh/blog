#Git 迁移项目 
@(Git)[GIT, Markdown, git]
>项目需要从原有低版本Gitlab本地服务器迁移到本地另外一台高版本的Gitlab服务器，倒腾了个把小时，做个记录方便以后用查阅

- 在目标Gitlab服务器上建立新仓库

- 添加新的远程仓库
```
$ git remote add originTarget  XXXXX.git
```
- 提交本地最新master分支（当然其它分支也可以）push到新的Gitlab仓库

```
$ git push originTarget "分支名"
```
- 移除之前的远程仓库
```
$ git remote remove origin
```
- 修改现有远程仓库名称
```
$ git remote rename originTarget origin
```
- 好了，现在本地代码已经关联到新的远程仓库



