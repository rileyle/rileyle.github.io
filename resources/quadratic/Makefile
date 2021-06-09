# List the targets to generate.
all: quadratic.pdf
	echo "all : done.";echo

# Pattern rule for generating PDF from LaTex files.
quadratic.pdf : quadratic.tex proj.eps
	pdflatex quadratic
	pdflatex quadratic
	rm *.aux *.log *.out
	echo "quadratic.pdf : done."

clean:
	rm -f *.aux *.log *.out *.pdf
	echo "clean : done.";echo
