## makefile:变量

### 文本替换

```
foo := a.o b.o c.o
foo := a.o b.o c.o

bar := $(foo:.o=.c)
# bar := $(foo:%.o=%)

all:
	@echo $(bar)
```
2.运行目标: 
输入`make`。结果如下
      <!-- 执行命令截图 -->

