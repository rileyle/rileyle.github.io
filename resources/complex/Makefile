# List the targets to generate.
all: complex.pdf complex.md
	echo "all : done.";echo

# Pattern rule for generating Markdown from LaTeX files.
%.md : %.tex
	pandoc --mathjax -f latex-auto_identifiers -s $*.yaml $*.tex  -t markdown-header_attributes -o $*.md

# Pattern rule for generating PDF from LaTeX files.
%.pdf : %.tex 
	pdflatex $*
	pdflatex $*
	rm *.aux *.log *.out
	echo "$*.pdf : done."

clean:
	rm -f *.aux *.log *.out *.md *.pdf
	echo "clean : done.";echo
