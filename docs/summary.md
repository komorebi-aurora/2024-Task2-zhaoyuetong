##### Git 命令:

   1.git clone：用于从远程仓库将项目代码克隆到本地,方便在本地进行开发和管理。

2. git add ：将当前目录下所有未被追踪的新文件以及已修改但未暂存的文件添加到暂存区。
3. git commit -m ："提交信息"：把暂存区的文件变更提交到本地仓库，-m 选项用于添加提交说明，方便记录和追溯变更内容。
4. git push origin main：将本地仓库中指定分支的提交推送到远程仓库
5. git branch dev：创建一个名为 dev 的新分支，不切换分支。
6. git checkout dev：切换到名为 dev 的分支进行开发。
7. git merge feature-plot：将 feature-plot 分支合并到当前所在分支，实现功能分支代码的整合。

##### Conda 命令：

1. conda create -n plot_env python=3.8：创建一个名为 plot_env 的虚拟环境，并指定 Python 版本 为 3.8。虚拟环境可实现不同项目的环境隔离，避免依赖冲突。
2. conda activate plot_env：激活名为 plot_env 的虚拟环境，激活后执行的包安装等操作都在该虚拟环	境内进行。
3. conda env export > environment.yml：将当前虚拟环境的依赖信息导出到 environment.yml 文件	中，方便在其他环境中快速配置相同的依赖。

##### Anaconda 环境配置的优点与难点：

- 优点

  1. 环境隔离：可以为不同项目创建独立的虚拟环境，每个环境拥有各自的 Python 版本和包依赖，避免了不同项目间依赖冲突的问题。

  2. 跨平台支持：在 Windows、Linux、macOS 等主流操作系统上均可使用，方便不同系统的开发者进行项目开发。

- 难点

   安装与配置复杂：初次安装 Anaconda 时，可能会遇到环境变量配置等问题，对于新手不太友好。如果配置不当，可能导致命令无法正常执行。

##### Git 分支管理中的经验

1. 明确分支用途：创建不同分支用于不同目的，如 dev 分支用于日常开发，功能分支，用于开发特定功能。这样可以使开发过程更加清晰，便于团队协作和代码管理。

2. 及时合并分支：功能开发完成后，应及时将功能分支合并到主开发分支，避免分支长期存在导致合并时冲突过多难以解决。同时在合并前要确保功能分支代码经过充分测试。

3. 解决冲突技巧：合并分支时遇到冲突是常见情况，要学会查看冲突提示，手动编辑文件解决冲突部分，然后再提交合并。

##### 部署过程中遇到的问题及解决方案

- **问题**：在使用 git push推送代码到 GitHub 时，出现 “`fatal: unable to access 'https://github.com/...': Failed to connect to github.com port 443 after...`” 错误，无法连接到服务器。

- **解决方案**：首先检查网络连接，确认网络正常后，排查代理设置问题，若网络受限制，设置正确的代理；若使用 HTTPS 协议推送，检查认证信息是否正确，必要时重新输入账号密码；还可尝试切换为 SSH 协议推送，重新配置 SSH 密钥并关联到 GitHub 账户，最终解决了推送问题。

  ##### 更新 README.md:

  1. 项目简介：简要介绍项目的功能和用途，例如 “本项目是一个基于 Python 的绘图项目，通过运行 `Plot.py` 程序生成特定图像，用于展示数据可视化相关功能。”

  2. 文件说明：说明项目中主要文件和文件夹的作用，如 `src/` 文件夹存放项目的源代码，`images/` 文件夹用于保存生成的图像，`Plot.py` 是主程序文件，负责生成图像等。

  3. 部署步骤：详细列出部署项目的步骤，如 “1. 克隆项目仓库到本地：`git clone https://github.com/komorebi-aurora/2024-Task2-zhaoyuetong.git；2. 创建并激活 Anaconda 虚拟环境：`conda create -n plot_env python=3.8` ，`conda activate plot_env` ；3. 安装项目依赖：`pip install -r requirements.txt` ；4. 运行程序生成图像：`python Plot.py。”

  ##### 推送更改到 GitHub

  1. git add .：将所有变更添加到暂存区。

  2. git commit -m "提交总结文档并更新README"：提交暂存区的变更到本地仓库。

  3. git push origin main：将本地仓库的变更推送到远程 GitHub 仓库。