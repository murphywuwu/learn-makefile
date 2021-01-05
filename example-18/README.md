## makefile:条件语句

### 检查变量是否为空

```
nullstring = 
foo = $(nullstring)

all:
ifeq ($(strip $(foo)),)
	@echo "foo is empty after being stripped"
endif
ifeq ($(nullstring),)
	@echo "nullstring doesn't even have spaces"
endif
```
2.运行目标: 
输入`make`。结果如下
      <!-- 执行命令截图 -->

