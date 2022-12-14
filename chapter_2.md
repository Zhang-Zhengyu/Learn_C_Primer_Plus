## 2.1
```
getchar()
```
这行代码会让程序等待击键，窗口会在用户按下下一个键后关闭。

## 2.2 示例解释
`
#include<stdio.h>
`
预处理指令

stdio.h 提供键盘输入和屏幕输出的支持

`
int main(void)
`

main( )总是第一个被调用的函数

int 表明main( )函数返回一个整数

void表明main( )不带任何参数

- 注释在`/*`和`*/`两个符号之间

例： `/*一个简单的C程序*/`

```
return 0;
```
该行可视作结束main( )函数的要求

### 2.2.2 程序细节

**1. #include 指令和头文件**

#include 这行代码是一条 ***C预处理器指令（preprocessor directive)***

通常，C编译器会在编译前对源码进行一些准备工作，即 ***预处理(preprocessing)***

studio.h 文件包含了供编译器使用的输入和输出函数（如：printf( )）

C程序顶部的信息集合称作 ***头文件（header）***

并非所有程序都会用到 studio.h （I/O（输入/输出）包）

<br>

**2. main( )函数**

绝大多C程序从main()函数开始执行.

<br>


**3.注释**

`/*这是一条注释*/`
```C
/*这也是注释，
分成两行。*/
```

`//这种注释只能写成一行`

<br>

**4.花括号、函数体和块**

{

}

一般而言，所有的C函数都使用花括号标记函数体的开始和结束

花括号可用于把函数中的多条语句合并为一个单元或块（类似Pascal中`begin`和`and`）

<br>

**5.声明** *(declaration)*

`int num;`

这行代码叫作 声明 *（declaration）*，声明完成了两件事
   1. 在函数中有一个名为`num`的变量 *（variable）*
   2. `int`表明num是一个整数（没有小数点或小数部分）
   
`int`是C语言的一个关键字 *（keyword）*，表示一种基本的C语言数据类型。关键字是语言定义的单词，不能用作其他用途。

如：int不能用作函数名和变量名

在C语言中，所有的变量都必须先声明才能使用

以前的C语言，要求把变量声明在块的顶部，其他语句不能再任何声明的前面：

```C
int main() //旧规则
{
    int doors;
    int dogs;
    doors = 5;
    dogs = 3;
    //其他语句
}
```

C99 和C11 遵循C++的惯例，可以把声明放在块中任何位置（尽管如此，首次使用变量之前一定要先声明）

可以这样写：
```C
int main() //目前的C规则
{
    //一些语句
    int doors;
    doors = 5; //第一次使用doors
    //其他语句
    int dogs = 3; //第一次使用dogs
    //其他语句
}
```

- 命名
 
  - 给变量命名时使用有意义的变量名或标识符（例：一个变量用来数羊，变量名应为`sheep_count`而不是`x3`.

  如果变量名无法清楚地表达自身的用途，可在注释中进一步说明.

  C99 和 C11 允许使用更长的标识符名，但编译器只识别前63个字符。

  可以用小写字母、大写字母、数字和下划线(_)来命名，
  - **名称的第一个字符必须是字母或下划线**。

  - **避免自己使用以一个或两个下划线字符开始的标识符。** 因为操作系统和C库经常使用以一个或两个下划线字符开始的标识符
  - C语言的名称区分大小写
  
<br>

**6.赋值**

`num = 1;`

该复制表达语句从右侧把值赋到左侧，以分号结尾。

<br>

**7.printf()函数**

```C
printf("I am a simple ");
printf("computer.\n");
printf("My favourite number is %d because it is first.\n",unm);
```

圆括号表明`printf`是一个函数名，圆括号中的内容是从`main()`函数传递给`printf()`函数的信息。
如上第一行把I am a simple 传递给printf()函数。该信息被称为参数，或函数的实际参数（*actual argument*）

- 实际参数（简称实参）是传递给函数的特定值，
- 形式参数（简称形参）是函数中用于存储的变量。

\n组合代表一个换行符（*newline character*)

换行符是一个转义序列（*escape sequence*）。转义序列用于代表难以表示或难以输入的字符，每个转义序列都以反斜杠（\）开始。

%d相当一个占位符，%提醒程序该处打印一个变量，d表明把变量作为十进制整数打印

<br>

**8.return 语句**

见第十一章

<br>

## 2.3 简单程序的结构

```C
int main(void) //函数头

{
  int q; //声明
  q = 1; //语句
  printf("%d is neat.\n",q);//语句
  return 0;

}
```

简而言之
```C
#include <stdio.h>
int main(void)
{
  语句
  return 0；
}
```

## 2.4 提高程序的可读性
1. 选择有意义的函数名
2. 写注释
3. 在函数中用空行分隔概念上的多个部分
4. 每条语句各占一行

## 2.5 进一步使用C

```C
// fathm_ft.c -- 把2英寻转换成英尺
#include <stdio.h>
int main(void) 
{
	int feet, fathoms;
  
	fathoms = 2;
	feet = 6 * fathoms;
	printf("There are %d feet in %d fathoms!\n", feet, fathoms);
	printf("Yes, I said %d feet!\n", 6 * fathoms);
	return 0;
}
```

