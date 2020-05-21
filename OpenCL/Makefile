objects = m01400_a3-optimized2.o

all: $(objects)
	nvcc -arch=sm_61 $(objects) -o app
%.o: %.cu
	nvcc -x cu -arch=sm_61 -I. -I../include/ -I../src/modules/ $< -o $@
clean:
	rm -f *.o app
