## Makefile: 魔术式的隐藏命令

1. 在Makefile文件中输入以下代码

```
.PHONY:clean
RM = rm
OBJ = simple
OBJS = main.o foo.o bar.o

$(OBJ):$(OBJS)
	@echo 'successful creat *.o file'
main.o:
foo.o:
bar.o:
clean:prepare
	@echo $< is finished
	@$(RM) *.o
prepare:
	@echo $@ clean all *.o file
```

2. 运行`make`。结果如下

<!-- 执行命令截图 -->


