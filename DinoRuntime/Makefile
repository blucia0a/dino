CC=msp430-gcc
MEMENTOSDIR=../Mementos
CFLAGS=-mmcu=msp430fr5969 -g -O0 -I$(MEMENTOSDIR)/include 

.DUMMY: all
all: libdino.a

%.s: %.c
	$(CC) $(CFLAGS) -S -o $@ $^

%.c: include/mementos.h

libdino.a: dino.o 
	msp430-ar r $@ $^

clean:
	$(RM) libdino.a *.o
