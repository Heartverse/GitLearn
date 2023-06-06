# Git

---

[git 简明指南 (runoob.com)](https://www.runoob.com/manual/git-guide/)

Git 是一个开源的分布式版本控制系统(VCS Version Control System)

## Git配置

```bash
git config --global user.name "xxxx"
git config --global user.email "xxxxx"
```

## init

创建一个名为 .git 的新子目录（Windows 下该目录为隐藏的），其中包含所有必需的存储库文件（Git 存储库框架）。

```bash
git init
```

![Untitled](Git%201f06304d59d04bac8b585c290ba761f1/Untitled.png)

## add

## commit

```bash
# 如果这样输入
git commit
# 会进入vim编辑器
# 按i或a进行编辑
# 输入完之后 按Esc退出编辑
# 输入:wq 保存退出

# 一般这样用

git commit -m "fix(test):change the content"
```

[Git Commit 规范与配置 - 掘金 (juejin.cn)](https://juejin.cn/post/7091276495972204580)

报错：

![Untitled](Git%201f06304d59d04bac8b585c290ba761f1/Untitled%201.png)

原因：本地git仓库目录下为空

其他原因：

add 后未 commit

init错误

```bash
git remote rm origin  #之前git上传地址报错，删除一下
git config --global -l #查看git当前设置
git config --global --unset http.proxy #取消代理
git remote add origin https://github.com/XXX #XXX自己的github项目地址
#git remote add origin https://github.com/limecho/JupyterLabPrograms.git
git push origin master #没有分支，直接上传master

git init 
git add file名
git commit -m 'description message'
git remote add origin xxx
git push origin master
```

![Untitled](Git%201f06304d59d04bac8b585c290ba761f1/Untitled%202.png)

```bash
xilinx@corespec:~/system/dashboards$ git status
On branch corespec2.5
Your branch is up to date with 'origin/corespec2.5'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        IRCPMG.py
        IRCPMG_TW_Preset.py
        Motor_control_CPMG.py
        Motor_control_CPMG_Por.py
        Motor_control_CPMG_bk.py
        Motor_control_Position.py
        Probe_Calibration.py
        SRCPMG.py
        SRCPMG_TW_Preset.py
        new_Motor_control_CPMG_Por.py

nothing added to commit but untracked files present (use "git add" to track)

```