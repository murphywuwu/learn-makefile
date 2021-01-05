.PHONY:clean
CC = gcc
RM = rm
OBJ = simple
OBJS = main.o foo.o bar.o

$(OBJ):$(OBJS)
	@echo 'successful creat *.o file'
main.o:main.c
	$(CC) -c $^ -o $@
foo.o:foo.c
	$(CC) -c $^ -o $@
bar.o:bar.c
	@$(CC) -c $< -o $@
clean:prepare
	@echo $< is finished
	@$(RM) *.o
prepare:
	@echo $@ clean all *.o file