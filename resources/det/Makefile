all: det.pdf
	echo "all : done.";echo

# Pattern rule for generating PDF from LaTex files.
det.pdf : det.tex dets.eps
	pdflatex det
	pdflatex det
	rm *.aux *.log *.out
	echo "det.pdf : done."

clean:
	rm -f *.aux *.log *.out *.pdf
	echo "clean : done.";echo
