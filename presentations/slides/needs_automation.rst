Sphinx-Needs Automation
-----------------------

Dynamic Functions
~~~~~~~~~~~~~~~~~

.. code-block:: rst

   .. story:: Dynamic Functions
      :id: US_DF
      :status: open
      :linked_status: [[copy("status", 'US_002')]]

      This need has the id **[[copy("id")]]** and status **[[copy("status")]]**.

.. story:: Dynamic Functions
   :id: US_DF
   :status: open
   :linked_status: [[copy("status", 'US_002')]]

   This need has the id **[[copy("id")]]** and status **[[copy("status")]]**.

.. container:: small

   | Sphinx-Needs: `Dynamic Functions <https://sphinxcontrib-needs.readthedocs.io/en/latest/dynamic_functions.html>`_

Global Options
~~~~~~~~~~~~~~

.. code-block:: rst

   needs_global_options = {
       'global_option': 'Fix value',
       'author': ('Marco', '"security" in tags', 'Daniel)
       'status':[
            ('closed', 'status.lower() in ["done", "resolved", "closed"]'),
            ('open', 'status.lower() in ["open", "new"]')
       ]
   }



.. container:: small

   | Sphinx-Needs: `needs_global_options <https://sphinxcontrib-needs.readthedocs.io/en/latest/configuration.html#needs-global-options>`_

Warnings
~~~~~~~~

.. code-block:: rst

    def my_custom_warning_check(need, log):
        if need["status"] == "open":
            log.info(f"{need['id']} status must not be 'open'.")
            return True
        return False

    needs_warnings = {
        'invalid_status' : "status not in ['open', 'closed']",
        'type_match': my_custom_warning_check,
    }

Build log:

.. code-block:: text

   Checking sphinx-needs warnings
     type_match: passed
     invalid_status: failed
         failed needs: 2 (US_001, US_002)
         used filter: status not in ['open', 'closed']

.. container:: small

   | Sphinx-Needs: `needs_warnings <https://sphinxcontrib-needs.readthedocs.io/en/latest/configuration.html#needs-warnings>`_

Template 1/2
~~~~~~~~~~~~

.. container:: small

   ``/my_file.rst``

.. code-block:: text

   .. spec:: My specification
      :id: TEMPL_POST_SPEC
      :links: US_003, US_004
      :post_template: post_template

      This is my **specification** content.

.. container:: small

   ``/needs_templates/post_template.need``

.. code-block:: rst

   **Analytics for above need:** {{title}}

   .. needflow::
      :filter: id == '{{id}}' or '{{id}}' in links_back


.. container:: small

   | Sphinx-Needs: `post_template <https://sphinxcontrib-needs.readthedocs.io/en/latest/directives/need.html#post-template>`_

Template 2/2
~~~~~~~~~~~~

.. spec:: My specification
   :id: TEMPL_POST_SPEC
   :links: US_003, US_004
   :post_template: post_template

   This is my **specification** content.

Debug Layout 1/2
~~~~~~~~~~~~~~~~

.. code-block:: rst

   .. story:: Debug
      :id: US_DEBUG
      :status: open
      :layout: debug

.. story:: Debug
   :id: US_DEBUG
   :status: open
   :layout: debug

.. container:: small

   | Sphinx-Needs: `Debug Layout <https://sphinxcontrib-needs.readthedocs.io/en/latest/layout_styles.html#EX_DEBUG>`_


Debug Layout 2/2
~~~~~~~~~~~~~~~~

.. code-block:: rst

   .. needflow::
      :filter: id == 'TEMPL_POST_SPEC' or 'TEMPL_POST_SPEC' in links_back
      :debug:

.. container:: small

   | Sphinx-Needs: `needflow debug <https://sphinxcontrib-needs.readthedocs.io/en/latest/directives/needflow.html#needflow-debug>`_

.. needflow::
   :filter: id == 'TEMPL_POST_SPEC' or 'TEMPL_POST_SPEC' in links_back
   :debug:

