# Github上传代码操作步骤

## github 上添加 SSH key

* 我们想往自己的GitHub账号上传项目,如果使用https url方式的话,需要每次都输入账号密码,会显得很繁琐,所以我们在一开始就配置好SSH key更为方便,这样每次上传的时候都不用输入账号密码了.

1. 本地生成秘钥,命令如下:
`$ ssh-keygen -t rsa -C "your_email@example.com"`

2. 这时候我们一般可以在~/.ssh目录下找到我们的私钥和公钥

3. id_rsa(私钥) id_rsa.pub(公钥)

4. `cat id_ras.pub` 查看公钥具体信息

5. 设置github上的公钥

6. 使用`ssh -T git@github.com`测试是否与远程仓库建立连接

## 添加仓库/推送/克隆

* 添加远程仓库
`git remote add origin git@github.com:仓库名称.git`

* 重命名分支名称
`git branch -M main`

* 推送分支(首次推送)
`git push -u origin main`

* 克隆仓库
`git clone git@github.com:仓库名称.git`
