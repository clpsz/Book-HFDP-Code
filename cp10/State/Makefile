CXX = g++
CFLAGS = -Wall
LDFLAGS = 

target = _main
srcs = main.cpp Process.cpp
objs = $(srcs:.cpp=.o)
headers = $(wildcard *.h)


.PHONY: all
all: $(target)

$(target): $(objs) $(headers) FORCE
	$(CXX) $(LDFLAGS) -o _main $(objs)
	-rm -f *.o

$(objs):%.o:%.cpp
	$(CXX) $(CFLAGS) -c -o $@ $<

.PHONY: FORCE
FORCE: 

clean:
	rm -f _main *.o

