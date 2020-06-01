
.. _procedures-label:


******************************************************
Procedures and Keyword Arguments
******************************************************


.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _listsprites: https://plantuml.com/#
.. _together: https://forum.plantuml.net/4387/please-provide-together-keyword-group-diagram-nodes-together
.. _MigrationNotes: https://plantuml.com/preprocessing#ajlk3nchu0zkka0ybjng
.. _DefaultArgumentValue: https://plantuml.com/preprocessing#ae1b47605326b65f


Defines Are Deprecated
===============================================================================

Existing stdlib icon libraries use !define and !definelong to create different macros.

.. tip ::

    !function and !procedure should be used instead of !define and !definelong

    Per MigrationNotes_: 

        *You should not use !define and !definelong anymore. Use !function, !procedure 
        or variable definition instead.*

        *!define should be replaced by return !function*

        *!definelong should be replaced by !procedure.*



Default Values
===============================================================================

Per DefaultArgumentValue_, "In both procedure and return functions, you can define default values for arguments"

.. tip ::
    The `default argument <https://plantuml.com/en/preprocessing#ajlk3nchu0zkka0ybjng>`__ value can help to simplify definitions


.. uml:: defaultArgument.puml
    :align: center
    :caption: *Using default argument* 


.. literalinclude:: defaultArgument.puml
    :linenos: 
    :emphasize-lines: 2,6,7



Keyword Arguments
===============================================================================

Current macros are polymorphic e.g. macros are defined twice with a different number of arguments.

However, the ordering of the arguments is hardcoded e.g. first parameter is "alias".

This has a number of issues:

#. if the user wants to specify the 5th parameter only, they need to specify the first 4 also.
#. if we want to add new parameters in the future, then we need to add them at the end - adding maybe more macros to do so.

Keyword Arguments allow the user to specify what they care about, and the procedure uses defaults for other parameters.
It also gives extensibility.


See :ref:`Step-by-step Towards A Standard Macro` for the under-the-hood work that led towards the following release.

https://plantuml.com/news
*17 May, 2020: Use keyword arguments with the preprocessor (V1.2020.10). (Thanks to Crashedmind for the suggestion !)*

