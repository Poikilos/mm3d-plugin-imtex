PLUGINS =  \
			  imtex.so \

LFLAGS = -O2 -Wall -lImlib2
CFLAGS = -O2 -Wall -DMM3D_EDIT -I../../src -I../../src/libmm3d -I../.. -DPLUGIN

all: ${PLUGINS}
	
%.o: %.cc
	g++ ${CFLAGS} -c $<

%.so: %.o
	g++ ${LFLAGS} -shared -o $*.so $<

clean:
	rm -rf *.o *.so core core.*
