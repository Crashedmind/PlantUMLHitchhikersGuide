*******************************************************************************
Standardising Standard Library 
*******************************************************************************



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

DefaultArgumentValue_

"In both procedure and return functions, you can define default values for arguments"
    The `default argument <https://plantuml.com/en/preprocessing#ajlk3nchu0zkka0ybjng>`__
    value can help to simplify definitions
    
    There are also now `dynamic invocation <https://plantuml.com/en/preprocessing#mr9qytp1zez3ka0ybjov>`__
    which may be useful
