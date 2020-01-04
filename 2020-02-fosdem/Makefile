VIEWER=evince

default: pdf

pdf: outline.md
	pandoc outline.md -o outline.pdf -t beamer

check: pdf
	$(VIEWER) outline.pdf

clean:
	rm -vf outline.pdf
