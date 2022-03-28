Working with existing code
--------------------------

Reuse existing code 1/5
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block::

   .. literalinclude::  /slides/sphinx_code.rst
      :language: rst
      :lines: 3-10
      :linenos:

.. container:: small

   Result:

.. literalinclude::  /slides/sphinx_code.rst
   :language: rst
   :lines: 3-10
   :emphasize-lines: 1, 3-4
   :linenos:

.. container:: small

   Sphinx documentation: `Showing code examples <http://www.sphinx-doc.org/en/stable/markup/code.html>`_


Automated code documentation 2/5
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. code-block:: rst

   .. autofunction:: os.path.join

.. container:: small

   Result:

.. autofunction:: os.path.join
   :noindex:

.. container:: small

   Sphinx documentation: `Include documentation from docstrings <http://www.sphinx-doc.org/en/stable/ext/autodoc.html>`_

Inheritance diagrams 3/5
~~~~~~~~~~~~~~~~~~~~~~~~
.. code-block:: rst

   .. inheritance-diagram:: dwf.Dwf

.. inheritance-diagram:: dwf.Dwf
   :parts:  1


Used code (examples/dwf/dwf.py):

.. literalinclude::  /../examples/dwf/dwf.py
   :language: python

.. container:: small

   Sphinx documentation: `Include inheritance diagrams <http://www.sphinx-doc.org/en/stable/ext/inheritance.html>`_

Documenting program output 4/5
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. code-block:: rst

   .. command-output:: python -V

.. container:: small

   Result:

.. command-output:: python -V

.. container:: small

   Sphinx documentation: `sphinxcontrib.programoutput <http://sphinxcontrib-programoutput.readthedocs.io/en/latest/>`_

Documenting database models 5/5
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. code-block::

   .. sadisplay::
      :module: dwf_db

.. image:: /_static/sphinx_database.png

.. container:: small

   Sphinx documentation: `sphinxcontrib-sadisplay <https://pypi.python.org/pypi/sphinxcontrib-sadisplay>`_

   Standalone tool: `sadisplay <https://pypi.python.org/pypi/sadisplay>`_
