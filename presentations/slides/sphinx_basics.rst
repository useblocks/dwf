Sphinx Basics
-------------
Text 1/4
~~~~~~~~

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

.. container:: small

   Sphinx documentation: `reStructuredText Primer <http://www.sphinx-doc.org/en/stable/rest.html>`_

Lists 2/4
~~~~~~~~~

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

.. container:: small

   Sphinx documentation: `reStructuredText Primer <http://www.sphinx-doc.org/en/stable/rest.html>`_

Images & Tables 3/4
~~~~~~~~~~~~~~~~~~~

.. code-block:: rst

   Images
   ======

   .. image:: my_image.png
      :scale: 50%

   Tables
   ======

   =====  =====  =======
   A      B      A and B
   =====  =====  =======
   False  False  False
   True   False  False
   False  True   False
   True   True   True
   =====  =====  =======

.. container:: small

   Sphinx documentation: `reStructuredText Primer <http://www.sphinx-doc.org/en/stable/rest.html>`_

Code 4/4
~~~~~~~~

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

.. container:: small

   Sphinx documentation: `Showing code examples <http://www.sphinx-doc.org/en/stable/markup/code.html>`_


