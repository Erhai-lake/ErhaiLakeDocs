# 第一个C语言项目

## 1.打开VS

## 2.创建项目

1. 点击创建项目
2. 在右侧类型中,找到空项目,并选择
3. 下一步
4. 修改项目名称和项目存放路径
5. 最后点创建

![图片](/_media/1.png)

## 3.创建源文件

1. 后缀
   * `.c` 为后缀的叫 源文件
   * `.h` 为后缀的叫 头文件
2. 步骤
    1. 右键源文件
    2. 添加
    3. 新建项
    4. 选择 `c++文件(.cpp)`
    5. 名字改为 `Holle World.c`
    6. 最后点创建

![图片](/_media/2.png)
![图片](/_media/3.png)

## 4.写代码

```C
#include <stdio.h>

//打印一个Holle World到屏幕
// 主函数
int main() {
    // 打印
	printf("Holle World");
    // 返回0
	return 0;
}
```
Ctrl + F5 执行

![图片](/_media/4.png)

> [!TIP]
> C语言代码中一定要有 `main` 函数(主函数)
>
> 标准的主函数写法
>
> ```c
> int main(){
>     return 0;
> }
> ```
>
> `int` - 整数类型
>
> 与 `return 0;` 呼应

> [!WARNING]
> `main` 函数古老的写法(不推荐,有些编译器还编不过去)
> ```C
> void main(){}
> ```

> [!TIP]
> `printf()` 是一个库函数,专门用于打印数据的
>
> 使用 `printf()` 函数,需要声明他的库 `#include <stdio.h>`
>
> `stdio.h`
>
> std - 标准
> i - input - 输入
> o - output - 输出