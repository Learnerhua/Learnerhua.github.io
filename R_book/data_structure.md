---
output: html_document
encoding: UTF-8
---
# 数据基本结构 {#data-structure}
前面我们已经介绍过向量，它是R中最基本的数据结构，这章我们来认识一下R中其他几种常见的数据结构

- 矩阵
- 列表
- 数据框

## 矩阵 {#matrix}
矩阵可以存储行(row)和列(column)二维的数据。它实际上是向量的另一种表现形式，也就说它的本质还是向量，一维的向量用二维的方式呈现。  
在R语言中通过matrix函数来创建矩阵：  


```r
matrix(c(2,4,6,3,7,8), nrow = 2, ncol = 3)
```

```
##      [,1] [,2] [,3]
## [1,]    2    6    7
## [2,]    4    3    8
```
默认矩阵的排列方向是按列从左往右排列，当然，也可以按行从上往下排列，只需要添加byrow参数即可：  

```r
matrix(c(2,4,6,3,7,8), nrow = 2, ncol = 3, byrow = TRUE)
```

```
##      [,1] [,2] [,3]
## [1,]    2    4    6
## [2,]    3    7    8
```
矩阵的相关属性如下：

```r
m <- matrix(c(2,4,6,3,7,8), nrow = 2, ncol = 3)
class(m)
```

```
## [1] "matrix" "array"
```

```r
length(m)
```

```
## [1] 6
```

```r
dim(m)#矩阵的维度
```

```
## [1] 2 3
```
<font color="#90CBFB"><b>个人理解：</b></font>**矩阵其实就是将一维的向量平铺开来，展示成二维的形式，所以矩阵中的元素全部是同一类型的。**


## 列表 {#list}
列表可以理解成多个向量的集合。  
在R中可以使用list函数来创建列表：  

```r
list1 <- list(
  a = c(5, 10),
  b = c("I", "love", "R", "language", "!"),
  c = c(TRUE, TRUE, FALSE, TRUE)
)
list1
```

```
## $a
## [1]  5 10
## 
## $b
## [1] "I"        "love"     "R"        "language" "!"       
## 
## $c
## [1]  TRUE  TRUE FALSE  TRUE
```
|异同|向量|列表|
|----|----|----|
|相同点|元素之间用逗号隔开|元素之间用逗号隔开|
|不同点|元素是单个值，每个元素的数据类型必须相同|元素可以是向量矩阵或者列表|

列表的属性如下：  

```r
class(list1)
```

```
## [1] "list"
```

```r
length(list1)
```

```
## [1] 3
```

## 数据框 {#dataframe}
数据框其实是一种特殊形式的列表，即如果列表中的元素是**等长的向量**那么这样的列表就是一个数据框。数据框类似于我们经常用的excel表格，由于数据框融合了向量、列表和矩阵的特性，所以在数据科学的统计建模和可视化中运用非常广泛。  
在R中，使用**data.frame**函数来创建数据框：  

```r
df <- data.frame(
  name      = c("Alice", "Bob", "Carl", "Dave"),
  age       = c(23, 34, 23, 25),
  marriage  = c(TRUE, FALSE, TRUE, FALSE),
  color     = c("red", "blue", "orange", "purple")
)
df
```

```
##    name age marriage  color
## 1 Alice  23     TRUE    red
## 2   Bob  34    FALSE   blue
## 3  Carl  23     TRUE orange
## 4  Dave  25    FALSE purple
```
数据框的属性如下：  

```r
class(df)
```

```
## [1] "data.frame"
```

```r
nrow(df)
```

```
## [1] 4
```

```r
ncol(df)
```

```
## [1] 4
```

## 总结
- 介绍了矩阵的定义，创建方法，属性
- 介绍了列表的定义，创建方法，属性
- 介绍了数据框的定义，创建方法，属性**（重点）**




