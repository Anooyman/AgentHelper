# 学习教程
https://github.com/InternLM/Tutorial/blob/camp3/docs/L0/Python/task.md

# 实战营Linux基础课程学习笔记

## 1. InternStudio开发机介绍
- InternStudio: 云端算力平台，用于大模型微调，提供开发机环境。
- 访问: 通过 InternStudio官网 进入控制台。
- 功能:
  - 开发机管理: 创建、配置、查看日志。
  - 文件管理: 可视化界面，支持上传、下载、创建文件和查看隐藏文件。
  - 资源共享: 团队成员间共享算力资源。
  - SSH密钥配置: 安全访问开发机。
  - 个人信息和资源监控: 编辑信息和查看资源使用状态。

## 2. SSH及端口映射
- SSH: 加密协议，用于安全访问和文件传输。
  - 由服务器和客户端组成，通过TCP连接和密钥交换建立安全会话。
- 远程连接开发机:
  - 使用密码或SSH密钥登录。
  - 支持使用VSCode等工具进行SSH连接。
- 端口映射:
  - 将外网端口映射到内网端口，解决Web服务访问问题。
  - 使用SSH命令进行端口映射，如-L参数设置本地端口转发。

## 3. 文件管理
- 创建文件: touch filename 创建空文件。
- 创建目录: mkdir dirname 创建新目录。
- 目录切换: cd dirname 切换当前目录。
- 显示当前目录: pwd 打印工作目录的完整路径。
- 查看文件内容: cat filename 显示文件内容。
- 编辑文件: 使用vi或vim进入编辑模式。
- 复制文件/目录: cp [选项] 源文件 目标文件，-r递归复制目录。
- 创建链接: ln -s target linkname 创建软链接。
- 移动/重命名文件: mv oldname newname。
- 删除文件/目录: rm filename，-r递归删除目录。
- 查找文件: find [路径] [选项] 搜索文件系统。
- 列出目录内容: ls [选项]，-l显示详细信息。
- 文本处理: sed 用于执行脚本进行文本替换等操作。

## 4. 进程管理
- 查看进程: ps列出进程，top动态显示进程状态。
- 树状图显示进程: pstree。
- 查找进程: pgrep根据条件查找进程。
- 更改进程优先级: nice。
- 作业信息: jobs显示后台作业列表。
- 后台和前台切换: bg和fg。
- 杀死进程: kill发送信号到进程，-9强制杀死。

## 5. 工具使用
- TMUX: 终端复用器，允许多个会话共享一个窗口。
  - 安装: apt install tmux。
  - 使用: tmux启动，Ctrl+d退出。

## 6. Conda和Shell介绍
- Conda: 跨平台的包和环境管理器。
  - 设置: 配置镜像源，如清华源，加快下载速度。
  - 环境管理:
    - 创建: conda create -n envname python=version。
    - 激活: conda activate envname。
    - 退出: conda deactivate。
    - 删除: conda remove --name envname --all。
    - 导出/导入: conda env export > file.yml，conda env create -f file.yml。
- Shell脚本: 自动化命令执行，系统管理，批处理。

## 7. studio-conda使用
- 功能: 快速克隆预设Conda环境。
- 使用:
  - 列出环境: studio-conda env -l。
  - 克隆环境: studio-conda target-conda-name。

## 8. 常见问题
- 开发机环境重置:
  - SSH连接到开发机。
  - 删除/root目录下所有文件: rm -rf /root。
  - 重启开发机以重置环境。
  - 重新链接共享目录: ln -s /share /root/share。

## 任务截图：

### SSH 链接
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/InterLM_study_3/img/jietu.png)
### Linux 命令
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/InterLM_study_3/img/linux.png)
### 创建 conda 环境
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/InterLM_study_3/img/conda.png)
### 还原环境
![image](https://github.com/Anooyman/LLMStudyNote/blob/main/InterLM_study_3/img/reset.png)
