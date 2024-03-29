---
title: Go 语言基础语法
---

##
Go 标记
Go 程序可以由多个标记组成，可以是关键字，标识符，常量，字符串，符号。如以下 GO 语句由 6 个标记组成：

```go
fmt.Println("Hello, World!")
```
## 行分隔符

在 Go 程序中，一行代表一个语句结束。每个语句不需要像 C 家族中的其它语言一样以分号 ; 结尾，因为这些工作都将由 Go 编译器自动完成。

如果你打算将多个语句写在同一行，它们则必须使用 ; 人为区分，但在实际开发中我们并不鼓励这种做法。

以下为两个语句：

```go
fmt.Println("Hello, World!")
fmt.Println("菜鸟教程：runoob.com")
```

## 注释
注释不会被编译，每一个包应该有相关注释。

单行注释是最常见的注释形式，你可以在任何地方使用以 // 开头的单行注释。多行注释也叫块注释，均已以 /* 开头，并以 */ 结尾。如：

```java
// 单行注释
/*
 Author by 菜鸟教程
 我是多行注释
 */
 ```

 ## 标识符
标识符用来命名变量、类型等程序实体。一个标识符实际上就是一个或是多个字母(A~Z和a~z)数字(0~9)、下划线_组成的序列，但是第一个字符必须是字母或下划线而不能是数字。

以下是有效的标识符：

```go
mahesh   kumar   abc   move_name   a_123
myname50   _temp   j   a23b9   retVal
```

以下是无效的标识符：

```text
1ab（以数字开头）
case（Go 语言的关键字）
a+b（运算符是不允许的）
```

## 字符串连接
Go 语言的字符串连接可以通过 + 实现：

实例
```go
package main
import "fmt"
func main() {
    fmt.Println("Google" + "Runoob")
}

```

以上实例输出结果为：
::: tip 输出结果
GoogleRunoob
:::

## 关键字

下面列举了 Go 代码中会使用到的 25 个关键字或保留字：

```go
break	default	func	interface	select
case	defer	go	map	struct
chan	else	goto	package	switch
const	fallthrough	if	range	type
continue	for	import	return	var
```

除了以上介绍的这些关键字，Go 语言还有 36 个预定义标识符：

```go
append	bool	byte	cap	close	complex	complex64	complex128	uint16
copy	false	float32	float64	imag	int	int8	int16	uint32
int32	int64	iota	len	make	new	nil	panic	uint64
print	println	real	recover	string	true	uint	uint8	uintptr
```

程序一般由关键字、常量、变量、运算符、类型和函数组成。

程序中可能会使用到这些分隔符：括号 ()，中括号 [] 和大括号 {}。

程序中可能会使用到这些标点符号：.、,、;、: 和 …。

## Go 语言的空格
在 Go 语言中，空格通常用于分隔标识符、关键字、运算符和表达式，以提高代码的可读性。

Go 语言中变量的声明必须使用空格隔开，如：

```go
var x int
const Pi float64 = 3.14159265358979323846
```

在运算符和操作数之间要使用空格能让程序更易阅读：

无空格：

```go
fruit=apples+oranges;
```
在变量与运算符间加入空格，程序看起来更加美观，如：

```go
fruit = apples + oranges; 
```
在关键字和表达式之间要使用空格。

例如：

```go
if x > 0 {
    // do something
}
```

在函数调用时，函数名和左边等号之间要使用空格，参数之间也要使用空格。

例如：
```
result := add(2, 3)
```

## 格式化字符串
Go 语言中使用 fmt.Sprintf 或 fmt.Printf 格式化字符串并赋值给新串：

+ Sprintf 根据格式化参数生成格式化的字符串并返回该字符串。
+ Printf 根据格式化参数生成格式化的字符串并写入标准输出。

### Sprintf 实例
```go 
package main

import (
    "fmt"
)

func main() {
   // %d 表示整型数字，%s 表示字符串
    var stockcode=123
    var enddate="2020-12-31"
    var url="Code=%d&endDate=%s"
    var target_url=fmt.Sprintf(url,stockcode,enddate)
    fmt.Println(target_url)
}
```

::: tip 输出结果为
Code=123&endDate=2020-12-31
:::

### Printf 实例
```go
package main

import (
    "fmt"
)

func main() {
   // %d 表示整型数字，%s 表示字符串
    var stockcode=123
    var enddate="2020-12-31"
    var url="Code=%d&endDate=%s"
    fmt.Printf(url,stockcode,enddate)
}

```

::: tip 输出结果为
Code=123&endDate=2020-12-31
:::
