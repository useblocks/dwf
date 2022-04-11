Sphinx-Needs Customization
--------------------------

Types
~~~~~

.. code-block:: rst

   needs_types = [
       dict(
           directive="req",
           title="Requirement",
           prefix="R_",
           color="#BFD8D2",
           style="node"
       ),
       dict(directive="spec", title="Specification", prefix="S_", color="#FEDCD2", style="node"),
   ]

.. container:: small

   | Sphinx-Needs: `Need Types <https://sphinxcontrib-needs.readthedocs.io/en/latest/configuration.html#needs-types>`_
   | PlantUML: `Styles <https://plantuml.com/deployment-diagram>`_




Links
~~~~~

.. code-block:: rst

   needs_extra_links = [
       {
          "option": "triggers",
          "incoming": "is triggered by",
          "outgoing": "triggers",
          "copy": False,
          "allow_dead_links": True,
          "style": "#00AA00"
          "style_part": "#00AA00"
          "style_start": "-",
          "style_end": "--o",
       }
    ]

.. container:: small

   | Sphinx-Needs: `Need Links <https://sphinxcontrib-needs.readthedocs.io/en/latest/configuration.html#needs-extra-links>`_
   | PlantUML: `Line styles <https://plantuml.com/deployment-diagram#b5f6831632fd63c1>`_



Layout
~~~~~~

.. code-block:: rst

   .. story:: Layout example
      :layout: complete

   .. story:: Layout example
      :layout: focus


.. story:: Layout example
   :id: US_002
   :status: closed
   :links: US_003
   :layout: complete

   Some content

.. story:: Layout example
   :id: US_003
   :status: open
   :links: US_002
   :layout: focus_l

   Some content




.. container:: small

   | Sphinx-Needs: `Layouts <https://sphinxcontrib-needs.readthedocs.io/en/latest/layout_styles.html#layouts>`_


Styles
~~~~~~

.. story:: Style example
   :id: US_004
   :layout: focus_l
   :style: red

   ``:style: red``

.. story:: Style example
   :id: US_005
   :layout: focus_l
   :style: green_border

   ``:style: green_border``

.. story:: Style example
   :id: US_006
   :layout: focus_l
   :style: discreet

   ``:style: discreet``

.. story:: Style example
   :id: US_007
   :layout: focus_l
   :style: yellow, blue_border

   ``:style: yellow, blue_border``

.. container:: small

   | Sphinx-Needs: `Styles <https://sphinxcontrib-needs.readthedocs.io/en/latest/layout_styles.html#styles>`_