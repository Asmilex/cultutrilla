# makefile rápido para trabajar con punteros

CC=g++
CPPFLAGS=-Wall -I./includes

DIR_SRC=src/
DIR_OBJ=obj/
DIR_BIN=bin/

SOURCE_MODULES=$(DIR_SRC)main.cpp $(DIR_SRC)punteros.cpp
OBJECT_MODULE=$(SOURCE_MODULES:.cpp=.o)
OBJECT_MODULES=$(OBJECT_MODULE:src=obj) #$(DIR_SRC)=$(DIR_OBJ))
EXECUTABLE=$(DIR_BIN)punteros

$(EXECUTABLE): $(OBJECT_MODULES)

	$(CC) $^ -o $@ #$^  hace refenrencia a todos los objetos de los que depende la regla
.o: .cpp
	$(CC) $(CPPFLAGS) $< -o $@ #$< hace referencia al primer elemento del que depende la regla

clean:
	rm -rf obj/* bin/* include/*~ src/*~


# bin/punteros: obj/main.o
# 	g++ -o bin/punteros obj/main.o
# obj/main.o: src/main.cpp include/punteros.h 
# 	g++ -c -o obj/main.o src/main.cpp
# clean:
# 	rm -rf obj/* bin/* include/*~ src/*~


# bin/intervalo : obj/intervalo.o obj/main.o # para construir inervalo necesitas ...archivos de los que depende
# 	g++ -o bin/intervalo obj/main.o obj/intervalo.o
# obj/intervalo.o: src/intervalo.cpp include/intervalo.h
# 	g++ -c src/intervalo.cpp -o obj/intervalo.o -Iinclude
# obj/main.o: src/main.cpp include/intervalo.h
# 	g++ -c src/main.cpp -o obj/main.o -Iinclude
# clean: #al ir vacío siempre se ejecuta SIEMPRE LLEVAR ESTA ORDEN
# 	rm -rf doc/html	doc/latex obj/* bin/*

# #otras regla adicionales
# doxy:
# 	doxygen doc/intervalo.doxy
# 	firefox doc/html/index.html

# zip: clean # empaquetame todo, pero antes me lo limpias DEBE DE EXISTIR FICHERO ZIP SI NO TE DA ERROR
# 	zip -r zip/practica2.zip * 
