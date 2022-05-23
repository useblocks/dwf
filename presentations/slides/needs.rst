Sphinx-Needs
------------

.. image:: _static/sphinx-needs-logo-bg.svg
   :height: 300px
   :class: needs_logo

.. revealjs-break::
   :notitle:

Extension to manage requirements, specifications or test cases

Can be configured to support other types.
Like user stories, bugs, servers, ...

Developed to support `ISO 26262 <https://en.wikipedia.org/wiki/ISO_26262>`_ inside Sphinx

.. container:: small

   Sphinx Documentation: `Sphinx-needs <http://sphinxcontrib-needs.readthedocs.io/en/latest/>`_

Need-Objects
~~~~~~~~~~~~

.. story:: As user I want to be able to use my email address for login
  :id: US_001
  :tags: user; login; email, security

  We need to use the unique email address for user login and verification

  .. image:: /_static/needs_alice_bob..png

.. spec:: Use flask-login for secure user verification and authorisation
   :tags: user, security
   :id: SP_001
   :links: US_001

Need-Objects Code
~~~~~~~~~~~~~~~~~

.. code-block::

   .. story:: As user I want to be able to use my email address for login
      :id: US_001
      :tags: user; login; email, security

      We need to use the unique email address for user login and verification

      .. uml::

           object Alice
           object Bob
           Alice --> Bob

   .. spec:: Use flask-login for secure user verification and authorisation
       :tags: user, security
       :id: SP_001
       :link: US_001

.. container:: small

   Sphinx-Needs documentation: `need/ req (or any other defined need type) <http://sphinxcontrib-needs.readthedocs.io/en/latest/directives.html#need-req-or-any-other-defined-need-type>`_



Need-Objects Filtering
~~~~~~~~~~~~~~~~~~~~~~

As list

.. code-block::

   .. needlist::
      :tags: security

.. needlist::
   :tags: security

.. container:: small

   Sphinx-Needs documentation: `needfilter <http://sphinxcontrib-needs.readthedocs.io/en/latest/directives.html#needfilter>`_

Need-Objects Filtering with complex filter
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

As table

.. code-block::

   .. needtable::
      :filter: id == "US_001" or "security" in tags
      :columns: id, title, outgoing
      :layout: table

.. needtable::
   :filter: id == "US_001" or "security" in tags
   :columns: id, title, outgoing
   :style: table

Need-Objects Filtering with regex
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

As diagram

.. code-block::

   .. needflow::
      :filter: search("\w{5,}", title) and "security" in tags  # word with at least 5 chars inside title

.. image:: /_static/need_diagram_filter.png

Other filter result types
~~~~~~~~~~~~~~~~~~~~~~~~~

This presentation has :need_count:`status == "open"` open needs.

.. code-block:: rst

   This presentation has :need_count:`status == "open"` open needs.

.. image:: /_static/need_sequence.svg
   :scale: 30%

.. image:: /_static/need_gantt.svg
   :scale: 30%

.. image:: /_static/need_bar.png
   :scale: 30%


.. container:: small

   Docs: |
   `need_count <https://sphinxcontrib-needs.readthedocs.io/en/latest/roles.html#need-count>`_ |
   `needsequence <https://sphinxcontrib-needs.readthedocs.io/en/latest/directives/needsequence.html>`_ |
   `needgantt <https://sphinxcontrib-needs.readthedocs.io/en/latest/directives/needgantt.html>`_ |
   `needbar <https://sphinxcontrib-needs.readthedocs.io/en/latest/directives/needbar.html>`_