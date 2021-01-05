## makefile:`@`语法

在上一个例子中执行`make test`, `make all`等打印的结果如下
<!-- 执行命令截图 -->

每个执行命令打印的结果都包含了: 目标中的命令 + 返回结果。这样输出的信息看起来会比较混乱。所以为了使用Make不答应出命令，只要做一点小小的修改，就是在命令前加一个`@`符号。这一符号告诉Make，在运行时不要将这一行命令显示出来。代码如下

```
all: 
	@echo "Hello World"
test:
	echo "It is my test example"
```
运行`make test`,`make all`结果如下:
<!-- 执行命令截图 -->

加了`@`后运行`make test`就只输出"It is my test example"。