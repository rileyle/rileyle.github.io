# List the targets to generate.
all: complex.pdf
	echo "all : done.";echo

# Pattern rule for generating Postscript from LaTex files.
# (Latex three times to process references and table of contents.)
complex.pdf : complex.tex complex.eps
	pdflatex complex
	pdflatex complex
	rm *.aux *.log *.out
	echo "complex.ps : done."

clean:
	rm -f *.aux *.log *.out *.pdf
	echo "clean : done.";echo
