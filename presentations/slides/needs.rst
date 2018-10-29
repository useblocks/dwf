.. revealjs::

    .. revealjs:: Sphinx-Needs

        .. image:: _static/needs_logo_big.png
            :height: 300px
            :class: needs_logo

        Extension to manage requirements, specifications or test cases

        Can be configured to support other types.
        Like user stories, bugs, servers, ...

        Developed to support `ISO 26262 <https://en.wikipedia.org/wiki/ISO_26262>`_ inside Sphinx

        .. rv_small::

            Sphinx Documentation: `Sphinx-needs <http://sphinxcontrib-needs.readthedocs.io/en/latest/>`_

    .. revealjs:: Sphinx-Needs
        :subtitle: Need-Objects Code

        .. rv_code::

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

        .. rv_small::

            Sphinx-Needs documentation: `need/ req (or any other defined need type) <http://sphinxcontrib-needs.readthedocs.io/en/latest/directives.html#need-req-or-any-other-defined-need-type>`_

    .. revealjs:: Sphinx-Needs
        :subtitle: Need-Objects Result

        .. story:: As user I want to be able to use my email address for login
           :id: US_001
           :tags: user; login; email, security

           We need to use the unique email address for user login and verification

           .. image:: _static/needs_alice_bob..png

        .. spec:: Use flask-login for secure user verification and authorisation
               :tags: user, security
               :id: SP_001
               :links: US_001

    .. revealjs:: Sphinx-Needs
        :subtitle: Need-Objects Filtering

        As list

        .. rv_code::

            .. needfilter::
                :tags: security

        .. needfilter::
            :tags: security

        .. rv_small::

            Sphinx-Needs documentation: `needfilter <http://sphinxcontrib-needs.readthedocs.io/en/latest/directives.html#needfilter>`_

    .. revealjs:: Sphinx-Needs
        :subtitle: Need-Objects Filtering with complex filter

        As table

        .. rv_code::

            .. needfilter::
                :filter: id == "US_001" or "security" in tags
                :layout: table

        .. needfilter::
            :filter: id == "US_001" or "security" in tags
            :layout: table

    .. revealjs:: Sphinx-Needs
        :subtitle: Need-Objects Filtering with regex

        As diagram

        .. rv_code::

            .. needfilter::
                :filter: search("\w{5,}", title) and "security" in tags  # word with at least 5 chars inside title
                :layout: diagram

        .. image:: _static/need_diagram_filter.png

    .. revealjs:: Sphinx-Needs
        :subtitle: Export

        .. rv_code::

            make needs

        .. rv_code::

            # File: _build/needs/needs.json
            {
                "created": "2017-09-21T20:40:49.090464",
                "current_version": "1.0",
                "project": "Documentation without Frustration",
                "versions": {
                    "1.0": {
                        "created": "2017-09-21T20:40:49.090443",
                        "needs": {
                            "SP_001": {
                                "description": "",
                                "id": "SP_001",
                                "links": [
                                    "US_001"
                                ],
                                "status": null,
                                "tags": [
                                    "user"
                                ],
                                "title": "Use flask-login for secure user verification and authorisation",
                                "type": "spec",
                                "type_name": "Specification"
                            },
                            "US_001": {
                                "description": "We need to use the unique email address for user login and verification\n\n.. uml::\n\n         @startuml\n         rectangle Alice\n         rectangle Bob\n         Alice -right-> Bob\n         @enduml",
                                "id": "US_001",
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

        .. rv_small::

            Sphinx-Needs documentation: `Builders <http://sphinxcontrib-needs.readthedocs.io/en/latest/builders.html>`_

    .. revealjs:: Sphinx-Needs
        :subtitle: Import

        .. rv_code::

            .. needimport:: needs.json
               :id_prefix: IMP_
               :version: 1.0
               :tags: imported
               :filter: "UST" in id

        .. needimport:: needs.json
           :id_prefix: IMP_
           :tags: imported
           :filter: id == "SP_001"

        .. rv_small::

            Sphinx-Needs documentation: `needimport <http://sphinxcontrib-needs.readthedocs.io/en/latest/directives.html#needimport>`_
