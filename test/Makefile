# Copyright (C) 2023 Ethan Uppal. All rights reserved.
#
# Purpose:	builds the test program for the config library.
# Requires:	the config library to be installed.

CC		:= $(shell which gcc || which clang)
CFLAGS	:= -std=c99 -pedantic -Wall -Wextra \
		   -Wno-unused-parameter \
		   -Wno-gnu-zero-variadic-macro-arguments
LDFLAGS	:= -L/usr/local/lib -lconfig \
		   -I/usr/local/include 
SRC		:= main.c
EXEC	:= main

test: build_test
	./main config.txt

build_test: $(SRC)
	$(CC) $(CFLAGS) $(LDFLAGS) $^ -o $(EXEC)

clean:
	rm -rf $(EXEC)
