# $@ : target label
# $< : the first prerequisite after the colon
# $^ : all of the prerequisite files
# $* : wildcard matched part

VIEWER=evince
GENERATED_IMAGES=../photos/Creepage_vs_clearance.png ../photos/severity.png

default: pdf

pdf: clean outline.md $(GENERATED_IMAGES)
	pandoc --pdf-engine=xelatex outline.md -o outline.pdf -t beamer

%.png : %.svg
	inkscape --export-png $@ --export-dpi=300 $<

check: pdf
	$(VIEWER) outline.pdf

clean:
	rm -vf outline.pdf $(GENERATED_IMAGES)
