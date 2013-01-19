PROJECT = spyglass
TARGET = proposal
CC = xelatex
CCFLAGS = -shell-escape
VERSION = 1.0

all: $(TARGET).pdf

%.pdf:	%.tex title/* files/*
	$(CC) $(CCFLAGS) $<


.PHONY:	clean all spell dist
clean:
	rm -f $(TARGET).{pdf,log,aux,pyg}

spell:
	aspell -l el_gr --ignore-case=true -c $(TARGET).tex
dist:
	cp ${TARGET}.pdf ../dist/${PROJECT}_${TARGET}_v_${VERSION}.pdf
