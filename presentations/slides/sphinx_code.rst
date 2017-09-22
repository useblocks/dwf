.. revealjs::

    .. revealjs:: Working with existing code
        :subtitle: 1/5

        Reuse existing code

        .. rv_code::

            .. literalinclude::  slides/sphinx_code.rst
                :language: rst
                :lines: 3-10
                :linenos:

        .. literalinclude::  slides/sphinx_code.rst
                :language: rst
                :lines: 3-10
                :emphasize-lines: 1, 3-4
                :linenos:

        .. rv_small::

            Sphinx documentation: `Showing code examples <http://www.sphinx-doc.org/en/stable/markup/code.html>`_

    .. revealjs:: Working with existing code
        :subtitle: 2/5

        Automated code documentation

        .. rv_code::

            .. autofunction:: os.path.join

        .. autofunction:: os.path.join
            :noindex:

        .. rv_small::

            Sphinx documentation: `Include documentation from docstrings <http://www.sphinx-doc.org/en/stable/ext/autodoc.html>`_

    .. revealjs:: Working with existing code
        :subtitle: 3/5

        Inheritance diagrams

        .. rv_code::

            .. inheritance-diagram:: dwf.Dwf

        .. inheritance-diagram:: dwf.Dwf
            :parts:  1


        Used code (examples/dwf/dwf.py):

        .. literalinclude::  ../examples/dwf/dwf.py
                :language: python

        .. rv_small::

            Sphinx documentation: `Include inheritance diagrams <http://www.sphinx-doc.org/en/stable/ext/inheritance.html>`_

    .. revealjs:: Working with existing code
        :subtitle: 4/5

        Documenting program output

        .. rv_code::

            .. command-output:: python -V

        .. command-output:: python -V

        .. rv_small::

            Sphinx documentation: `sphinxcontrib.programoutput <http://sphinxcontrib-programoutput.readthedocs.io/en/latest/>`_

    .. revealjs:: Working with existing code
        :subtitle: 5/5

        Documenting database models

        .. rv_code::

            .. sadisplay::
                :module: dwf_db

        .. image:: _static/sphinx_database.png

        Sphinx documentation: `sphinxcontrib-sadisplay <https://pypi.python.org/pypi/sphinxcontrib-sadisplay>`_

        Standalone tool: `sadisplay <https://pypi.python.org/pypi/sadisplay>`_
