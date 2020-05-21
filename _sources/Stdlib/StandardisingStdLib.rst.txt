.. _FunctionPointer: https://www.geeksforgeeks.org/function-pointer-in-c/

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



Step-by-step Towards A Standard Macro
===============================================================================


.. uml:: ProcedureBuildup.puml
    :align: center
    :caption: *each output is numbered to match the procedure e.g. 51 is output for ffoo51()* 


.. literalinclude:: ProcedureBuildup.puml
    :linenos: 


Close But... 
===============================================================================

We can use the DefaultArgumentValue_ to avoid having to specify a parameter value when we call our procedure.
BUT this only works if the default parameters are at the end i.e. it is all based on the order of the procedure parameters.

*In other words, the user has to know/care about the order of parameters.*

.. todo ::
    add ref to reqs

To specify color blue I need to do

```$ffoo6("myaliasbatch2", "mydescription", "mylabel", "mytechnology", 2, blue)```

What I want to do 
```$ffoo6($color=blue)```
or 
```$ffoo6($scale=2)```


Procedure Keyword Arguments
===============================================================================


To enable the StdLib standardisation, I suggested the *keyword arguments* and Arnaud produced a release to play with next day - and this became part of an official release:


.. uml:: pre-processing.puml
    :align: center
    :caption: *each output is numbered to match the procedure e.g. 51 is output for ffoo51()* 


.. literalinclude:: pre-processing.puml
    :linenos: 



Extensibility
===============================================================================

So now we have a way for the user to specify any or all of the sprite parameters.

But what happens if we want to add new parameters in the future?

Option 1: Reserve Parameters
-------------------------------------------------------------------------------
One option is to reserve parameters in the procedure definition:


.. code-block:: 

    !unquoted procedure $SpriteDecorator($MySprite, $alias, $description="", $label="", $technology="", $scale=1, $colour="red", $res1="", $res2="", $res3="", $res4="")

and used a function/procedure to map the new parameter feature to a reserved word.

We're not smart enough to predict the future, and we don't want to impose limits, so we won't be doing this. 

Option 2: Dynamic Invocation
-------------------------------------------------------------------------------

As a user I want to be able to call a procedure to draw an icon - and not have to change my code if new functionality is added in the future.
But I would like to benefit from the new features.

This type of thing can be done in e.g. C code, using a FunctionPointer_ i.e. if I had different functions with different parameters, I could pass any of these as a parameter (pointer to that function) to another function, for that function to call.

This gives a level of abstraction / separation between the user code, and the library code.




Backwards Compatiblity
===============================================================================