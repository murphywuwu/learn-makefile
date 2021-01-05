## makefile:变量

### 特定于目标的变量

```
all: one = cool

all:
	@echo one is defined: $(one)

other:
	@echo one is nothing: $(one)
```
2.运行目标: 
输入`make`。结果如下
      <!-- 执行命令截图 -->
输入`make other`。结果如下

