#The following macros should be defined.
TARGET1=i2c-pi-arduino-asc
OBJECT1=i2c-pi-arduino-asc.o
OBJECT2=
CC=gcc
CXX=g++
LD=g++
LD_FLAGS+= -lwiringPi
C_FLAGS+= -g -O0
# end of user configuration
#
ALL: $(TARGET1)
$(TARGET1):$(OBJECT1) $(OBJECT2)
	$(LD) $^ $(LD_FLAGS) -o $@
%.o: %.c
	$(CC) $(C_FLAGS) -c $<
%.o: %.cpp
	$(CXX) $(C_FLAGS) -c $<
.PHONY: clean
clean :
	-rm -f $(OBJECT1) $(OBJECT2)
