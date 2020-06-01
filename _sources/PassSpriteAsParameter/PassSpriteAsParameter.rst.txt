******************************************************
PassSpriteAsParameter
******************************************************



.. _MigrationNotes: https://plantuml.com/preprocessing#ajlk3nchu0zkka0ybjng
.. _DefaultArgumentValue: https://plantuml.com/preprocessing#ae1b47605326b65f






Understand How To Pass A Sprite To A Procedure
===============================================================================

.. uml:: option1.puml
    :align: center

Source
-------------------------------------------------------------------------------

.. literalinclude:: ./option1.puml
    :emphasize-lines: 12, 16
    :linenos: 






Understand How To Pass A Sprite To A Procedure - using unquoted keyword
===============================================================================
This option uses the unquoted keyword. The caller of the procedure does not need 
to add quotes when calling the procedure.


.. uml:: option2.puml
    :align: center
    

Source
-------------------------------------------------------------------------------

.. literalinclude:: ./option2.puml
    :emphasize-lines: 12, 16
    :linenos: 







Use Procedure Defaults 
===============================================================================

And Tidy Up The Procedure So It's Easier To Read

.. uml:: option3.puml
    :align: center
    :caption: *blah* 

Source
-------------------------------------------------------------------------------

.. literalinclude:: ./option3.puml
    :emphasize-lines: 12, 22
    :linenos: 




So What?
===============================================================================
We said previously that the current stdlib macros are largely the same across files - changing for each icon.

So now we have a way to define a procedure(s) in one place, and pass an icon.




