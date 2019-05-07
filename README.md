# A PhD Thesis Template for JHU Astronomy Students 
A working LaTeX template that is mainly designed for the astro students in the Johns Hopkins University (JHU).

The detailed requirements are listed in the library [webpage](https://www.library.jhu.edu/library-services/electronic-theses-dissertations/formatting-guidelines-checklist/), and this repo is based on the [Brian Weitzner](https://github.com/weitzner) [template](https://github.com/weitzner/jhu-thesis-template) provided in that webpage.

***Highlights***:
1. Use the [NASA/ADS](https://ui.adsabs.harvard.edu) **BibTeX entries** directly.
2. Examples of citation, figure, table, **subfigures**, **horizontal figure**, and **long table**.
3. References orderd by name then publication date.
4. CV template displays publications by author order (i.e., 1st-, 2nd, and n-th aurthored sections), and publication type (i.e., journals and conference proceedings).
5. If you used ```\added{}```, ```\deleted{}```, or ```\replaced{}{}``` while revising your journal manuscript, this template will handle them by displaying the final version only. 
6. Support for Simplified **Chinese** characters. You can adjust it for other languages.

## 1. Compile this template
Obtain this template from https://github.com/seawander/jhu-thesis-template-astro and make your own revisions.

### 1.1 TeXShop Users
Open ```main.tex```, and select ```pdflatexmk```, then click ```Typeset```.

### 1.2 Command-line Users
```cd``` to your directory, type ```make```. Use ```make clean``` to clean up.

## 2. Make Your Revisions
Follow the instructions in the [template](https://github.com/weitzner/jhu-thesis-template) by [Brian Weitzner](https://github.com/weitzner), and the links therein.

A few notes:
1. Compline your cv (in this [folder](https://github.com/seawander/jhu-thesis-template-astro/tree/master/moderncv)) first, then compline your thesis.
2. You can put your figures in different folders, but remember to add the folders' directories to ```\graphicspath{{intro_chapter/}{chapter_apj/}{chapter_apj_dup/}}``` in ```main.tex```.
3. Put your new chapters in a folder, then remembre to add it in ```main.tex```, e.g., starting from the 304 line (or uncomment them if you have identical folders as mine): 
```
%\begin{refsection}[chapterNMF/nmf_chapter.bib] % put your own chapter here in this format
%\include{chapterNMF/nmf_chapter}
%\cleardoublepage
%\printbibliography[title={References}]
%\end{refsection}
```
4. After adding a new chapter, if you use the command-line, then remember to add the corresponding info in the file [```makefile```](https://github.com/seawander/jhu-thesis-template-astro/blob/master/makefile) among line 5 and line 13. Then uncomment or add new lines starting from line 28.

## 3. Limitations
1. This template does not support the [```deluxetable```](https://journals.aas.org/aastexguide/#deluxetable) in AAS Journals, so I adjusted them myself. That's why I used long table (example given in the ```Chapter 2.2.2```). You can probably write an interface yourself. If that works, please let me (or the future graduate students) know!
2. If your paper is published in the [SPIE format](https://www.overleaf.com/latex/templates/spie-proceedings-style-template-and-guidelines-for-authors/qpkhfttzvnhz) (i.e., using numbers for the references), you may have to use ```\citet{}```, ```\citep{}```, and ```\citealp{}``` as in the AAS Journals.
3. I manually bolded my names in the publications in the cv. You can probably try more some automatic method.
4. The reference sections will display all the authors, you may try to limit the number of authors if there are too many. You can use [this solution](https://tex.stackexchange.com/a/26582) to change the [```plainyr-rev.bst```](https://github.com/seawander/jhu-thesis-template-astro/blob/master/moderncv/plainyr-rev.bst) file's line 248 and line 249. I have tested it and that works.
