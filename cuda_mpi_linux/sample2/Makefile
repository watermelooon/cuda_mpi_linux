CUDA_INSTALL_PATH = /usr/local/cuda-11.4
MPI_INSTALL_PATH = /usr/local/openmpi-4.1.1
 
NVCC = $(CUDA_INSTALL_PATH)/bin/nvcc
MPICC = $(MPI_INSTALL_PATH)/bin/mpic++
 
LDFLAGS = -L$(CUDA_INSTALL_PATH)/lib64
LIB = -lcudart -lcurand
 
CFILES = test.cpp
CUFILES = test_cuda.cu
OBJECTS = test_cuda.o test.o
EXECNAME = test
 
all:
	$(MPICC) -c $(CFILES)
	$(NVCC) -c $(CUFILES)
	$(MPICC) -o $(EXECNAME) $(OBJECTS) $(LDFLAGS) $(LIB) 
 
clean:
	rm -f *.o $(EXECNAME)
