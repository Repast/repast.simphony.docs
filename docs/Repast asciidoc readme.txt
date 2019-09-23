ASCIIDoc command cheatsheet
---------------------------
The basic command is: python <path to asciidoc.py> --options sourceFile.txt

Generate site with inline TOC:

	python c:\asciidoc-8.6.9\asciidoc.py RepastReference.txt

Generate site with sidebar navigation and no inline TOC:

	python c:\asciidoc-8.6.9\asciidoc.py --conf-file=layout2.conf RepastReference.txt


Styles
------
asiidoc html are styled with the default CSS in the /asciidoc-xxx/stylesheets.
We should figure out how to specify the stylesheet to use so that we can
customize the FAQ and Reference, however since the style is inlined into the 
html output, we can edit the html files directly for small changes.  Here's a 
list of style changes that need to be done after the html is compiled:

FAQ
* change the link style to not underline always, but just underline on hover:

a {
  color: blue;
  text-decoration: none;
}
a:visited {
  color: fuchsia;
}
a:hover {
    text-decoration: underline;
}
