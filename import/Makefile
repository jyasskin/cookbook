CXX:=g++
DEPENDENCIES:=jsoncpp icu-uc
CXXFLAGS:=-Wall -g -std=gnu++11 $(shell pkg-config --cflags $(DEPENDENCIES)) -DU_CHARSET_IS_UTF8=1
LDFLAGS:=$(shell pkg-config --libs $(DEPENDENCIES))

all: tojson

tojson.o: tojson.cpp cb_database.h Makefile
cb_database.o: cb_database.cpp cb_database.h Makefile

tojson: tojson.o cb_database.o
	$(CXX) -o $@ $^ $(LDFLAGS)
