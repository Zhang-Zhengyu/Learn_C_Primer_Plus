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
#### 2.2.2.1 #include 指令和头文件

#include 这行代码是一条 ***C预处理器指令（preprocessor directive)***

通常，C编译器会在编译前对源码进行一些准备工作，即 ***预处理(preprocessing)***

studio.h 文件包含了供编译器使用的输入和输出函数（如：printf( )）

C程序顶部的信息集合称作 ***头文件（header）***

并非所有程序都会用到 studio.h （I/O（输入/输出）包）

#### 2.2.2.2 main( )函数








