robot.pdf: titlepage.pdf robot.tex all.tex
	printf '\\def\\release{%s}\n' `cat ../../../RELEASE` > release.tex
	printf '\\def\\reldate{%s}\n' "`date '+%B %Y'`" >> release.tex
	pdflatex robot
	sh funcidx_make.sh
	pdflatex robot

titlepage.pdf: figs/rtb-montage.png
	convert $< $@

clean:
	-rm titlepage.pdf *.idx *.ind *.ilg *.aux *.log *.out *.toc

