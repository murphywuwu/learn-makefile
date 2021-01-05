one = export blah="I was set!"; echo $$blah

define two
export blah=set
echo $$blah
endef

all:
	@echo "This print 'I was set'"
	@$(one)
	@echo "This does not print 'I was set' because echo command runs in a seperate shell"
	@$(two)