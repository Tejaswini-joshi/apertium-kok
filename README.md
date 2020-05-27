Konkani

                        apertium-kon
===============================================================================

This is an Apertium monolingual language package for Konkani. What you can use this language package for:

Morphological analysis of Konkani
Morphological generation of Konkani

Requirements
You will need the following software installed:

lttoolbox (>= 3.3.0)
apertium (>= 3.3.0)
vislcg3 (>= 0.9.9.10297)
If this does not make any sense, we recommend you look at: www.apertium.org

Compiling
Given the requirements being installed, you should be able to just run:

$ ./configure $ make

You can use ./autogen.sh instead of ./configure if you're compiling from SVN.

If you're doing development, you don't have to install the data, you can use it directly from this directory.

If you are installing this language package as a prerequisite for an Apertium translation pair, then do (typically as root / with sudo):

make install
You can give a --prefix to ./configure to install as a non-root user, but make sure to use the same prefix when installing the translation pair and any other language packages.

Testing
If you are in the source directory after running make, the following commands should work:

$ echo "TODO: test sentence" | apertium -d . kon-morph TODO: test analysis result

$ echo "TODO: test sentence" | apertium -d . kon-tagger TODO: test tagger result

Files and data
apertium-kon.kon.dix - Monolingual dictionary
kon.prob - Tagger model
apertium-kon.kon.rlx - Constraint Grammar disambiguation rules
apertium-kon.post-kon.dix - Post-generator
modes.xml - Translation modes
Notes on kon.prob
apertium-kon uses the perceptron tagger, so in order for it to work, it needs to be called with -gx: apertium-tagger -gx kon.prob
