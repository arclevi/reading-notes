# Makefile for programs in directory 06-Backtracking-Algorithms
# ***************************************************************

PROGRAMS = \
    maze \
    nim \
    tictac

# ***************************************************************
# Parameters to control Makefile operation
# Note that the gccx command script must be defined

CC = gccx
CFLAGS = 

# ***************************************************************
# Entry to bring the package up to date

all: $(PROGRAMS)

# ***************************************************************
# Standard entries to remove files from the directories
#    tidy    -- eliminate unwanted files
#    scratch -- delete derived files in preparation for rebuild

tidy:
	rm -f ,* .,* *~ core a.out graphics.ps

scratch: tidy
	rm -f *.o *.a $(PROGRAMS)

# ***************************************************************
# C compilations

maze.o: maze.c mazelib.h
	$(CC) $(CFLAGS) -c maze.c

mazelib.o: mazelib.c mazelib.h
	$(CC) $(CFLAGS) -c mazelib.c

nim.o: nim.c
	$(CC) $(CFLAGS) -c nim.c

tictac.o: tictac.c
	$(CC) $(CFLAGS) -c tictac.c


# ***************************************************************
# Executable programs

maze: maze.o mazelib.o
	$(CC) $(CFLAGS) -o maze maze.o mazelib.o

nim: nim.o
	$(CC) $(CFLAGS) -o nim nim.o

tictac: tictac.o
	$(CC) $(CFLAGS) -o tictac tictac.o

