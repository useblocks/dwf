.. revealjs::

    .. revealjs:: Documentation = Code
        :subtitle: Integrated Development Environment

        .. image:: _static/code_ide.png


    .. revealjs:: Documentation = Code
        :subtitle: Same requirements for code and documentation

        * Editable inside IDE (text, images, diagrams, everything!)
        * Text based files
        * Stored and version-controlled beside the code
        * Deeply linked with code (e.g. reuse of docstrings)
        * Focused on information and not on layout or design



    .. revealjs:: Example

        .. code-block:: rst

            My code document
            ================

            This little piece of text describes the function
            :ref:`my_package.my_module.my_class.my_func`.

            Docstring
            ---------

            .. autofunction:: my_package.my_module.my_class.my_func

            Inheritance diagram
            -------------------

            .. inheritance-diagram:: my_package.my_module.my_class

            Code example
            ------------

            You can use the function like this::

                test_class = MyClass()
                return_value = test_class.my_func(some_data)

