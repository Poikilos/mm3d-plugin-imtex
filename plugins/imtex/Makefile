PLUGINS =  \
			  imtex.so \

LFLAGS = -O2 -Wall -lImlib2
CFLAGS = -O2 -Wall -I../../src -I../.. -DPLUGIN

all: ${PLUGINS}
	
%.o: %.cc
	g++ ${CFLAGS} -c $<

%.so: %.o
	g++ ${LFLAGS} -shared -o $*.so $<

clean:
	rm -rf *.o *.so core core.*
