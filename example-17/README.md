## makefile:条件语句


```
foo = ok

all:
ifeq ($(foo), ok)
	@echo "foo equals ok"
else
	@echo "nope"
endif
```
2.运行目标: 
输入`make`。结果如下
      <!-- 执行命令截图 -->

