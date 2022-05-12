Sphinx-Needs Structure
----------------------

Embedded needs 1/2
~~~~~~~~~~~~~~~~~~

.. code-block:: rst

   .. story:: My parent story
      :id: ST_PAR_001

      This parent need contains the following need:

      .. story:: My child story
         :id: ST_CHIlD_001
         :style: red_border

         This is the child need.

Embedded needs 2/2
~~~~~~~~~~~~~~~~~~

.. story:: My parent story
   :id: ST_PAR_001

   This parent need contains the following need:

   .. story:: My child story
      :id: ST_CHIlD_001
      :style: red_border

      This is the child need.

Need parts 1/2
~~~~~~~~~~~~~~

.. code-block:: rst

   .. story:: A Story with parts
      :id: ST_PARTS_001
      :links: ST_PARTS_001.1, ST_PARTS_001.nothing

      As awesome user I want to:

      * :need_part:`(1)Get everything`
      * :np:`(nothing)Be responsible for nothing`


Need parts 2/2
~~~~~~~~~~~~~~


.. story:: A Story with parts
   :id: ST_PARTS_001
   :links: ST_PARTS_001.1, ST_PARTS_001.nothing

   As awesome user I want to:

   * :need_part:`(1)Get everything`
   * :np:`(nothing)Be responsible for nothing`

