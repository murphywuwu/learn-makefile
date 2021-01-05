before_variable = before

one = $(before_variable) one $(later_variable)
two := $(before_variable) two $(later_variable)

later_variable = later

all: 
	@echo $(one)
	@echo $(two)