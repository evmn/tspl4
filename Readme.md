# The Scheme Programming Language

## Download webpages from [The Scheme Programming Language](https://www.scheme.com/tspl4/)

```sh
wget -c -r --no-parent -k https://www.scheme.com/tspl4/
```
## Edit index.html and customize your calibre follow [instructions](https://manual.calibre-ebook.com/faq.html#id15)

```html
<html>
   <body>
     <h1>Table of Contents</h1>
     <p style="text-indent:0pt">
        <a href="file1.html">First File</a><br/>
        <a href="file2.html">Second File</a><br/>
        .
        .
        .
     </p>
   </body>
</html>
```

>By default, when adding HTML files, calibre follows links in the files in depth first order. This means that if file A.html links to B.html and C.html and D.html, but B.html also links to D.html, then the files will be in the order A.html, B.html, D.html, C.html. If instead you want the order to be A.html, B.html, C.html, D.html then you must tell calibre to add your files in breadth first order. Do this by going to Preferences → Advanced → Plugins → File type and customizing the HTML to ZIP plugin.

## Open index.html with Calibre

Right click index.html and select open with Calibre.

## Generate epub

Select convert from zip to epub, and set *Table of Contents*'s *Level 1 TOC(XPath expression)* to `//*[name()='h1']`, and *Level 2 TOC(XPath expression)* to `//*[name()='h3']`, then set chapter mark to none in *Structure detection*.

## Edit book

Search all text files in regex **dot all** and **wrap** mode, remove lines match `<hr class="copyright"/>.*http://www.scheme.com</a></p>`.

# Reference

 - [The Scheme Programming Language](https://www.scheme.com/tspl4/)
