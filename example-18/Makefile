nullstring = 
foo = $(nullstring)

all:
ifeq ($(strip $(foo)),)
	@echo "foo is empty after being stripped"
endif
ifeq ($(nullstring),)
	@echo "nullstring doesn't even have spaces"
endif
	