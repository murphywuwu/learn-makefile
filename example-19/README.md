## makefile:ifdef

```
bar = 
foo = $(bar)

all:
ifdef foo
	@echo "foo is defined"
endif
ifdef bar
	@echo "but bar is not"
endif
```
2.运行目标: 
输入`make`。结果如下
      <!-- 执行命令截图 -->

