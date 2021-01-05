.PHONY:clean
# 变量的定义
CC = gcc
RM = rm
OBJ = simple
OBJS = main.o foo.o bar.o

# 变量的引用 
$(OBJ):$(OBJS)
	echo 'successful creat *.o file'
main.o:
	$(CC) -c main.c -o main.o
foo.o:
	$(CC) -c foo.c -o foo.o
bar.o:
	$(CC) -c bar.c -o bar.o
clean:
	$(RM) *.o