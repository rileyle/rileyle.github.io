# List the targets to generate.
all: unc.pdf
	echo "all : done.";echo

# Pattern rule for generating PDF from LaTex files.
unc.pdf : unc.tex 
	pdflatex unc
	rm *.aux *.log *.out
	echo "unc.pdf : done."

clean:
	rm -f *.aux *.log *.out *.pdf
	echo "clean : done.";echo
