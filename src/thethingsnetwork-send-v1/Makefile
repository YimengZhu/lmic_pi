CFLAGS=-I../../lmic
LDFLAGS=-lwiringPi

thethingsnetwork-send-v1: thethingsnetwork-send-v1.cpp
	cd ../../lmic && $(MAKE)
	$(CC) $(CFLAGS) -o thethingsnetwork-send-v1 thethingsnetwork-send-v1.cpp ../../lmic/*.o $(LDFLAGS)
	gcc -Wall -s -o test-sub test-sub.c -lmosquitto -lpthread

all: thethingsnetwork-send-v1

.PHONY: clean

clean:
	rm -f *.o thethingsnetwork-send-v1
