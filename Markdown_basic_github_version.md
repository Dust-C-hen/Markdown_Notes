<!-- #的个数表示标题的级别 -->
<!-- 注释的快捷键是Ctrl+/ -->
<!-- 自动格式化的快捷键是Shift+Alt+F，仅对表格排版有效 -->

# Markdown 常用语法综合指南

> 这是一个引言区块。Markdown 是一种轻量级标记语言，它允许人们使用易读易写的纯文本格式编写文档。

---

<!-- 生成目录 github不支持TOC语法 需要手动写目录-->
<!-- 但是目录只要列出大部分标题后，vscode会自动补全，应该是插件在起作用 -->
## 目录
- [Markdown 常用语法综合指南](#markdown-常用语法综合指南)
  - [目录](#目录)
  - [基本快捷键/操作](#基本快捷键操作)
  - [文本样式 (Text Styling)](#文本样式-text-styling)
  - [列表 (Lists)](#列表-lists)
    - [无序列表](#无序列表)
    - [有序列表](#有序列表)
    - [任务列表 (Task Lists)](#任务列表-task-lists)
  - [代码 (Code)](#代码-code)
    - [行内代码](#行内代码)
    - [代码块 (Code Blocks)](#代码块-code-blocks)
  - [引用块 (Blockquotes)](#引用块-blockquotes)
  - [表格](#表格)
  - [数学公式 (LaTeX)](#数学公式-latex)
  - [链接与多媒体 (Links \& Media)](#链接与多媒体-links--media)
    - [基本链接](#基本链接)
    - [自动识别URL](#自动识别url)
    - [锚点链接](#锚点链接)
    - [邮件链接](#邮件链接)
  - [高级图表 (Mermaid)](#高级图表-mermaid)
  - [提示块与折叠 (HTML Tricks)](#提示块与折叠-html-tricks)
  - [脚注](#脚注)
  - [图片](#图片)

---

## 基本快捷键/操作
*注：以下快捷键主要适用于 VS Code + Markdown Preview Enhanced 插件，GitHub 网页端不可用。*

注释的快捷键是`Ctrl+/`

自动格式化的快捷键是`Shift+Alt+F`，仅对表格排版有效

预览`Ctrl+K+V`或点击右上角图标

导出pdf：直接在预览界面右键，`Open in Blowser`，然后在浏览器里`Ctrl+P`打印。

需要信任当前文件夹才能正常预览和编辑

---
## 文本样式 (Text Styling)

说明，github一定要加空行换行，否则会连在一起

**这是加粗文本** (Bold)

_这是斜体文本_ (Italic)

**_这是加粗斜体文本_** (Bold Italic)

~~这是删除线文本~~ (Strikethrough)

<mark>这是高亮文本</mark> (GitHub 支持 HTML 标签)

---

## 列表 (Lists)

### 无序列表

- 项目 A
- 项目 B
- 子项目 B-1 (使用缩进)
  - 子项目 B-2

* 也可以使用减号
  - 子项目

- 或者加号
  - 子项目

### 有序列表

1. 第一项
2. 第二项
3. 第三项
   1. 嵌套的有序列表

### 任务列表 (Task Lists)

- [x] 已完成的任务
- [ ] 未完成的任务
- [ ] 待办事项 C

---


## 代码 (Code)

### 行内代码

在文本中插入 `console.log('Hello World')` 这样的短代码。

### 代码块 (Code Blocks)

指定语言可实现语法高亮（例如：python, c, javascript, bash）：

```python
def hello():
    print("Hello, Markdown!")

hello()
```

```c++
#include <iostream>
int main() {
    std::cout << "这是 C++ 代码" << std::endl;
    return 0;
}
```

---

## 引用块 (Blockquotes)
> 这是一个普通引用。
>
> > **嵌套引用**：这是引用中的引用。
> > 它可以包含代码块：
> > ```cpp
> > int a = 10;
> > ```

## 表格
github渲染想让图表居中比较麻烦，此处省略。

| 插件名称                      | 推荐理由                                            |
| :---------------------------- | :-------------------------------------------------- |
| **Markdown All in One**       | 基础增强：自动目录、快捷键、列表补全。              |
| **Markdown Preview Enhanced** | 渲染核心：支持 LaTeX 公式、Mermaid 图表、导出 PDF。 |



<!-- 通过html代码加标题 -->
<p align="left"><font face="黑体" size=4.>表1 示例表格</font></p> 

| 姓名  |  职业  |  技能 |
| :---: | :----: | ----: |
| 艾伦  | 程序员 |   C++ |
| 莎拉  | 设计师 | Figma |

(注：冒号决定对齐方式，左边是左对齐，两边是居中，右边是右对齐)

---

## 数学公式 (LaTeX)
Markdown 完美支持 LaTeX 数学公式，适合理工科笔记。
行内公式：质能方程是 $E = mc^2$。
独立公式块(github里必须严格按照下述写法换行)：
$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$

麦克斯韦方程组 (微分形式)：
$$
\begin{cases}
\nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0} \\
\nabla \cdot \mathbf{B} = 0 \\
\nabla \times \mathbf{E} = -\frac{\partial \mathbf{B}}{\partial t} \\
\nabla \times \mathbf{B} = \mu_0\mathbf{J} + \mu_0\varepsilon_0\frac{\partial \mathbf{E}}{\partial t}
\end{cases}$$矩阵示例：$$A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}
$$

---

## 链接与多媒体 (Links & Media)
### 基本链接
Markdown中，链接的基本格式为：`[链接文本](链接地址 "可选标题")`
[百度](https://www.baidu.com "百度一下，你就知道")

### 自动识别URL
直接输入URL或用尖括号包裹，Markdown会自动将其转换为超链接。
<www.google.com>

### 锚点链接

用于文档内跳转：

[跳转到标题](#表格)
[跳转到本文开头](#title-markdown-常用语法综合指南)

### 邮件链接

Markdown支持创建邮件超链接：
[发送邮件](mailto:example@email.com)

---

## 高级图表 (Mermaid)
需要 Markdown Preview Enhanced 插件支持，github端暂时不支持，此处略去。

---

## 提示块与折叠 (HTML Tricks)
引用提示：
注意： 这里的配置对 Windows 和 Mac 都通用。
支持嵌套引用。
折叠详情 (适合做答案解析):

<details> <summary><b>点击查看 C++ 虚析构函数的作用</b></summary>
当通过基类指针删除派生类对象时，如果基类析构函数不是虚函数，则不会调用派生类的析构函数，可能导致内存泄漏。 </details>

---

## 脚注
Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

---

## 图片
可以直接复制图片，然后粘贴在这里
![alt text](image.png)

这种方法会根据页面大小自动调整图片排列，并设置图片居中和大小
<p align = "center">    
<img  src="image.png" width="400" />
<img  src="image.png" width="400" />
<img  src="image.png" width="400" />
<img  src="image.png" width="400" />
</p>

<p align = "center">    
<img  src="image.png" width="400" />
</p>


