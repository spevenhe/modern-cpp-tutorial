#
# 1.1.cpp
#
# chapter 1 introduction
# modern cpp tutorial
#
# created by changkun at changkun.de
# https://github.com/changkun/modern-cpp-tutorial
#

C = gcc
CXX = g++

SOURCE_C = foo.c
OBJECTS_C = foo.o 

SOURCE_CXX = 1.1.c.and.cpp

TARGET = 1.1.out
LDFLAGS_COMMON = -std=c++17
DEBUG_FLAGS = -g -O0 -Wall

# 构建目录
BUILD_DIR = build
DEBUG_DIR = debug

all:
	dirs
	@echo Directories created
	$(C) -c $(SOURCE_C)
	$(CXX) $(SOURCE_CXX) $(OBJECTS_C) $(LDFLAGS_COMMON) -o $(BUILD_DIR)/$(TARGET)
debug:
	mkdir -p $(DEBUG_DIR)
	$(C) -c $(SOURCE_C) -o $(DEBUG_DIR)/$(OBJECTS_C)
	$(CXX) $(SOURCE_CXX) $(DEBUG_DIR)/$(OBJECTS_C) $(LDFLAGS_COMMON) $(DEBUG_FLAGS) -o $(DEBUG_DIR)/$(TARGET)
clean:
	rm -rf $(BUILD_DIR) $(DEBUG_DIR)
