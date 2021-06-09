# List the targets to generate.
all: cramer.pdf
	echo "all : done.";echo

# Pattern rule for generating Postscript from LaTex files.
# (Latex three times to process references and table of contents.)
cramer.pdf : cramer.tex 
	pdflatex cramer
	pdflatex cramer
	rm *.aux *.log *.out
	echo "cramer.pdf : done."

clean:
	rm -f *.aux *.log *.out *.pdf
	echo "clean : done.";echo
