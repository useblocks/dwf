.. revealjs::

    .. revealjs:: Sphinx
        :subtitle: Documentation generator

        .. image:: _static/sphinx_workflow.png


        `Sphinx <http://www.sphinx-doc.org>`_,
        based on
        `docutils <http://docutils.sourceforge.net/>`_
        and
        `restructuredText <http://docutils.sourceforge.net/rst.html>`_

    .. revealjs:: Sphinx Basics
        :subtitle: 1/3

        .. code-block:: rst

            Sphinx Basics
            =============

            Text styles
            ------------
            **bold text**  *italic text*  ``code sample``

            Links
            -----
            http://dwf.rtfd.io

            `Documentation without frustration <http://dwf.rtfd.io>`_

        .. rv_small::

            Sphinx documentation: `reStructuredText Primer <http://www.sphinx-doc.org/en/stable/rest.html>`_

    .. revealjs:: Sphinx Basics
        :subtitle: 2/3

        .. code-block:: rst

            Unsorted list
            =============

            * Item 1
            * Item 2

                * Item 2.1

            * Item 2

            Sorted list
            ===========

            #. Item 1
            #. Item 2

        .. rv_small::

            Sphinx documentation: `reStructuredText Primer <http://www.sphinx-doc.org/en/stable/rest.html>`_

    .. revealjs:: Sphinx Basics
        :subtitle: 3/3

        .. code-block:: rst

            Source Code
            ===========
            Just use two of it::

                def func(me):
                    return me

            Or for more details:

            .. code-block:: python
                :linenos:
                :emphasize-lines: 1,3

                def func(a, b):
                    c = a + b
                    return c

        .. rv_small::

            Sphinx documentation: `Showing code examples <http://www.sphinx-doc.org/en/stable/markup/code.html>`_


