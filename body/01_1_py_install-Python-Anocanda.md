# Python：安装和环境配置

::: {.callout-important}
！**只需安装**：Anaconda + VScode。

- 直接使用 Anaconda 中的 Python 环境即可。
- 不要单独安装 Python 3.12 / 3.13。
:::


<br>

对于初学者来讲，建议安装 Anaconda 套装。它是一个开源的 Python 发行版，集成了 Python 解释器、包管理器 Conda 和许多常用的科学计算和数据分析库（如 NumPy、Pandas、Matplotlib 等）。

虽然 Anaconda 自带的编辑器 Jupyter Notebook 很好用，但如果你平时经常用 VScode 写东西，建议安装 [VScode](https://www.lianxh.cn/details/1174.html) 作为编辑器。VScode 支持多种编程语言，可以安装各种插件来增强功能。

> **参考安装教程：**

-   [Python运行环境之VSCode与Anaconda安装配置](https://blog.csdn.net/weixin_43679228/article/details/147256251)
-   [Anaconda + VS Code 的安装与使用](https://blog.csdn.net/m0_51976564/article/details/136141325)

下面是基于我的使用经验总结的安装步骤：

## 安装 Anaconda

对于多数用户，只需看 Step 1-4 即可。

1.  [下载 Anaconda](https://www.anaconda.com/products/distribution#download-section)（建议注册一个账号，若不注册，可以点击 **Skip**）。

2.  安装 Anaconda。**安装 Anaconda 最重要的事情：**

    -   **Select Installation Type** 页面，建议选择 **Just Me**，然后点击 **Next**。

    -   **Choose Install Location** 页面，建议使用默认路径 `C:\Users\用户名\Anaconda3` 作为 Anaconda 的安装路径，这样可以避免一些潜在的权限和路径问题。**然而，** 如果你的用户名中包含中文字符或空格，建议选择「自定义路径」，并选择一个英文路径，如 `C:\myProgram\Anaconda3`。

    -   **Advanced Installation Options** 页面，确保**同时勾选**如下两个选项：

        -   \[√\] `Add Anaconda to my PATH environment variable`
        -   \[√\] `Register Anaconda as my default Python 3.x`

        ![](https://fig-lianxh.oss-cn-shenzhen.aliyuncs.com/20250513210628.png)

    -   详情参见：[VSCode与Anaconda安装配置](https://blog.csdn.net/weixin_43679228/article/details/147256251)

3.  安装完成后，打开 Anaconda Navigator（在开始菜单或应用程序中找到它）。

4.  在 Anaconda Navigator 中，你可以创建和管理虚拟环境、安装包、启动 Jupyter Notebook 等。

5.  安装完成后，打开 Anaconda Prompt（命令行界面），输入以下命令检查安装是否成功：

    ``` bash
    conda --version
    ```

    如果显示版本号，则表示安装成功。

6.  在 Anaconda Prompt 中输入以下命令更新 Conda 到最新版本：

    ``` bash
    conda update conda
    ```

7.  创建一个新的虚拟环境（**可选**）：如果你想在一个独立的环境中工作，比如，你要同时使用 Python 3.8 和 Python 3.12，以便完成不同的项目，你可以创建一个新的虚拟环境。输入以下命令创建一个名为 `myenv38` 的虚拟环境，并安装 Python 3.8：

    ``` bash
    conda create --name myenv38 python=3.8
    ```

    同理，如果你想使用 Python 3.12，你可以创建一个名为 `myenv312` 的虚拟环境，并安装 Python 3.12：

    ``` bash
    conda create --name myenv312 python=3.12
    ```

    接下来，你可以激活特定的虚拟环境，比如 **myenv38**，输入以下命令：

    ``` bash
    conda activate myenv38
    ```

    此时，若执行 `canda list` 命令，你会看到当前环境中安装的所有包和版本信息；而执行 `canda install Stargazer, v = 2.1.1`，则会在当前环境中安装 `Stargazer` 包的 2.1.1 版本。

## 安装 VScode

1.  [下载 VScode](https://code.visualstudio.com/Download)（选择适合你操作系统的版本）。
2.  安装 VScode（双击下载的安装包，按照提示完成安装）。
3.  安装完成后，打开 VScode。
4.  在 VScode 中，你可以 [安装各种插件](https://www.lianxh.cn/details/1490.html) 来增强功能，比如 Python、Jupyter 等。

### 建议安装的 VScode 插件

如果你不了解 VScode，可以先读一下 [VScode编辑器](https://www.lianxh.cn/details/1174.html)。

有关插件的安装，参见：[VScode插件：安装、配置和使用](https://www.lianxh.cn/details/1490.html)

#### Python 插件

> [VScode：实用 Python 插件清单](https://www.lianxh.cn/details/1489.html)

-   Python
-   Jupyter
-   Pylance
-   Data Wrangler
-   GitHub Copilot (首月免费，后续每月 \$10.0，使用 Visa 或 Master 信用卡付款)
-   GitHub Copilot Chat
-   Cline (Copilot 的替代品，Free)

#### Markdown 插件

> [VScode：实用 Markdown 插件推荐](https://www.lianxh.cn/details/1390.html)

-   Markdown All in One
-   Markdown Preview Enhanced
-   Marp (制作[幻灯片](https://www.lianxh.cn/search.html?s=marp))



## 参考资料

-   [Anaconda 官网](https://www.anaconda.com/)
-   [Conda 官网](https://docs.conda.io/en/latest/)
-   [Conda vs pip](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html#conda-vs-pip)
-   [Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html)\
-   [Conda Environment Management](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
-   [Conda Package Management](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-pkgs.html)

## 相关推文

-   连享会, 2021, [司继春：Python学习建议和资源](https://www.lianxh.cn/details/563.html), 连享会 No.563.
-   连小白, 2025, [Python常用包盘点：经济与金融领域的必备工具包](https://www.lianxh.cn/details/1568.html), 连享会 No.1568.
-   连玉君, 2024, [从基础到 AI 助手：Python 用户最爱的 VScode 插件清单](https://www.lianxh.cn/details/1489.html), 连享会 No.1489.
-   王胜文, 2023, [VScode编辑器：常用快捷键-Markdown专题](https://www.lianxh.cn/details/1174.html), 连享会 No.1174.
-   初虹, 2022, [Markdown-LaTeX：经管人的VSCode配置大全](https://www.lianxh.cn/details/1004.html), 连享会 No.1004.
-   连玉君, 2024, [VScode：实用 Markdown 插件推荐](https://www.lianxh.cn/details/1390.html), 连享会 No.1390.
-   初虹, 2024, [让「记录」变得简单：Markdown使用详解](https://www.lianxh.cn/details/1456.html), 连享会 No.1456.
-   宋森安, 2021, [用Markdown制作幻灯片-五分钟学会Marp（上篇）](https://www.lianxh.cn/details/656.html), 连享会 No.656.
-   宋森安, 2021, [用Markdown制作幻灯片-五分钟学会Marp（下篇）](https://www.lianxh.cn/details/657.html), 连享会 No.657.
-   连玉君, 2022, [Marp幻灯片模板：用Markdown快速写幻灯片](https://www.lianxh.cn/details/1059.html), 连享会 No.1059.