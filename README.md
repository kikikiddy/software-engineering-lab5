# 软件工程实验五：Git 协作与标签

本仓库基于本地计算器项目，保留此前提交历史。main.c 实现加减法，collaboration.c 用于冲突实验。

## 实验方式

由同一名操作者使用两个本地克隆副本 A、B 模拟两个开发工作区，两者使用相同真实账号。
本次没有其他同学实际参与；提交记录不代表多人参与。冲突、合并与远程推送均真实执行。

## 编译运行（PowerShell）

```powershell
gcc -std=c11 -Wall -Wextra -Werror main.c -o calculator.exe
.\calculator.exe
gcc -std=c11 -Wall -Wextra -Werror collaboration.c -o collaboration.exe
.\collaboration.exe
```

## 实验步骤

1. 将本地项目推送到本仓库，从远程克隆第二个工作区。
2. A、B 从同一基线修改 collaboration.c 的同一行；A 先推送，B 推送被拒绝。
3. B 获取并合并远程 main，实际产生内容冲突；保留 A、B 两项输出，清除冲突标记，编译验证后提交、推送。
4. A 拉取合并结果，验证两个工作区与远程 main 一致。
5. 创建附注标签 v1.0-lab5 与临时标签 lab5-temp，推送并查看；删除本地和远程临时标签，保留 v1.0-lab5。

## 后续同学如何参与

公开仓库可直接克隆。若要直接推送，需由仓库所有者在 GitHub 设置中邀请为协作者，接受邀请后再推送自己的功能分支。
也可以 Fork 后通过 Pull Request 提交修改。请先拉取最新代码，避免覆盖其他人的修改。
实验原始记录与报告配图保存在操作者本机，未上传个人实验报告。
