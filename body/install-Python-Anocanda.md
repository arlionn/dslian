## 安装 VScode 
1. [下载 VScode](https://code.visualstudio.com/Download)（选择适合你操作系统的版本）。
2. 安装 VScode（双击下载的安装包，按照提示完成安装）。
3. 安装完成后，打开 VScode。
4. 在 VScode 中，你可以安装各种扩展来增强功能，比如 Python 扩展、Jupyter 扩展等。

## 安装 Anaconda
1. [下载 Anaconda](https://www.anaconda.com/products/distribution#download-section)（选择适合你操作系统的版本）。
2. 安装 Anaconda（双击下载的安装包，按照提示完成安装）。
3. 安装完成后，打开 Anaconda Navigator（在开始菜单或应用程序中找到它）。
4. 在 Anaconda Navigator 中，你可以创建和管理虚拟环境、安装包、启动 Jupyter Notebook 等。
5. 安装完成后，打开 Anaconda Prompt（命令行界面），输入以下命令检查安装是否成功：
   ```bash
   conda --version
   ```
   如果显示版本号，则表示安装成功。
6. 在 Anaconda Prompt 中输入以下命令更新 Conda 到最新版本：
   ```bash
   conda update conda
   ```
7. 创建一个新的虚拟环境（可选）：如果你想在一个独立的环境中工作，比如，你要同时使用 Python 3.8 和 Python 3.12，以便完成不同的项目，你可以创建一个新的虚拟环境。输入以下命令创建一个名为 `myenv38` 的虚拟环境，并安装 Python 3.8：
   ```bash
   conda create --name myenv38 python=3.8
   ```
   同理，如果你想使用 Python 3.12，你可以创建一个名为 `myenv312` 的虚拟环境，并安装 Python 3.12：
   ```bash
   conda create --name myenv312 python=3.12
   ```
   接下来，你可以激活特定的虚拟环境，比如 **myenv38**，输入以下命令：
   ```bash
   conda activate myenv38
   ```
   此时，若执行 `canda list` 命令，你会看到当前环境中安装的所有包和版本信息；而执行 `canda install Stargazer, v = 2.1.1`，则会在当前环境中安装 `Stargazer` 包的 2.1.1 版本。


## 建议安装的 VScode 扩展

- Python
- Jupyter
- Pylance
- Jupyter Keymap
- Jupyter Cell Tags
- Jupyter Notebook Renderers
- Jupyter Notebook Renderers (Preview)

备选扩展
- copolit
- GitHub Copilot Labs
- GitHub Copilot Chat
- 换一组



## 参考资料
- [Anaconda 官网](https://www.anaconda.com/)
- [Conda 官网](https://docs.conda.io/en/latest/)
- [Conda vs pip](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html#conda-vs-pip)
- [Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html)        
- [Conda Environment Management](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
- [Conda Package Management](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-pkgs.html)