VIEWER=evince

default: pdf

pdf: clean outline.md
	pandoc --latex-engine=xelatex outline.md -o outline.pdf -t beamer

check: pdf
	$(VIEWER) outline.pdf

clean:
	rm -vf outline.pdf
