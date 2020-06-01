ALL_EXE = libNE10.a
all: $(ALL_EXE) 

#CC=gcc
CFLAGS=-I. -I../inc -Wall

VPATH = ../modules/dsp/:../modules/

DEPS = Makefile 

SRC_DIR = ../modules/dsp/

#LIB_FILES =
#LIB_OBJS := $(subst .c,.o,$(LIB_FILES))

libNE10.a: NE10_fft.o NE10_fft_float32.o NE10_fft_generic_float32.o NE10_init.o NE10_fft_int32.o NE10_fft_int32.o NE10_fft_generic_int32.o
# $@: target file name, $^: all prerequisites
#	$(CC) -g -o $@ $^ -lm
	ar rcs $@ $^

clean:
	rm -rf *.o $(ALL_EXE) 

#pattern rules
%.o: %.c $(DEPS)
# $<: first prerequisite
	$(CC) -g -c -o $@ $< $(CFLAGS)

%.o: %.cpp $(DEPS)
	g++ -g -c -o $@ $< $(CFLAGS)

