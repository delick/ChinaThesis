# 中国地质大学（北京）学位论文 LaTeX 模板框架

本项目是基于 latexstudio 的 ChinaThesis 项目更改而来的 LaTeX 学位论文模板，基本符合学校硕士论文格式的要求。（也可以更改成本科和博士论文模板，但没有校对格式）

## 学校论文指南和要求

1. **硕士学位论文**
- **学硕**：[中国地质大学（北京）学术学位硕士学位论文书写指南.doc](https://www.cugb.edu.cn/download.action?id=58&deptCode=20300)
- **专硕**：[中国地质大学（北京）专业学位硕士学位论文书写指南.doc](https://www.cugb.edu.cn/download.action?id=59&deptCode=20300)

2. **博士学位论文**
[中国地质大学（北京）博士学位论文书写指南.doc](https://www.cugb.edu.cn/download.action?id=57&deptCode=20300)

## 原模板说明

包括模板代码、注释、文档，示例论文，以及用于维护模板的持续集成和单元测试。
该框架针对国内高校 LaTeX 模板的普遍需求提供了指南，并尽可能使格式与内容分离，
旨在帮助编写高质量的中文模板，也可供已有模板进行参考。

主要特性：
- 支持跨平台使用，兼容最新的 TeX Live, MacTeX 和 MikTeX 发行版，
  并向后兼容到 2016 年的版本
- 不支持已经过时的 CTeX 套装
- 数学符号遵循国内的排版习惯
- 参考文献格式符合 GB/T 7714
- 单元测试（l3build）
- 持续集成（travis-ci）



## 使用模板

模板的源代码代码位于 `chinathesis.dtx` 文件中，
编译模板的使用说明文档 `chinathesis.pdf`：
```
latexmk -xelatex chinathesis.dtx
```

编译论文 `main.pdf`：
```
latexmk -xelatex main.tex
```

清理论文编译过程中的临时文件：
```
latexmk -c main.tex
```

以上编译过程也可以用 `make` 工具：
```
make doc        # 编译生成 chinathesis.pdf
make            # 编译生成论文 main.pdf
make clean      # 删除编译过程中生成的临时文件
```
