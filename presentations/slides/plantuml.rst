.. revealjs::

    .. revealjs:: PlantUML

        Tool: `PlantUML <http://plantuml.com>`_

        Sphinx documentation: `sphinx-plantuml <https://pypi.python.org/pypi/sphinxcontrib-plantuml>`_

    .. revealjs:: PlantUML
        :subtitle: Class diagrams - Result

        .. image:: _static/plantuml_class.png



    .. revealjs:: PlantUML
        :subtitle: Class diagrams - Code

        .. rv_code::
            @startuml
                class user {
                    name
                    age
                    email
                    check_password()
                    send_email(message)
                }

                class domain
                class group
                class api_key
                class permission

                user --> domain
                user --> group
                user --> api_key
                user --> permission: 1:n
                group --> permission: 1:n
            @enduml

        .. rv_small::

            PlantUML documentation: `Class diagram <http://plantuml.com/class-diagram>`_


    .. revealjs:: PlantUML
        :subtitle: Sequence diagrams - Result

        .. image:: _static/plantuml_sequence.png

    .. revealjs:: PlantUML
        :subtitle: Sequence diagrams - Code

        .. rv_code::

            @startuml
                user --> server : send request
                server --> server: check request
                server --> database: ask for data
                database --> server: provide data
                server --> server: render data
                server --> user: send rendered data
            @enduml

        .. rv_small::

            PlantUML documentation: `Sequence diagram <http://plantuml.com/sequence-diagram>`_

    .. revealjs:: PlantUML
        :subtitle: PyCharm Integration

        .. image:: _static/pycharm_plantuml.png

        .. rv_small::

            Plugin: `IntelliJ PlantUML Integration <https://plugins.jetbrains.com/plugin/7017-plantuml-integration>`_