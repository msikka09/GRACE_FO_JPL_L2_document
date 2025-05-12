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

:math:`\Psi`, :math:`\psi`, :math:`\Phi`, :math:`\phi`. Equations within

text are easy— A well known Maxwell thermodynamic relation is

:math:`\left.{\partial T \over \partial P}\right|_{s} = 

\left.{\partial v \over \partial s}\right|_{P}`. You can also set aside

equations like so:



.. math::



   \begin{aligned}

   du &=& T\ ds -P\ dv, \qquad \mbox{first law.}\label{fl}\\

   ds &\ge& {\delta q \over T}.\qquad  \qquad \mbox{second law.} \label{sl}

   \end{aligned}



Eq. (`[fl] <#fl>`__) is the first law. Eq. (`[sl] <#sl>`__) is the

second law. References [1]_ are available. If you have a postscript

file, say ``sample.figure.eps``, in the same local directory, you can

insert the file as a figure. Figure `1 <#sample>`__, below, plots an

isotherm for air modeled as an ideal gas.



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



.. [1]

   Lamport, L., 1986, *LaTeX: User’s Guide & Reference Manual*,

   Addison-Wesley: Reading, Massachusetts.

