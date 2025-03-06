# 📝 武汉理工大学实验报告LaTeX模板

这是一个用于创建武汉理工大学实验报告的 LaTeX 模板，提供标准的封面页、内容格式及排版风格，完全符合学校实验报告规范要求。

## ✨ 特点

- 标准的实验报告格式，包含封面、**内容页**
- 预定义格式化命令，简化排版
- 支持算法、代码、表格等学术元素
- 打印模式，优化纸质输出效果
- 易于定制的个人和课程信息

## 🚀 使用方法

1. 复制整个模板文件夹
2. 安装必要的字体（见[字体要求](#-字体要求)）
3. 修改 `settings.tex` 中的个人信息和报告信息
4. 编辑 `content.tex` 文件，添加报告内容
5. 使用 **XeLaTeX** 编译 `template.tex` 文件（**注意：必须使用 XeLaTeX 而非 pdfLaTeX**）

## 📥 下载模板

您可以通过以下几种方式获取模板：

### 方式一：使用 git 克隆

如果您安装了 git，可以使用以下命令克隆仓库：

```bash
git clone https://github.com/rinki-s/whut-latex-report-template.git
```

### 方式二：直接下载 ZIP 包

1. 访问 [GitHub 仓库页面](https://github.com/rinki-s/whut-latex-report-template)
2. 点击页面上的绿色 "Code" 按钮
3. 在弹出菜单中选择 "Download ZIP"
4. 下载完成后，解压缩文件到您的工作目录

## 📦 文件结构

- `template.tex`：主模板文件，控制整体结构
- `settings.tex`：个人和实验课程信息设置
- `styles.tex`：样式和格式定义（字体、间距等）
- `content.tex`：实验报告内容（替换此文件）
- `res/`：资源文件夹（图片等）

## ⚙️ 必填配置项（settings.tex）

在 `settings.tex` 中配置以下个人和课程信息：

```latex
\newcommand{\studentid}{1xxxxxxxxx}            % 学号
\newcommand{\coursename}{示例实验课程名称}      % 课程名称
\newcommand{\department}{示例开课学院}          % 开课学院
\newcommand{\teachername}{示例指导教师姓名}     % 指导教师
\newcommand{\studentname}{韩梅梅}              % 学生姓名
\newcommand{\studentclass}{示例专业班级}        % 专业班级
\newcommand{\academicyearstart}{2024}         % 学年开始
\newcommand{\academicyearend}{2025}           % 学年结束
\newcommand{\semester}{2}                      % 学期
\newcommand{\experimentname}{示例实验项目名称}  % 实验项目名称
\newcommand{\completedate}{2025年2月31日}      % 完成日期
```

## 🔤 字体要求

本模板需要以下字体才能正确编译：

- **基础字体**
  - **思源宋体 CN (Source Han Serif CN)**：中文正文主要字体
  - **思源黑体 CN (Source Han Sans CN)**：中文标题和强调文本
  - **Times New Roman**：英文正文字体
  
- **代码与特殊字体**
  - **更纱黑体 (Sarasa Mono SC)**：等宽中文字体，用于代码显示
  - **Courier Prime**：英文等宽字体，用于代码块

> **💡 提示**：模板默认使用思源系列字体，这些是开源字体，提供了优秀的排版效果。如果需要与学校官方文档更接近的外观，可以考虑修改为 SimHei 和 SimSong（即 Windows 自带黑体和宋体），修改后请到 `styles.tex` 中取消注释 `\usepackage[BoldFont, SlantFont]{xeCJK}`。

### 字体安装指南

1. **Windows 用户**:
   - [思源宋体](https://github.com/adobe-fonts/source-han-serif/releases)：下载后右键安装
   - [思源黑体](https://github.com/adobe-fonts/source-han-sans/releases)：下载后右键安装
   - [更纱黑体](https://github.com/be5invis/Sarasa-Gothic/releases)：下载后右键安装

2. **macOS 用户**:
   - **使用 Homebrew 安装**（推荐）：
     ```bash
     brew install --cask font-source-han-serif
     brew install --cask font-source-han-sans
     brew install --cask font-sarasa-gothic
     ```
   
   - **手动安装**:
     - 思源宋体：[下载](https://github.com/adobe-fonts/source-han-serif/releases) OTC 版本，解压后双击字体文件，点击"安装字体"
     - 思源黑体：[下载](https://github.com/adobe-fonts/source-han-sans/releases) OTC 版本，解压后双击字体文件，点击"安装字体"
     - 更纱黑体：[下载](https://github.com/be5invis/Sarasa-Gothic/releases) ttc 文件，双击打开后点击"安装"
     - 或将下载的字体文件拖放到 Font Book 应用程序中
   
   - **验证安装**：打开"字体册"应用，搜索安装的字体确认是否成功

3. **Linux 用户**:
   - 使用系统包管理器安装相应字体
   - 或手动下载字体文件放入 `~/.fonts` 目录

### 修改字体配置

如果您想更换字体或系统中没有默认字体，可以修改 `styles.tex` 中的字体设置：

```latex
% 字体设置
\setCJKmainfont{思源宋体 CN}      % 中文正文字体，可改为：宋体-简、STSong、华文宋体等
\setCJKsansfont{思源黑体 CN}      % 中文无衬线字体，可改为：黑体-简、STHeiti、华文黑体等
\setCJKmonofont{Sarasa Mono SC}  % 中文等宽字体，可改为 Noto Sans Mono CJK SC
\setmainfont{Times New Roman}    % 英文衬线字体
\setsansfont{思源黑体 CN}         % 英文无衬线字体，可用 Arial、Helvetica 等替代
\setmonofont{Courier Prime}      % 英文等宽字体，可用 Courier New、Consolas 等替代
```

## 📚 常用命令

### 标题结构

- `\hone{标题}`：第一级标题（"第X部分：标题"）
- `\htwo{标题}`：第二级标题（"X、标题"） 
- `\hthree{标题}`：第三级标题（"X. 标题"）
- `\hfour{标题}`：第四级标题（"(X) 标题"）
- `\blankline`：插入空行

### 图片插入

```latex
\includegraphics[width=0.7\textwidth]{res/example-image.png}
\captionof{figure}{图片说明}
```

### 表格创建

```latex
% 普通表格
\begin{tabular}{|c|c|c|}
    \hline
    列1 & 列2 & 列3 \\
    \hline
    数据1 & 数据2 & 数据3 \\
    \hline
\end{tabular}
\captionof{table}{表格说明}


% 推荐：使用 tabularray 创建更美观的表格
\noindent\begin{tblr}{
    width=\linewidth,  % 表格宽度为页宽
    colspec={|X[c]|X[c]|X[c]|},  % 等宽居中列
    hlines  % 水平线
}
    表头1 & 表头2 & 表头3 \\
    数据1 & 数据2 & 数据3 \\
\end{tblr}
```

> **⚠️ 注意**：当表格宽度设为 `\linewidth` 时，**必须**在表格前添加 `\noindent` 避免缩进导致表格溢出页面边距。

### 代码块

```latex
\begin{lstlisting}[language=Python, caption=示例代码]
def hello_world():
    print("Hello, world!")
    
hello_world()
\end{lstlisting}
```

### 算法描述

```latex
\begin{algorithm}[H]
    \SetAlgoLined
    \caption{示例算法}
    \KwIn{输入参数}
    \KwOut{输出结果}
    
    初始化步骤\;
    \While{条件满足}{
        执行循环体\;
    }
    \Return{结果}\;
\end{algorithm}
```

### 公式编写

```latex
% 行内公式
这是一个行内公式 $E=mc^2$

% 行间公式
\begin{equation}
    F = G\frac{m_1 m_2}{r^2}
    \label{eq:gravity}
\end{equation}
```

## 🖨️ 打印模式

在 `settings.tex` 中取消注释 `\enableprintmode` 行以启用打印模式：

```latex
\enableprintmode  % 启用打印模式
```

启用后会自动添加空白页，优化双面打印时的页面布局。

## 📄 编译方法

```bash
# 使用 XeLaTeX 编译（必须）
xelatex template.tex

# 如果有参考文献，使用以下完整流程
xelatex template.tex
bibtex template
xelatex template.tex
xelatex template.tex
```

> **⚠️ 重要**：本模板必须使用 **XeLaTeX** 而非 pdfLaTeX，以确保中文字体和特殊格式正确渲染。

## ❓ 常见问题

- **Q: 编译出错怎么办？**  
  A: 确保使用 **XeLaTeX** 而非 pdfLaTeX 编译，并检查 LaTeX 错误日志，确保安装了所有必要的包（ctex, tabularray, algorithm2e, tcolorbox 等）。

- **Q: 如何修改字体？**  
  A: 在 `styles.tex` 中修改 `\setCJKmainfont`、`\setmainfont` 等字体设置。如需更接近学校官方模板，建议使用华文宋体和华文黑体。

- **Q: 编译时提示缺少字体怎么办？**  
  A: 下载并安装相应的字体，或修改 `styles.tex` 中的字体设置为您系统上已有的字体。

- **Q: 封面校徽图片在哪里？**  
  A: 位于 `res/image.png`。

- **Q: 表格显示不正确或超出页面边距？**  
  A: 确保使用 `\noindent` 开始表格环境，特别是当表格宽度设置为 `\linewidth` 时。

## 📝 贡献

欢迎提交问题和改进建议！如发现 bug 或有新功能需求，请提交 issue。

## 📜 许可证

该模板基于 [MIT 许可证](LICENSE) 开源。