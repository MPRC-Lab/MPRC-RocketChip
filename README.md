# MPRC-RocketChip
## 协作开发参考流程
### 步骤一: 注册并fork仓库
注册github账号，访问[中央仓库](https://github.com/MPRC-Lab/MPRC-RocketChip)，点击右上角的**fork**按钮(如下图所示)，将中央项目fork到自己的账户下，随后参与项目的同学的绝大多数开发工作都是在自己的仓库中完成的。  
![](http://chuquan-public-r-001.oss-cn-shanghai.aliyuncs.com/github-images/github001.png)  

### 步骤二: 初始化本地仓库
```mkdir [yourprojectdir]```  
```git init```  
```git clone [your-forked-repo-url].git```  

### 步骤三: 本地仓库开发管理
常用命令: 
```
// 跟踪文件
git add [filename|*]
```
```
// 提交至本地仓库
git commit -m "you-commit-message"
```
```
// 查看当前状态
git status
```
```
// 查看提交日志
git log
```
更多命令请自行查阅。  
### 步骤四: 同步远程仓库并向中央仓库发起pull request
当自己负责的部分开发完成时，可以将其合并到中央仓库时。此时，请先将自己的代码与中央仓库的master分支进行合并。
```
// 先给自己的仓库添加远程分支，注意本步骤与初始化过程类似，整个项目周期只需执行一次即可
git remote add mprc https://github.com/MPRC-Lab/MPRC-RocketChip.git
```  
```
// 合并分支
git pull mprc master
```  
如有冲突，请自行解决。通常情况下，**不去修改他人创建的文件**或者**自己创建的文件不与中央仓库中已有文件同名**，是不会产生冲突的。  
```
// 推送至自己的远程仓库
git push -u origin master
```  
最后就是向项目维护者发出pull request的合并请求。进入自己项目仓库，选择**pull request**（如下图所示），然后自行创建新的pull request，并填写相关信息，请尽可能详细地描述自己本次合并所做的工作。  
![](http://chuquan-public-r-001.oss-cn-shanghai.aliyuncs.com/github-images/github002.png) 
