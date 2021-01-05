## makefile:函数

### 语法
`$(fn, arguments) or $(fn, arguments)`

### 示例
```
bar := $(subst not, totally, "I am not superman")
all:
	@echo $(bar)
```

2.运行目标: 
输入`make`。结果如下
      <!-- 执行命令截图 -->


