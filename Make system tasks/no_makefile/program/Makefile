CC:=gcc
BIN:=main
SRC:=$(wildcard *.c)
CFLAGS:= -Wall -Wextra
OBJS:=$(SRC:.c=.o)

PREFIX:=/usr

.PHONY: all install uninstall clean

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $(CFLAGS) -o $@ $^
	
%.o: %.c
	$(CC) $(CFLAGS) -c $^

install:
	install -d $(PREFIX)/include
	install -m 644 maths.h $(PREFIX)/include/maths.h
	install -m 644 usage.h $(PREFIX)/include/usage.h

uninstall:
	$(RM) $(PREFIX)/include/maths.h
	$(RM) $(PREFIX)/include/usage.h

clean:
	$(RM) $(OBJS) $(BIN)
