---
output: html_document
encoding: UTF-8
---
# 对象与变量 {#object-variable}

## 基本运算 {#primary-calculation}
可以把R语言当做计算器使用：

``` r
1 + 2
```

```
## [1] 3
```

``` r
5 - 3
```

```
## [1] 2
```

``` r
3 * 4
```

```
## [1] 12
```

``` r
12 / 3
```

```
## [1] 4
```

``` r
2^3
```

```
## [1] 8
```

``` r
(2 + 4) / 3
```

```
## [1] 2
```

## 对象 {#object}
在R中存储的数据称为**对象（object）**，R语言数据处理实际上就是不断的创建和操控这些对象,对象可以理解成用来装数据和函数的盒子或容器（container）。  
<font color="#A5AAA3"><b>
*和python类似，R语言也可以被理解成一种面向对象的编程语言*</b></font> 

<div class="figure" style="text-align: center">
<img src="images/object.png" alt="R语言中的赋值操作" width="80%" height="80%" />
<p class="caption">(\#fig:create-object)R语言中的赋值操作</p>
</div>
如图\@ref(fig:create-object)所示，创建一个R对象，首先确定一个名称，然后使用赋值操作符 <-，将数据赋值给它。（Windows操作系统中赋值的符号可以使用快捷键：ALT + -）

## 变量 {#variable}
这里的R对象在计算机编程语言中称之为**变量（variable）**，和其他编程语言类似，R语言中的变量也有自己的命名规则：

- <font color="#90CBFB"><b>变量名必须以字母、数字、下划线_和句点.组成</b></font> 
- <font color="#90CBFB"><b>变量名的第一个字符不能为数字</b></font>
- <font color="#90CBFB"><b>变量名的第一个字符如果是句点.，那么句点后面不能紧跟数字</b></font>
- <font color="#90CBFB"><b>变量名是区分大小写的，y和Y是两个不同的变量名</b></font>
- <font color="#90CBFB"><b>在中文环境下，汉字也可以作为变量名的合法字符使用，但不推荐使用</b></font>

**举例：**  
1. 赋值变量

``` r
x <- 10
```
2. 打印变量

``` r
x
```

```
## [1] 10
```
3.使用变量

``` r
x + 90
```

```
## [1] 100
```

## 变量的属性和类型 {#attribute-type}
**变量类型**  
所有R对象都有其属性，其中最重要的两个属性是类型和长度,查看变量的类型可以使用***typeof***和***class***函数：

``` r
typeof(x)
```

```
## [1] "double"
```

``` r
class(x)
```

```
## [1] "numeric"
```
<font color="#A5AAA3"><b>*在R语言中，double类型是双精度浮点数的类型。它代表一个十进制数，并且保留了一定的小数位数（通常是15到17位）。double类型是最常用的数值数据类型，因为它们可以用于处理小数值和大数值。在计算中，它们是高精度数字，因此适用于科学计算，统计学和工程应用。*</b></font>

**关于class和typeof两个函数的区别如下：**  
1. typeof() 函数：  
typeof() 函数用于获取对象的基本类型信息，返回一个描述对象类型的字符字符串。
它通常用于确定对象的基本存储类型，例如 "double"（双精度浮点数）、"integer"（整数）、"character"（字符）、"logical"（逻辑值）等。
对于大多数常见的对象类型，typeof() 函数可以给出准确的类型信息，但在某些情况下可能不够详细。  
2. class() 函数：  
class() 函数用于获取对象的类别信息，返回一个描述对象类别的字符字符串或字符向量。
它通常用于确定对象的高级类型，即对象所属的类别或类。
在面向对象编程中，对象的类别定义了对象的属性和方法。通过 class() 函数，你可以确定对象是属于哪个类别，并调用与该类别相关联的方法。
对于基本数据类型（如数字、字符、逻辑值）或没有明确的类别的对象，class() 函数可能返回一个空字符向量。  

R语言中的变量类型包括以下几种：  

- 数值型（Numeric）：用于表示数值的变量类型，包括整数和浮点数。
- 整数型（Integer）：用于表示整数的变量类型。
- 字符型（Character）：用于表示文本字符串的变量类型。
- 逻辑型（Logical）：用于表示逻辑值（真或假）的变量类型。
- 复数型（Complex）：用于表示复数的变量类型。
- 因子型（Factor）：用于表示分类变量的变量类型，具有有限个数的离散取值。
- 日期型（Date）：用于表示日期的变量类型。
- 时间型（POSIXct）：用于表示日期和时间的变量类型。
- 时间型（POSIXlt）：用于表示日期和时间的变量类型，以列表形式存储。
- 数组型（Array）：用于存储多维数据的变量类型。
- 矩阵型（Matrix）：用于存储二维数据的变量类型。
- 列表型（List）：用于存储不同类型元素的变量类型。
- 数据框型（Data Frame）：用于存储二维表格数据的变量类型，类似于表格或数据库中的数据结构。
  
**获取变量的长度**  
对于变量来说最重要的属性除了它的类型外还有它的长度，可以使用***length***函数来确定变量的长度。  

``` r
length(x)
```

```
## [1] 1
```
## 总结

- 介绍了R的计算功能
- 介绍了R中对象和变量的概念以及变量的命名规则
- 介绍了R中变量的属性，及其类型和长度的查看方法







