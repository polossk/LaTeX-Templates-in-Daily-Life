# Paper Templates

*最后一次更新 2022-06-05*

小论文模板（paper）合集。小论文目前提供 Elsevier 和 Springer 两家出版社，其中 Springer 目前提供新老两个版本的模板（部分期刊需要老模板）。

## 内容说明

|              | 文档类型   | 官方模板来源                      | 本地最近更新 |
| ------------ | ---------- | --------------------------------- | ------------ |
| Elsevier     | elsarticle | [LaTeX Instructions][1]           | 2021-04-23   |
| Springer     | sn-jnl     | [LaTeX Author Support][2]         | 2022-06-05   |
| Springer-old | svjour3    | [Submission guidelines of JSC][3] | 2022-07-05   |

## 使用说明

* 每个出版社提供本地模板完整压缩包，**建议使用前自行更新模板**。
* 每种期刊应配套准备两个文件：一个是期刊投稿说明，即 `<ABBR>-<JOURNAL>.pdf`；另一个是期刊对应的 $\LaTeX$ 格式文档，即 `<ABBR>-<PUBLISHER>-Setting.tex`。
* 默认文件如下：
  * `artical-local.pdf`：编译好的小论文
  * `artical-local.tex`：小论文文档本体
  * `elsarticle.cls` 或 `sn-jnl.cls`：论文模板 `cls` 文件
  * `*.bst`：参考文献格式控制文件
  * `makefile`：make 编译控制
  * `math-symbols.tex`：数学符号插件 <github.com/polossk/Math-Symbols-in-LaTeX>
  * `reference.bib`：参考文献 bib 集合
  * `<ABBR>-<PUBLISHER>-Setting.tex`：格式文档

[1]: https://www.elsevier.com/authors/policies-and-guidelines/latex-instructions
[2]: https://www.springernature.com/kr/authors/campaigns/latex-author-support
[3]: https://media.springer.com/full/springer-instructions-for-authors-assets/zip/468198_LaTeX_DL_468198_240419.zip
