---
title: "R语言入门学习笔记"
author: "欧阳继华"
date: "2023-07-21"
site: bookdown::bookdown_site
knit: bookdown::render_book
output: bookdown::bs4_book
documentclass: book
classoption: oneside
biblio-style: apa
bibliography: [references.bib]
link-citations: yes
# github-repo: perlatex/R4DS-book
# url: "https://bookdown.org/wangminjie/R4DS/"
#cover-image: images/cover.jpg
description: "这本书是作者本人用来记录R语言入门的学习笔记，为了方便运行R代码，首次尝试使用R语言提供的Rbookdown包来记录学习的过程"
---

<!-- 下面这个R语言代码块用于整个文档的渲染 -->



# 前言 {.unnumbered #Introduction}
大家好，这本书是一份**零基础系统性学习R语言**的学习笔记。
<img src="images/Rlogo.png" width="50%" height="75%" style="display: block; margin: auto;" />

## 写作目的 {.unnumbered #goal}
作者本人是一枚生物信息学专业入门小白，在平时的工作学习中经常需要使用计算机程序语言来分析和处理数据，因此需要寻找一种简洁高效的语法来记录学习的过程，在学习R语言的过程中发现R中的`rmarkdown`
语法很适合用来记录这种文中需要插入代码的笔记，因此最终选择了R中的`bookdown`
包来记录R语言的学习笔记。在创作这本书之前，本人学习R语言采用的是learn by doing,即“边做边学”或者“在做中学”的学习模式，需要用到什么功能就去网上直接google相关代码，然后复制粘贴，这种以实践为导向的学习方法的确能够快速解决学习者当前所面临的问题，但它的缺点也很明显：知其然而不知其所以然，不能够系统全面地从底层掌握R语言的使用技巧，遇到问题也不能又快又好地解决，因此我决定利用空闲时间系统化地学习R语言，为以后进一步实现R语言的高级应用打下坚实基础。

## 关于R {.unnumbered #about-R}
看到这本书人想必已经了解，至少听说过R语言是什么了（[R语言简介](https://www.r-project.org/about.html)），就我个人的理解，**R语言是一款带有强大可视化功能的统计学软件**，在科学研究的数据分析中具有极高的应用价值，因为几乎所有的自然科学的研究发展都离不开统计学，没有统计学支撑的分析结果是没有说服力的，而R语言最擅长的便是统计学，R的资源库，例如[R综合档案网络（CRAN）](https://cran.r-project.org/mirrors.html)中还包含了大量的适合各个专业领域分析的R包,并且能够快速方便地用代码生成出版级的高清图片，极大地提高了科学研究的效率，因此我建议无论是否是计算机相关专业的朋友，都可以学一点R语言，它绝对不会让你后悔。

## 关于本书 {.unnumbered #about-the-Book}
鉴于本人能力有限，没有过多的时间和精力去阅读国外大神写的R语言原著（见 [推荐书目](#recommend-books)），在学R的过程中使用的教材主要是四川师范大学物理学博士[王敏杰](https://github.com/perlatex)老师的《数据科学中的R语言》,以及北京大学数学科学学院副教授[李东风](https://www.math.pku.edu.cn/jsdw/js_20180628175159671361/l_20180628175159671361/69932.htm)老师的《R语言教程》,严格意义上来说属于二次创作，书中难免会出现理解不到位的地方，欢迎大家随时批评指正。

## 参考书目 {.unnumbered #reference-books}
- [《数据科学中的R语言》](https://bookdown.org/wangminjie/R4DS/)
- [《R语言教程》](https://www.math.pku.edu.cn/teachers/lidf/docs/Rbook/html/_Rbook/index.html)


## 推荐书目 {.unnumbered #recommend-books}
1. R for Data Science: Import, Tidy, Transform, Visualize, and Model Data.[@wickham2023]
2. R in Action, Third Edition: Data Analysis and Graphics with r and Tidyverse. [@kabacoff2022]
3. Ggplot2: Elegant Graphics for Data Analysis.[@wickham-ggplot2]

## 致谢 {-}
感谢在此书编写过程中帮助过我的老师，同学，以及其他朋友，没有大家的关照我几乎不可能完成如此复杂艰巨的工作，感谢！

