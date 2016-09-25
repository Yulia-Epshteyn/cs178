ServerCountThrees: ServerCountThrees.o readInt32BitLE.o
	gcc -o ServerCountThrees ServerCountThrees.o readInt32BitLE.o
	
ServerCountThrees.o: ServerCountThrees.c readInt32BitLE.h
	gcc -c ServerCountThrees.c
	
readInt32BitLE.o: readInt32BitLE.c readInt32BitLE.h
	gcc -c readInt32BitLE.c 
	
test: ServerCountThrees 
	if [ ! -d output ]; then mkdir output; fi
	cp ServerCountThrees output/
	cp threesData.bin output/
	./output/ServerCountThrees