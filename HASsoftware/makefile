# makefile

# choose model from:
# 1- SimpleTorus3D
# 2- WarpedTorus3D
# 3- WarpedTorus3D_V
# 4- DoubleWell2D_ExtendedVar

ModelDir = models/WarpedTorus3D_V

mainExec : main.o model.o HAS.o
	g++ -std=c++14 -lclapack main.o model.o HAS.o -o mainExec

model.o : $(ModelDir)/model.cpp $(ModelDir)/model.hpp
	g++ -std=c++14 -I$(ModelDir) -c $(ModelDir)/model.cpp

HAS.o : HAS.cpp HAS.hpp $(ModelDir)/model.hpp
	g++ -std=c++14 -I$(ModelDir) -c HAS.cpp

main.o : $(ModelDir)/main.cpp $(ModelDir)/model.hpp HAS.hpp
	g++ -std=c++14 -I$(ModelDir) -c $(ModelDir)/main.cpp


