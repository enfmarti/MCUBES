MonteCUBES - Monte Carlo Utility Based Experiment Simulator
===========================================================

This is MonteCUBES, a Markov Chain Monte Carlo plugin for GLoBES,
intended to optimize the scanning of the neutrino oscillation parameter
space.

MonteCUBES is free software, you can redistribute it and/or modify it
under the terms of the GNU General Public License.

The GNU General Public License does not permit this software to be
redistributed in proprietary programs.

This library is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

Limitations
===========

MonteCUBES is a plugin for GLoBES. You cannot run MonteCUBES without a
working GLoBES installation. As per the GLoBES README:

GLoBES is *not* thread safe.
GLoBES is *not* designed to be used in *security critical* applications 
and environments, e.g. no care has been taken to avoid vulnerability
to heap corruption exploits etc.

These limitations remain true in MonteCUBES.


Credit
======

Like GLoBES, MonteCUEBS is intended for academic use. Thus, the
authors would appreciate being given proper academic credit when it is
used. If you use MonteCUBES to produce a publication or talk, we would
therefore ask you to indicate this and to cite the following
reference:

Mattias Blennow and Enrique Fernandez-Martinez
Neutrino oscillation parameter sampling with MonteCUBES
arXiv: 0903.3985 [hep-ph, hep-ex]

Since using MonteCUBES means that you will also be using GLoBES,
proper credit should also be given to the GLoBES developers. See the
GLoBES README for details.

Availability
============

The current stable version of MonteCUBES as well as the manual is
available from

 GitHub

Installation
============

MonteCUBES follows the standard GNU installation procedure. However,
it needs to be installed in the same directory as your GLoBES
installation. Please consult the INSTALL file in this distribution for
more detailed instructions.

Testing the installation
========================

In order to check the library functions introduced by the MonteCUBES
library, the test program 'mcbtest' will be created along with the library
files. After installation, it is located in the 'bin' directory under the
installation path. When run, it will make a series of checks to make sure
that the library functions work properly. It will also produce a short
Monte Carlo simulation (using only a prior and no experimental definition).
This simulation is made with a fixed random seed and will produce the same
result whenever it is run. The resulting files are named 'out.mcb', 'out.mc1',
and 'out.mc2'. The content of these files should correspond to that of the
files 'testout.mcb', 'testout.mc1', and 'testout.mc2', located in the
'share/doc/montecubes' directory under the installation path.

Files included in the distribution
==================================

The following files are included in the MonteCUBES tar-ball distribution:

In root directory:
ChageLog - Contains a log of changes made to files in directory
AUTHORS  - Contains a list of authors and their contributions
COPYING  - Contains licence for the package (GNU GPL)
INSTALL  - Contains installation instructions
NEWS     - Contains a list of new features
README   - This file
TODO     - A list of future features not yet implemented

In directory "src" (C-library source files):
ChangeLog         - Contains a log of changes made to files in directory 
montecubes.h      - Main header file containing API definitions
montecubes.c      - Main library source file
mcb_data.c        - Contains method for setting rates
mcb_io.h          - Header file for I/O methods
mcb_io.c          - Implementation of I/O methods
mcb_rand.h        - Header file for pseudo random number handling
mcb_rand.c        - Pseudo random number handling methods
mcb_test.c        - Source file for the test program
nsi_probability.h - Header file for the nSIEGE implementation
nsi_probability.c - Implementation of the nSIEGE
nue_probability.h - Header file for the NUE implementation
nue_probability.c - Implementation of the NUE

In directory "matlab" (Matlab GUI files):
ChangeLog           - Log of chages made to files in directory
MonteCUBES.m        - Main GUI file containing GUI handling methods
MonteCUBES.fig      - Matlab .fig for the GUI
MCUBESs.jpg         - MonteCUBES logo used in GUI
MCB_readmcb.m       - Method for reading simulation files
density1D.m         - Method for drawing a 1D histogram plot
scatter1D.m         - Method for drawing chain progression plots
interval1D.m        - Method for drawing 1D confidence intervals
scatter2D.m         - Method for drawing a 2D scatter plot
contournum2Dplain.m - Method for drawing a 2D contour plot
trianglePlot.m      - Method for drawing triangle plots
contournum3D.m      - Method for drawing 3D surface plots
mcbFilter.m         - Method for gaussian filtering

In directory "doc" (documentation and test files):
manual.pdf  - User manual in PDF format
testout.mcb - Output summary file for test program
testout.mc1 - Output chain file for test program
testout.mc2 - Output chain file for test program

In addition, each directory contains files related to the GNU build 
system (Autotools) used to produce a distribution tar-ball and installation
files.


Reporting Bugs
==============

A list of known bugs can be found in the BUGS file.  

If you find a bug which is not listed in these files please report it
to <emb@kth.se>.

All bug reports should include:

       The version number of MonteCUBES, and where you obtained it.
       The version number of GLoBES, and where you obtained it.
       The hardware and operating system
       The compiler used, including version number and compilation options
       A description of the bug behaviour
       A short program which reproducibly exercises the bug

It is also useful if you can report the result of running your program
with the GNU debugger (gdb).

Thank you.

Contributing to MonteCUBES
==========================

If you are interested in participating in MonteCUBES development,
please send a mail to Mattias Blennow <emb@kth.se>
