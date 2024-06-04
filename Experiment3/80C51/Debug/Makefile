###############################################################################
# Makefile for project 
###############################################################################

## General options
PROJECT = 
MCU = 80C51
COMPILER = "ASEM-51 (Proteus)"
TARGET = Debug
SHELL = C:\WINDOWS\system32\cmd.exe

## Tools general options

## Processing Tools
ASM=asem.exe
DDX=ASEMDDX.EXE
#  D:/Experiment/Experiment3/80C51/Debug/Debug.HEX: TOOL=ASM
#  Post: $(DDX) $(DDXFLAGS) Debug.lst
#     D:/Experiment/Experiment3/80C51/Program.asm

# Build tree:
all:	Debug

Debug:	Debug.HEX

Debug.HEX:	../Program.asm 
	$(ASM) "..\Program.asm" "Debug.HEX" Debug.lst $(ASMFLAGS)  /INCLUDES:"..\..\..\..\software5\Proteus 8 Professional\Tools\ASEM51"
	$(DDX) $(DDXFLAGS) Debug.lst

# tidy - delete all temporary files which are not involved in the target generation
tidy:
	rm -rf Debug.lst

# cleanup - delete all generated files
clean:	tidy
	rm -rf Debug.HEX
	rm -rf Debug.SDI
