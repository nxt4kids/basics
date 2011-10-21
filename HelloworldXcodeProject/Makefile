
# Config
USB=-U

# Path to the NXC compiler relative to the Makefile
NXC=nbc
NXTCOM=nxtcom

# Options to pass to the compiler
OPTIONS=-Z2

# Change the name of the program helloworld.rxe to be whatever you want
# to name the final executable
PROGRAM=helloworld

all: $(PROGRAM).rxe download

$(PROGRAM).rxe: source/$(PROGRAM).nxc Makefile
	cd source;                    \
	$(NXC) -O=../build/$(PROGRAM).rxe \
				$(OPTIONS) \
		        $(PROGRAM).nxc

download: $(PROGRAM).rxe
	cd build;  \
	$(NXTCOM) $(USB) $(PROGRAM).rxe
	
clean:
	/bin/rm -vf build/$(PROGRAM).rxe
		   
