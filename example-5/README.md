## makefile:依赖关系

1. 在makefile中输入如下代码

```
all:test1 test2
	@echo "Hello World"
test1:
	@echo "It is my test example1"
test2:
  @echo "It is my test example2"
```
2. 在终端中运行`make all`，结果如下

<!-- 执行命令截图 -->

如上诉结果运行`make all`,先打印了`make test1`的输出结果，接着再打印了`make test2`输出的结果，最后打印了`make all`的结果。

为什么会出现这样的结果呢？这是因为`all:test1 test2`这一行代码定义了三个目标之间的依赖关系。all目标后面的test1,test2是告诉Make,all目标依赖test1,test2目标，这一依赖目标在Makefile中又被称为先决条件。出现这种依赖关系时，Make工具会按**从左到右**的先后顺序先构建规则中所依赖的每一个目标。如果希望构建all目标，那么Make会在构建它之前先构建test1,test2目标，这就是为什么我们称之为先决条件的原因。
