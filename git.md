## IDEA配置VC之Git

## 下载Git

官网: [https://git-scm.com/](https://git-scm.com/)，下载并安装

## 配置Idea的Git设置

来到IDEA配置的 Version Control -\&gt;GitHub 页面，登录自己的GitHub帐号，然后回到 Version Control -\&gt;Git ，配置Git可执行文件的目录，在Git安装目录的cmd文件夹内，选择git.exe，确定，再点击TEST,成功的话会弹出Git的版本号。

## 配置Git

打开Git安装目录内的git-bash.exe

 [![](/img/git1.png)]

输入命令:

$ cd ~  #保证当前路径在&quot;~&quot;下

$ ssh-keygen -t rsa -C &quot;xxxxxx@yy.com&quot;  #建议填写自己真实有效的邮箱地址 生成密钥

生成成功的密钥在~/.ssh/目录内，默认id\_rsa

添加ssh key到GitHub

1.登录GitHub账号；点击右上角账号头像的&quot;▼&quot;→Settings→SSH kyes→Add SSH key。

2.复制id\_rsa.pub的公钥内容。

3.进入c:/Users/xxxx\_000/.ssh/目录下，打开id\_rsa.pub文件，全选复制公钥内容。

4.Title自定义，将公钥粘贴到GitHub中Add an SSH key的key输入框，最后&quot;Add Key&quot;。

配置账户

$ git config --global user.name &quot;your\_username&quot;  #设置用户名

$ git config --global user.email &quot;your\_registered\_github\_Email&quot;  #设置邮箱地址(建议用注册giuhub的邮箱)

测试ssh keys是否设置成功。

$ ssh -T [git@github.com](mailto:git@github.com)

提示输入yes连接

**Hi xxx! You&#39;ve successfully authenticated, but GitHub does not provide shell access**. #出现这句话，说明设置成功。

## 使用Git

然后自己去学习怎么使用Git吧
