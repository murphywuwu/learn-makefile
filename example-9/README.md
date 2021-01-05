## Makefile: 自动变量

1. 在Makefile文件中输入以下代码

```
.PHONY:clean
CC = gcc
RM = rm
OBJ = simple
OBJS = main.o foo.o bar.o

$(OBJ):$(OBJS)
	echo 'successful creat *.o file'
main.o:main.c
	$(CC) -c $^ -o $@
foo.o:foo.c
	$(CC) -c $^ -o $@
bar.o:bar.c
	$(CC) -c $< -o $@
clean:prepare
	@echo $< is finished
	@$(RM) *.o
prepare:
	@echo $@ clean all *.o file
```

2. 先运行`make`，再运行`make clean`。结果如下

<!-- 执行命令截图 -->

这里面的`$@`和`$^`又分别是什么意思呢。一条规则由目标，依赖以及命令组成。一条规则中可以有多条命令。当目标和先决条件的名字在规则的命令中多次出现，每一次出现都是一种麻烦？更为麻烦的是，如果改变了目标和依赖名，那得在命令中全部跟着改。有没有简化这种更改的方法呢？这时便需要用到自动变量，如下

   + `$@`用于表示一个规则中的目标。当一个规则中有多个目标时，`$@`所指的是其中任何造成命令被运行的目标。
   + `$^`则是规则中的所有选择条件
   + `$<`表示的是规则中的第一个先决条件
