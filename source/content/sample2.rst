#################################################################
Sample tex to rst
#################################################################

This is a sample file in the text formatter LaTeX. I require you to use

it for the following reasons:



- It produces the best output of text, figures, and equations of any

  program I’ve seen.



- It is machine-independent. It runs on Linux, Macintosh (see

  ``TeXShop``), and Windows (see ``MiKTeX``) machines. You can e-mail

  ``ASCII`` text versions of most relevant files.



- It is the tool of choice for many research scientists and engineers.

  Many journals accept LaTeX submissions, and many books are written in

  LaTeX.



Some basic instructions are given next. Put your text in here. You can

be a little sloppy about spacing. It adjusts the text to look good. You

can make the text smaller. You can make the text tiny.



Skip a line for a new paragraph. You can use italics (*e.g.*

*Thermodynamics is everywhere*) or **bold**. Greek letters are a snap:


.. container:: float

   :name: sample



*A very good and modern option is the web-based*

```https://www.overleaf.com`` <https://www.overleaf.com>`__.



Or you can create a LaTeX file with any text editor (``vi``, ``emacs``,

``gedit``, etc.). To get a document, you need to run the

LaTeX application on the text file. The text file must have the suffix

“``.tex``” On a Linux cluster machine, this is done via the command



``latex file.tex``



This generates three files: ``file.dvi``, ``file.aux``, and

``file.log``. The most important is ``file.dvi``.



The finished product can be previewed in the following way. Execute the

commands:



``dvipdf file.dvi``



This command generates ``file.pdf``, which can be viewed with many

standard tools. Alternatively, you can use ``TeXShop`` on a Macintosh or

``MiKTeX`` on a Windows-based machine. The ``.tex`` file must have a

closing statement as below.



