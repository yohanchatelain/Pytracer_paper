all:
	pdflatex --interaction=nonstopmode -file-line-error paper.tex  
	bibtex paper
	pdflatex --interaction=nonstopmode  -file-line-error paper.tex  
	pdflatex --interaction=nonstopmode  -file-line-error paper.tex

revision:
	pdflatex --jobname=annotated --interaction=nonstopmode -file-line-error paper.tex  -o paper-annotated.pdf
	bibtex annotated
	pdflatex --jobname=annotated --interaction=nonstopmode  -file-line-error paper.tex -o paper-annotated.pdf
	pdflatex --jobname=annotated --interaction=nonstopmode  -file-line-error paper.tex -o paper-annotated.pdf
	mv annotated.pdf paper-annotated.pdf
	
tar:
	rm -f paper.tar.gz
	tar  --exclude='.git' --exclude='paper.tar.gz' -cvf paper.tar.gz .

clean:
	rm *.{bbl,aux,log,pdf,blg,out}