the makefile in this directory (/../../ldd3-5/LDD3) is the original makefile from ______________________ .
you can use this as a basis for your files. 

In general all you have to do is:

PREPARING THE MAKEFILE:

1) go to the bottom of the original Makefile and find this last section between `else` and `endif`:

```
else
    # called from kernel build system: just declare what our modules are
    obj-m := hello.o hellop.o seq.o jiq.o sleepy.o complete.o \
             silly.o faulty.o kdatasize.o kdataalign.o jit.o
endif

```

2) If the name .o file(s) corresponding to the .c file(s) you are trying to compile is already listed, move on to step 3.
   Otherwise: add a .o file with the same name as your .c file

3) Remove the names of the files other than the ones you are trying to compile.


Example: 
   
    If you are trying to compile hello.c, the end of your Makefile should look like this:


```
else
    # called from kernel build system: just declare what our modules are
    obj-m := hello.o
endif
```

COMPILING: