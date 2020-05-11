.. image:: https://img.shields.io/badge/dmtn--151-lsst.io-brightgreen.svg
   :target: https://dmtn-151.lsst.io
.. image:: https://travis-ci.com/lsst-dm/dmtn-151.svg
   :target: https://travis-ci.com/lsst-dm/dmtn-151

######################################
Host Galaxy Association for DIAObjects
######################################

DMTN-151
========

This document argues that, in order to better enable extragalactic transient science with brokers, two new DIAObject catalog elements should be computed and included in the alert packets: (1) the objectId for the three Object catalog galaxies with the lowest separation distance (based on the galaxy’s 2D luminosity profile) from the DIAObject, and (2) the separation distances for those three Objects.

Links
=====

- Live drafts: https://dmtn-151.lsst.io
- GitHub: https://github.com/lsst-dm/dmtn-151

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-dm/dmtn-151

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the `acronyms.tex` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
