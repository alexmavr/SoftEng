PROJECT = spyglass
TARGET = sdd
CC = xelatex
CCFLAGS = -shell-escape
VERSION = 0.2

all: $(TARGET).pdf

%.pdf:	%.tex preamble.tex title/* files/*
	$(CC) $(CCFLAGS) $(TARGET)
	$(CC) $(CCFLAGS) $(TARGET)


.PHONY:	clean all spell dist
clean:
	rm -f $(TARGET).{pdf,log,aux,pyg}

spell:
	aspell -l el_gr --ignore-case=true -c $(TARGET).tex
dist:
	cp ${TARGET}.pdf ../dist/${PROJECT}_${TARGET}_v_${VERSION}.pdf
