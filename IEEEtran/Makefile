all:
	pdflatex --interaction=nonstopmode -file-line-error paper.tex  
	bibtex paper
	pdflatex --interaction=nonstopmode  -file-line-error paper.tex  
	pdflatex --interaction=nonstopmode  -file-line-error paper.tex

revision:
	pdflatex --jobname=annotated --interaction=nonstopmode -file-line-error paper.tex 
	bibtex annotated
	pdflatex --jobname=annotated --interaction=nonstopmode  -file-line-error paper.tex
	pdflatex --jobname=annotated --interaction=nonstopmode  -file-line-error paper.tex

tar:
	rm -f paper.tar.gz
	tar  --exclude='.git' --exclude='paper.tar.gz' -cvf paper.tar.gz .

clean:
	rm *.{bbl,aux,log,pdf,blg,out}
