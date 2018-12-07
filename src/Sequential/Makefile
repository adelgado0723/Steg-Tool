C = gcc
HDRS = ../headers/bmplib.h
OBJS = bstsort.o bmp_steg_tool.o

bmpsteg : bmplib.o bmp_steg_tool.o
	$(C) -o bmpsteg ../headers/bmplib.c bmp_steg_tool.c

bmplib.o : ../headers/bmplib.c
	$(C) -c -g ../headers/bmplib.c

bmp_steg_tool.o : bmp_steg_tool.c 
	$(C) -c -g bmp_steg_tool.c
clean:
	rm -f bmpsteg *.o core *~
$(OBJS) : $(HDRS)
