**Keep acquisition metadata with converted images**

This is a development fork of `dcmstack <https://github.com/moloney/dcmstack>`__, a Python toolkit for DICOM-to-NIfTI conversion with metadata extraction and summarization. Upstream can retain that metadata in a NIfTI header extension or a separate JSON file, which is useful when downstream analysis needs more acquisition context than the voxel array alone provides.

**Contribution to review:** `PR #102 <https://github.com/moloney/dcmstack/pull/102>`__ proposes copying metadata-filter defaults before modifying them for an individual call. Its aim is to keep filter settings independent across repeated calls.

Begin with the `official documentation <https://dcmstack.readthedocs.org/>`__ for conversion and metadata handling, or the installation instructions below. The `branch comparison <https://github.com/moloney/dcmstack/compare/master...jdotc1:master>`__ shows this fork's default branch; the linked upstream pull request holds the proposed contribution.

----

========
dcmstack
========

This package provides DICOM to Nifti conversion with the added ability 
to extract and summarize meta data from the source DICOMs. The meta data
can be injected it into a Nifti header extension or written out as a JSON 
formatted text file.


Installing
----------

You can the latest release from PyPI by doing:

.. code-block:: console

  $ pip install dcmstack


Documentation
-------------

Documentation can be read online: https://dcmstack.readthedocs.org/

You can build the HTML documentation under build/sphinx/html with:

If you have the *sphinx* and *numpydoc* packages and a *make* command you 
can build the documentation by running the *make* command in the *doc/* 
directory. For example, to create the HTML documentation you would do:

.. code-block:: console
  
  $ python setup.py build_sphinx
  $ make html

And then view doc/_build/html/index.html with a web browser.


Running Tests
-------------

You can install dcmstack along with any test dependencies by installing the ``test`` 
extra. Then you can run the ``pytest`` command to run the test-suite:

.. code-block:: console
  
  $ pip install dcmstack[test]
  $ pytest

