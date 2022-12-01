COMPILER = gcc
CXXFLAGS = -std=c++11
LINKING_FLAGS = -lstdc++ -lncurses

OBJECT_FILES_DIST = "./object_files/"

OBJECT_FILES = main.o matrix.o

cmatrix: $(OBJECT_FILES)
	@printf "linking the created object files\n"
	$(COMPILER) $(OBJECT_FILES) $(LINKING_FLAGS) -o cmatrix
	@mv *.o $(OBJECT_FILES_DIST)

main.o: main.cpp
	@printf "main.cpp -> main.o\n"
	$(COMPILER) -c main.cpp $(CXXFLAGS) 

matrix.o: matrix.cpp matrix.h
	@printf "matrix.cpp -> matrix.o\n"
	$(COMPILER) -c matrix.cpp $(CXXFLAGS)


clean:
	@printf "removing object and executablefiles\n"
	rm -f ./object_files/* cmatrix