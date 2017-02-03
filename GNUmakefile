##
## Makefile for test mc + Root lib
##

CC      = g++
CFLAGS  = `root-config --cflags`
LDFLAGS = `root-config --libs`

SRC := $(shell find . -name "*.cc")
OBJ := $(subst .cc,.o,$(SRC))
INC := $(shell find . -name "*.h")

all: example clean

example: $(OBJ)
	#$(CC) -o $@ $^ $(LDFLAGS)
	$(CC) -o $@ $^ $(LDFLAGS)

example.o: example.cc
	$(CC) -c $(CFLAGS) $(INC) $<

Analyzer.o: Analyzer.cc
	$(CC) -c $(CFLAGS) $(INC) $<

.PHONY: clean cleanest

clean:
	rm *.o

cleanest: clean
	rm example
