## 如何下载并查看文件
1. 点击main，选择分支名字（eg. master) 获取此分支下的所有文件。
2. 点击code点击download Zip 则可以下载整个分支下的文件。

## 如何上传或直接编写文件
#### 上传
1. 选择你要上传的分支。
2. 点击Addfile 点击upload file 或者直接进行拖拽 点击commit。
3. 此方法一次上传的文件不能超过25M。
<img width="960" alt="图片" src="https://user-images.githubusercontent.com/73382919/122737459-a12d1f80-d2b3-11eb-9899-a17e56724cc5.png">



#### 直接编写
1. 在“Name your file”起名字地方，若新建文件夹，则输入文件夹名加‘/’，例如：test/
2. 书写内容，提交
<img width="785" alt="图片" src="https://user-images.githubusercontent.com/73382919/122737586-c588fc00-d2b3-11eb-8705-d9c6ad4918cd.png">


## 如何参与编辑
1. 注册GitHub账号，将账号名发给我。
2. 拉你进入这个项目，作为开发者身份，以后登陆自己的账号就可以编辑更改内容。

## MAC 如何通过终端上传到GitHub (可适用于传多个大文件）
### 1. 打开终端下载git
```
brew install git
```
或者直接搜索在此处下载 https://git-scm.com/downloads  
下载之后在终端输入
```
git version
```
若显示 git version 2.29.0 类似则下载成功

### 2.创建.ssh 文件
#### 配置SSH keys:
```
mkdir .ssh
cd .ssh
ssh-Keygen -t rsa -C "你注册gitHub的邮箱“
```
输入完成之后中间会提示你输入密码，不用管，继续敲回车，直到出现类似的图表。  
The key fingerprint is:  
5a:39:fa    
+--[RSA 2048]----+  
|                |  
| E·             |  
| o...o .        |  
|                |  
+----------------+  

输入指令
```
ls -la
```
如果出现类似这样的指令代表配置成功  
total 16  
drwxr 4   staff 136 1 16 18:31  
drwxr-xr-x+ 25  staff 840 1 16 18:31  
-rw---------1   staff 1679 1 16 18:31 id_rsa  
-rw-r--r-- 1  staff 396 1 16 18:31 id_rsa.pub  

输入指令   
```
pbcopy < ~/.ssh/id_rsa.pub
```

### 3.添加sshkey
 1. 点击右上角头像登陆GitHub，弹出列表选择“Settings”，然后选择"SSH and GPG keys"
 2. 点击New SSH Key, 输入Title（可以叫自己的邮箱), 粘贴自己刚刚通过指令获得的SSH Keys, 点击添加SSH Keys

### 4.通过终端上传文件
```
mkdir git                     //这里新建了一个文件夹，我的文件夹名字叫git

cd git                        //打开这个文件夹

git init                      //建立仓库

git remote add origin "你库的链接“         // 此处库的链接为: https://github.com/Kang-jingtong/BUTMA.git

git add .                     //把你要上传的内容放到新建的git文件夹里，add .会把此文件夹上的全部文件添加到代上传的列表

git commit -m "这里写上提交的注释"             //提交

git push -u origin master                 //第一次提交：写完这部刷新界面可以在git上看到，这里新建了一个叫master的分支。所有的内容都现在在分支里

git push                    //以后提交：直接git push
```
<img width="936" alt="图片" src="https://user-images.githubusercontent.com/73382919/122736720-e6048680-d2b2-11eb-87e4-abb5d06dbee5.png">


### 5.通过终端创建分支并上传文件
重复第4部操作
```
git checkout -b “分支名”                     //创建本地分支
git branch                                  //查看当前所处分支，颜色为绿色的是当前的分支
git push origin “分支名”                     //将分支及其分支内的内容上传到远端仓库
```

