.PHONY:clean
RM = rm
OBJ = simple
OBJS = main.o foo.o bar.o

$(OBJ):$(OBJS)
	@echo 'successful creat *.o file'
main.o:
foo.o:
bar.o:
clean:prepare
	@echo $< is finished
	@$(RM) *.o
prepare:
	@echo $@ clean all *.o file