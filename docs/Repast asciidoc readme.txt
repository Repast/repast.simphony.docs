ASCIIDoc command cheatsheet
---------------------------
The basic command is: python <path to asciidoc.py> --options sourceFile.txt

Generate Repast FAQ with inline TOC:

	python docs/asciidoc-8.6.9/asciidoc.py -a toc -a toclevels=3 --backend=xhtml11 -a icons -a iconsdir=./images docs/RepastFAQ/RepastFAQ.txt

Generate Repast Reference with sidebar navigation and no inline TOC:

	python docs/asciidoc-8.6.9/asciidoc.py -a toc -a toclevels=3 --backend=xhtml11 -a icons -a iconsdir=./images docs/RepastReference/RepastReference.txt

Styles
------
The ASCIIDOC HTML is styled with the default CSS in the /asciidoc-xxx/stylesheets.
The two main CSS files that determine the style for the Repast Reference are
asciidoc.css and toc2.css, the later is used to style the toc2 style used in the
Repast Reference. These CSS files are inlined into the output HTML from ASCIIDOC
so we don't actually need to include them on the site.

The default CSS have been changes as follows:

asciidoc.css 

/* Only underline links on hover */
#toc a:link {text-decoration: none; }
#toc a:hover { text-decoration: underline; }
 
toc2.css

max-width: 50em; 
/* increase the default margin size a bit for wider toc panel  */
margin-left: 23em;

/* increase the default toc width a bit */
width: 20em;
margin-bottom: 1.5em;

/* Only underline links on hover */
#toc a:link {text-decoration: none; }
#toc a:hover { text-decoration: underline; }
