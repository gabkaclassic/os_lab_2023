CC=gcc
CFLAGS=-I.

sequential_min_max : utils.o find_min_max.o utils.h find_min_max.h
	$(CC) -o sequential_min_max find_min_max.o utils.o sequential_min_max.c $(CFLAGS)

program : find_min_max.c utils.c
	gcc -o program find_min_max.c utils.c -lm

parallel_sequence_min_max : parallel_sequence_min_max.c
	$(CC) -o parallel_sequence_min_max parallel_sequence_min_max.c $(CFLAGS)

parallel_min_max : utils.o find_min_max.o utils.h find_min_max.h
	$(CC) -o parallel_min_max utils.o find_min_max.o parallel_min_max.c $(CFLAGS)

utils.o : utils.h
	$(CC) -o utils.o -c utils.c $(CFLAGS)

find_min_max.o : utils.h find_min_max.h
	$(CC) -o find_min_max.o -c find_min_max.c $(CFLAGS)

clean :
	rm utils.o find_min_max.o sequential_min_max parallel_min_max
all :
	rm *.txt utils.o find_min_max.o sequential_min_max parallel_min_max
	$(CC) -o utils.o -c utils.c $(CFLAGS)
	$(CC) -o find_min_max.o -c find_min_max.c $(CFLAGS)
	$(CC) -o sequential_min_max find_min_max.o utils.o sequential_min_max.c $(CFLAGS)
	$(CC) -o parallel_min_max utils.o find_min_max.o parallel_min_max.c $(CFLAGS)
