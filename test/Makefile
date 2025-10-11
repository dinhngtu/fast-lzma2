OBJ=file_test.o
LIB:=-L../ -lfast-lzma2	

CFLAGS:=-Wall -O1 -pthread
CFLAGS+=-g3 -fsanitize=address -fsanitize=undefined
CC:=gcc

EXT:=
ifeq ($(OS),Windows_NT)
	EXT:=.exe
	LIB:=../libfast-lzma2.dll
endif
CFLAGS+=-I../

file_test : $(OBJ)
	$(CC) $(CFLAGS) -pthread -o file_test$(EXT) $(OBJ) $(LIB)

clean:
	rm -f file_test$(EXT) $(OBJ)
