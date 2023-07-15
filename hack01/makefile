all:
	gcc -m32 --shared hackfile.c -o libhackfile.so

run:
	LD_PRELOAD=libhackfile.so ./docrypt sample.cry

clean:
	rm libhackfile.so