## makefile:赋值

### ?=

```
one = hello
one ?= will not be set
two ?= will be set

all: 
	@echo $(one)
	@echo $(two)

```
2.运行目标: 
输入`make`。结果如下
      <!-- 执行命令截图 -->

`?=`只设置还没有设置过的变量