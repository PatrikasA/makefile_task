CC:=gcc
BIN:=calculator
CPPFLAGS:=I$(PWD)
SRC:=$(wildcard *.c)
OBJS:=$(SRC:.c=.o)

PREFIX:=/usr

.PHONY: all clean install uninstall

all: $(BIN)

$(BIN): $(OBJS)
	$(CC) $^ -o $@

install:
	install -d $(PREFIX)/bin
	install -m 644 $(BIN) $(PREFIX)/bin/$(BIN)

uninstall:
	$(RM) $(PREFIX)/bin/$(BIN)

clean:
	rm -f $(BIN) $(OBJS)

