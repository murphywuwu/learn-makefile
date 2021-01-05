## Makefile: 变量

1. 在Makefile文件中输入以下代码

```
.PHONY:clean
# 变量的定义
CC = gcc
RM = rm
OBJ = simple
OBJS = main.o foo.o bar.o

# 变量的引用 
$(OBJ):$(OBJS)
	echo 'successful creat *.o file'
main.o:
	$(CC) -c main.c -o main.o
foo.o:
	$(CC) -c foo.c -o foo.o
bar.o:
	$(CC) -c bar.c -o bar.o
clean:
	$(RM) *.o
```

2. 先运行`make`，再运行`make clean`得到的结果和上个例子的结果一样。如下图

<!-- 执行命令截图 -->

**变量的定义**
如上，makefile的变量定义很简单，就是一个名字(变量名)后面跟上一个等号，然后再这个等号后面放变量所期望的值。
**变量的引用**
通过`$(变量名)`或者`${变量名}`这种模式。