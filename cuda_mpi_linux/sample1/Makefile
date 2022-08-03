 
CC = mpic++
NVCC = nvcc

LDFLAGS= -L/usr/local/cuda/lib64/  -I/usr/local/cuda/include
LIBS= -lcudart -lcurand -lcufft -lcublas
CFILES= simplempi.cpp
CUFILES= simplempi_cuda.cu
OBJECTS= simplempi.o simplempi_cuda.o
TARGET = simplempi.out


all:
	$(CC) -c $(CFILES)
	$(NVCC) -c $(CUFILES)
	$(CC) -o $(TARGET) $(OBJECTS) $(LDFLAGS) $(LIBS)

clean:
	rm -f *.o $(TARGET)
