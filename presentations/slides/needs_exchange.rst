Sphinx-Needs Data Exchange
--------------------------


Export
~~~~~~

.. code-block::

   make needs

.. code-block::

   # File: _build/needs/needs.json
   {
       "created": "2017-09-21T20:40:49.090464",
       "current_version": "1.0",
       "project": "Documentation without Frustration",
       "versions": {
           "1.0": {
               "created": "2017-09-21T20:40:49.090443",
               "needs": {
                   "SP_002": {
                       "description": "",
                       "id": "SP_001",
                       "links": [
                           "US_002"
                       ],
                       "status": null,
                       "tags": [
                           "user"
                       ],
                       "title": "Use flask-login for secure user verification and authorisation",
                       "type": "spec",
                       "type_name": "Specification"
                   },
                   "US_002": {
                       "description": "We need to use the unique email address for user login and verification\n\n.. uml::\n\n         @startuml\n         rectangle Alice\n         rectangle Bob\n         Alice -right-> Bob\n         @enduml",
                       "id": "US_002",
                       "links": [],
                       "status": null,
                       "tags": [
                           "user",
                           "login",
                           "email"
                       ],
                       "title": "As user I want to be able to use my email address for login",
                       "type": "story",
                       "type_name": "User Story"
                   }
               },
               "needs_amount": 2
           }
       }
   }

.. container:: small

   Sphinx-Needs documentation: `Builders <http://sphinxcontrib-needs.readthedocs.io/en/latest/builders.html>`_

Import
~~~~~~

.. code-block::

   .. needimport:: /needs.json
      :id_prefix: IMP_
      :version: 1.0
      :tags: imported
      :filter: "SP" in id

.. needimport:: /needs.json
  :id_prefix: IMP_
  :tags: imported
  :filter: "SP" in id

.. container:: small

   Sphinx-Needs documentation: `needimport <http://sphinxcontrib-needs.readthedocs.io/en/latest/directives.html#needimport>`_

External Needs
~~~~~~~~~~~~~~

.. code-block:: python

   needs_external_needs = [
       {
           'base_url': 'http://mydocs/my_project',
           'json_url':  'http://mydocs/my_project/needs.json',
           'version': '1.0',
           'id_prefix': 'ext_',
           'css_class': 'external_link',
       }
   ]


.. container:: small

   Sphinx-Needs documentation: `needs_external_needs <https://sphinxcontrib-needs.readthedocs.io/en/latest/configuration.html#needs-external-needs>`_

Services
~~~~~~~~

.. code-block:: rst

   .. needservice:: github-issues
      :query: repo:useblocks/sphinxcontrib-needs state:closed needtable viewports
      :max_amount: 1

.. needservice:: github-issues
   :query: repo:useblocks/sphinxcontrib-needs state:closed needtable viewports
   :max_amount: 1

.. container:: small

   Sphinx-Needs documentation: `GitHub service <https://sphinxcontrib-needs.readthedocs.io/en/latest/services/github.html>`_



Sphinx-Needs-Enterprise
~~~~~~~~~~~~~~~~~~~~~~~

Ready to use Ex- and Importers:

.. container:: small

    Azure DevOps, codebeamer, Jira, Elasticsearch

Supported targets:

.. container:: small

   Documentation build, ``needs.json`` file

`Sphinx-Needs Enterprise <https://useblocks.com/sphinx-needs-enterprise/>`_