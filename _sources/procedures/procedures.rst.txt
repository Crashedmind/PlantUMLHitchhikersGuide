
.. _procedures-label:


******************************************************
Procedures
******************************************************


.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _listsprites: https://plantuml.com/#
.. _together: https://forum.plantuml.net/4387/please-provide-together-keyword-group-diagram-nodes-together




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

.. note ::
    There is also `dynamic invocation <https://plantuml.com/en/preprocessing#mr9qytp1zez3ka0ybjov>`__ which may be useful. 
    I think of this as like C function pointers which are very useful.




Keyword Arguments
===============================================================================




https://plantuml.com/news
*17 May, 2020: Use keyword arguments with the preprocessor (V1.2020.10). (Thanks to Crashedmind for the suggestion !)*

