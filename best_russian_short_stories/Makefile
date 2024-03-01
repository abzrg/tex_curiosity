all: main.pdf

build:
	mkdir $@

main.pdf: main.tex | build
	latexmk -dvi- -pdf -file-line-error -interaction=nonstopmode -output-directory=build $<
	ln -sf build/main.pdf best_russian_short_stories.pdf

clean:
	latexmk -output-directory=build -C

.PHONY: all clean
