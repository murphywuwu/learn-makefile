## makefile:define

```
one = export blah="I was set!"; echo $$blah

define two
export blah=set
echo $$blah
endef

all:
	@echo "This print 'I was set'"
	@$(one)
	@echo "This does not print 'I was set' because echo command runs in a seperate shell"
	@$(two)
```
2.运行目标: 
输入`make`。结果如下
      <!-- 执行命令截图 -->

`define`里面实际上只是一连串命令。它和函数没有关系。但是这和命令之间使用分号有点不同。因为在define中的每个命令都按预期在单独的shell中运行。