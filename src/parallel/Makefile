C = mpic++
HDRS = ../inc/bmplib.h
OBJS = bstsort.o bmp_steg_tool.o

stegtool : $(OBJS)
	$(C) -o ../../bin/parallel/stegtool ../inc/bmplib.c bmp_steg_tool.c
	cp ../../bin/parallel/stegtool .

bmplib.o : ../inc/bmplib.c
	$(C) -o ../../bin/inc/bmplib.o -c -g ../inc/bmplib.c

bmp_steg_tool.o : bmp_steg_tool.c 
	$(C) -o ../../bin/parallel/bmp_steg_tool.o -c -g bmp_steg_tool.c
clean:
	rm -f ../../bin/parallel/stegtool ../../bin/parallel*.o ../../bin/inc/*.o core *~ stegtool *.o
$(OBJS) : $(HDRS)
