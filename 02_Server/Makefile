# Object files needed
OBJS = main.o Webhouse.o handshake.o base64.o sha1.o

# Final target
Template: $(OBJS)
	gcc -o Template $(OBJS) -lbcm2835 -lpthread -ljansson -lm

# Individual source file targets
main.o: main.c Webhouse.h handshake.h
	gcc -c main.c

Webhouse.o: Webhouse.c Webhouse.h
	gcc -c Webhouse.c

handshake.o: handshake.c handshake.h base64.h sha1.h
	gcc -c handshake.c

base64.o: base64.c base64.h
	gcc -c base64.c

sha1.o: sha1.c sha1.h
	gcc -c sha1.c

# Clean target
clean:
	rm -f Template $(OBJS)
