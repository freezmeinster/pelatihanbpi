MYDIR = .
build: $(MYDIR)/*.md
	for fl in $^ ; do \
		echo "Processing => "$${fl} ;\
		pandoc $${fl} -o $${fl}.pdf \
		"-fmarkdown-implicit_figures -o" \
		-V pagestyle=empty \
		-V papersize:a5 \
		--from=markdown \
		-V geometry:margin=1.5cm; \
	done
	pdftk *.pdf cat output dokumen.pdf
clean: $(MYDIR)/*.pdf
	for fl in $^ ; do \
		rm $${fl} ;\
		echo "Deleting => " $${fl} ;\
	done
