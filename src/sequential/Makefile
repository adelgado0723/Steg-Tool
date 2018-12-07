C = gcc
HDRS = ../inc/bmplib.h
OBJS = bmplib.o bmp_steg_tool.o

stegtool : $(OBJS)
	$(C) -o ../../bin/sequential/stegtool ../inc/bmplib.c bmp_steg_tool.c
	cp ../../bin/sequential/stegtool .

bmplib.o : ../inc/bmplib.c
	$(C) -o ../../bin/inc/bmplib.o -c -g ../inc/bmplib.c

bmp_steg_tool.o : bmp_steg_tool.c 
	$(C) -o ../../bin/sequential/bmp_steg_tool.o -c -g bmp_steg_tool.c
clean:
	rm -f ../../bin/sequential/stegtool ../../bin/sequential*.o ../../bin/inc/*.o core *~ stegtool *.o
$(OBJS) : $(HDRS)
