# LaTeX Templates in Daily Life

*最后一次更新 2022-06-05*

日常 LaTeX 文稿模板合集，提供五种最常用的文稿模板，作业类模板（assignment），普通笔记类模板（note），代码打印模板（code），日常汇报幻灯片模板（presentation）和小论文模板（paper）。小论文目前提供 Elsevier 和 Springer 两家出版社。

## 内容说明

文稿的格式控制一般由后缀为 `setting.tex` 文档来集中管理与控制。这些模板的区别如下表所示。

|                  | 文档类型   | 格式控制                 | 字号控制                 |
| ---------------- | ---------- | ------------------------ | ------------------------ |
| Assignment       | article    | `article-setting.tex`    | 支持自定义字号           |
| Code             | article    | `code-setting.tex`       | 原生命令                 |
| Note             | article    | `note-setting.tex`       | 原生命令                 |
| Presentation     | beamer     | `beamer-setting.tex`     | 默认字号，支持自定义字号 |
| Paper (Elsevier) | elsarticle | `default-el-journal.tex` | 原生命令                 |
| Paper (Springer) | sn-jnl     | `default-sn-journal.tex` | 原生命令                 |
| Paper (Springer) | svjour3    | `default-sv-journal.tex` | 原生命令                 |

* 文档字体选用 Adobe Fonts。因为相比较于普通的自带的字体（宋体、黑体、仿宋、楷体），Adobe Fonts 更美观一些；
* `math-symbols.sty` 集成了大多数数学公式符号及数学公式库，可以将其放在项目本地，或者存入 `%texlive%\texmf-local\tex\latex\polossk` 当中，其中 `%texlive%` 是本地 `texlive` 的安装目录；
* `nwpuname.ttf` 是学校名称特殊字体，需要额外自行安装；
* 代码打印模板平均每页 61 行代码，且打印格式相对更清晰；
* Paper 建议在期刊要求下自行添加格式要求，本 repo 仅提供基础格式。

## 备注

提供两种代码渲染格式，需要放在 `setting.tex` 的“添加代码控制”部分。

* 文档中的代码多为整片整片出现
  * ![#E41A1C](https://dummyimage.com/15/E41A1C/png&text=+) `#E41A1C`
  * ![#377EB8](https://dummyimage.com/15/377EB8/png&text=+) `#377EB8`
  * ![#4DAF4A](https://dummyimage.com/15/4DAF4A/png&text=+) `#4DAF4A`
  * ![#984EA3](https://dummyimage.com/15/984EA3/png&text=+) `#984EA3`
  * ![#FF7F00](https://dummyimage.com/15/FF7F00/png&text=+) `#FF7F00`

<svg width="240" height="24">
<rect fill="#e41a1c" width="48" height="24" x="0"></rect>
<rect fill="#377eb8" width="48" height="24" x="48"></rect>
<rect fill="#4daf4a" width="48" height="24" x="96"></rect>
<rect fill="#984ea3" width="48" height="24" x="144"></rect>
<rect fill="#ff7f00" width="48" height="24" x="192"></rect>
</svg>

```tex
\usepackage{listings}
\lstset{
    basicstyle=\footnotesize\ttfamily,
    numbers=left,
    numberstyle=\tiny,
    numbersep=5pt,
    tabsize=4,
    extendedchars=true,
    breaklines=true,
    emph={as, np, self, shape, axis},
    emphstyle=\color[HTML]{984ea3}\bfseries,
    keywordstyle=\color[HTML]{377eb8}\bfseries,
    numberstyle=\color[HTML]{e41a1c},
    commentstyle=\color[HTML]{4daf4a}\bfseries,
    stringstyle=\color[HTML]{ff7f00}\ttfamily\bfseries,
    rulesepcolor=\color[HTML]{cccccc},
    showspaces=false,
    showtabs=false,
    frame=shadowbox,
    framexrightmargin=5pt,
    framexbottommargin=4pt,
    showstringspaces=false,
    escapeinside=`', % 逃逸字符(1左面的键)，用于显示中文
}
```

* 文档中的代码多为行间出现
  * ![#CCCCCC](https://dummyimage.com/15/CCCCCC/png&text=+) `#CCCCCC`
  * ![#B20000](https://dummyimage.com/15/B20000/000000?text=+) `#B20000`

<svg width="240" height="24">
<rect fill="#cccccc" width="48" height="24" x="0"></rect>
<rect fill="#b20000" width="48" height="24" x="48"></rect>
<rect fill="#cccccc" width="48" height="24" x="96"></rect>
<rect fill="#b20000" width="48" height="24" x="144"></rect>
<rect fill="#cccccc" width="48" height="24" x="192"></rect>
</svg>

```tex
\definecolor{lightgray}{HTML}{cccccc} % \colorlet{lightgray}{gray!40}
\definecolor{darkred}{HTML}{b20000} % \colorlet{darkred}{red!70!black}
\usepackage{listings}
\lstset{
    basicstyle=\color{darkred}\normalsize\ttfamily,
    backgroundcolor=\color{lightgray},
    breaklines=true,
}
```
