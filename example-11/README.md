## makefile:赋值

### :=

```
before_variable = before

one = $(before_variable) one $(later_variable)
two := $(before_variable) two $(later_variable)

later_variable = later

all: 
	@echo $(one)
	@echo $(two)

```
2.运行目标: 
输入`make`。结果如下
      <!-- 执行命令截图 -->

`:=`只引用在此语句前已经定义了的变量