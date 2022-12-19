ASCIIDoc command cheatsheet
---------------------------
Asciidoc version 10 now works with Python 3.
* Install the python asciidoc package with pip.
* install the python Pygments package with pip for syntax highlighting support

* The basic command is: python -m asciidoc --options sourceFile.txt
* Specify a custom stylesheet using --attribute stylesheet="$(pwd)/repast_stylesheet.css"
* Specify syntax highlighting using --attribute source-highlighter=pygments

Generate Repast FAQ with inline TOC:

	python3 -m asciidoc -a toc -a toclevels=3 --backend=xhtml11 -a icons -a iconsdir=./images --attribute stylesheet="$(pwd)/repast_stylesheet.css" --attribute source-highlighter=pygments RepastFAQ/RepastFAQ.txt

Generate Repast Reference with sidebar navigation and no inline TOC (note different stylesheet):

	python3 -m asciidoc -a toc -a toclevels=3 --backend=xhtml11 -a icons -a iconsdir=./images --attribute stylesheet="$(pwd)/repast_reference_stylesheet.css" --attribute source-highlighter=pygments RepastReference/RepastReference.txt
	
Generate Repast NG browser notes:

	python3 -m asciidoc -a toc -a toclevels=3 --backend=xhtml11 -a icons -a iconsdir=./images --attribute stylesheet="$(pwd)/repast_stylesheet.css" --attribute source-highlighter=pygments RepastNG/browser.adoc


