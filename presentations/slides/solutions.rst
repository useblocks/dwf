.. revealjs::

    .. revealjs:: Documentation = Code
        :subtitle: Same requirements for code and documentation

        * Editable inside IDE (text, images, diagrams, everything!)
        * Text based files
        * Stored and versioned beside the code
        * Deeply linked with code (e.g. reuse of docstrings)
        * Focused on information and not on layout or design


    .. revealjs:: Example

            .. code-block:: rst

                My code document
                ================

                This little piece of text describes the function :ref:`my_package.my_module.my_class.my_func`.

                Docstring
                ---------

                .. autofunction:: my_package.my_module.my_class.my_func

                Inheritance diagram
                -------------------

                .. inheritance-diagram:: my_package.my_module.my_class

                Code example
                ------------

                You can use the function like this::

                    from my_package.my_module import my_class

                    test_class = my_class()
                    return_value = test_class.my_func(some_data)
