#TargetName : Dependencies
#<TAB>commands

PROJ_NAME=calender
SRC=src/Project_main.c src/calender.c  
#To check if the OS is Windows or Linux and set the executable file extension and delete command accordingly
ifdef OS
	RM = del /q
	FixPath = $(subst /,\,$1)
	EXEC = exe
else
	ifeq ($(shell uname), Linux)
		RM = rm -rf
		FixPath = $1
	  EXEC = out
	endif
endif

Build:$(SRC)
	gcc $(SRC) -Iinc  -o $(call FixPath, $(PROJ_NAME).$(EXEC))

Run :  Build
	./$(call FixPath,$(PROJ_NAME).$(EXEC)) -lm

Clean :
	$(RM) $(call FixPath,*.out) 