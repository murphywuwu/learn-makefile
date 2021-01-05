## makefile:目标

1.定义目标: 一个makefile可以定义多个目标。如下

```
all: 
	echo "Hello World"
test:
	echo "It is my test example"

```
2.运行目标: 
+ 运行方式1:在shell中输入
  1. `make`,`空格键`,`大写锁定键(Caps Lock)`。会出现如下选择界面
    <!-- 执行命令截图 -->
  2. 继续按下`大写锁定键`,可以选择其中一个命令
    + 选择all。结果如下 
      <!-- 执行命令截图 -->
    + 选择test。结果如下 
      <!-- 执行命令截图 -->
+ 运行方式2。`make`,`回车`。结果如下
      <!-- 执行命令截图 -->

运行`make`和运行`make all`的结果一样。
这是因为当没有指明具体目标是什么时,那么Make以Makefile文件中定义的第一个目标作为本次运行的目标。
