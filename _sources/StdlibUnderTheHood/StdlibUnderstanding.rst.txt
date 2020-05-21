.. _understandingstdlib-label:

*******************************************************************************
PlantUML Stdlib Under The Hood
*******************************************************************************


.. tip ::

    Below are the steps I took to understand the PlantUML Standard Library Macros.
    
    * It's a step-by-step in the dark - taking small validated steps.
    * The steps are listed here because it's educational and interesting.
    * **You should not, and don't have to, follow these steps.** 
    * Based on the understanding gained, there's a better way to go.

    **So you can skip this chapter and go straight to todo**
    

.. todo ::
    add ref to new way


Goal
===============================================================================

#. Look under the hood of the generated plantuml icon files from
   https://github.com/awslabs/aws-icons-for-plantuml to understand them
   better - from first principles e.g.
   https://github.com/awslabs/aws-icons-for-plantuml/blob/master/dist/Compute/Batch.puml
#. To confirm understanding

    * a new bare-minimum macro will be created that requires only 1 parameter `!define Batch(e\_alias)`
    * a new macro will be added to allow scaling the icon size


Steps to Understanding
===============================================================================

Using the sprite directly
-------------------------------------------------------------------------------

"Batch" is defined in
https://github.com/awslabs/aws-icons-for-plantuml/blob/master/dist/Compute/Batch.puml)
ala

::

    sprite $Batch [64x64/16z] {...


.. uml:: ./1.puml
    :align: center


.. literalinclude:: ./1.puml
    :linenos:
    :emphasize-lines: 8,9




Add an “as whatever”
-------------------------------------------------------------------------------

.. uml:: ./2.puml
    :align: center


.. literalinclude:: ./2.puml
    :linenos:
    :emphasize-lines: 9,10    


Bare Minimum
-------------------

Extract the sprite from the Batch.puml

Note that plantuml needs the @startuml and @endumlto recognize the file
as a plantuml diagram i.e. it won’t work without these



.. uml:: ./3.puml
    :align: center


.. literalinclude:: ./3.puml
    :linenos:
    :emphasize-lines: 3-9



Bare Minimum by including Batch.puml
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The result is the same.

.. uml:: ./3.1.puml
    :align: center


.. literalinclude:: ./3.1.puml
    :linenos:
    :emphasize-lines: 4



Illegal Bare Minimum by including all.puml
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Note: This is not valid plantuml as it does not contain any elements. 

* The VSCode Plantuml extension will happily render this in preview mode. But VSCode Plantuml extension export will fail 
* Plantuml call will generate a blank output.

.. literalinclude:: ./3.2.puml
    :linenos:
    :emphasize-lines: 4

Listsprites
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Add the listsprites keyword

.. uml:: ./3.3.puml
    :align: center

.. literalinclude:: ./3.3.puml
    :linenos:
    :emphasize-lines: 6






Where did that guy come from?
------------------------------------

If any color is added we get an actor (from Deployment Diagram so can
explicitly use a rectangle as the Deployment Diagram entity - see next
example)

.. uml:: ./4.puml
    :align: center


.. literalinclude:: ./4.puml
    :linenos:
    :emphasize-lines: 12


Lose the guy - add a Deployment Diagram Rectangle Instead
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. uml:: ./4.1.puml
    :align: center


.. literalinclude:: ./4.1.puml
    :linenos:
    :emphasize-lines: 11

Add some color
---------------------

.. uml:: ./5.puml
    :align: center


.. literalinclude:: ./5.puml
    :linenos:
    :emphasize-lines: 9


Understanding the AWSEntity Macro
----------------------------------------

Based on reconstructing the existing Macros, we can define our own
minimal macro:

::

    !define Batch(e_alias) AWSEntity(Batch, #D86613) as e_alias

where the parameters are 

#. ```Batch``` this refers to the sprite $Batch 
#. ```e_alias``` this adds on a "as whatever" so multiple calls to same sprite return multiple rendered icons. 
#. ```#D86613``` is the color defined as part of the sprite puml file


.. uml:: ./6.puml
    :align: center


.. literalinclude:: ./6.puml
    :linenos:
    :emphasize-lines: 27-29

 



Add Scaling to AWSEntity Macro
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Replacing the last lines from the previous example to add scale.

.. uml:: ./6.1.puml
    :align: center


.. literalinclude:: ./6.1.puml
    :linenos:
    :emphasize-lines: 25-27


.. note ::
    This scale parameter could be added to existing macros in puml files e.g.
    https://github.com/awslabs/aws-icons-for-plantuml/blob/master/dist/Compute/Batch.puml

    But, for each macro (4 in this case), we would need to add a new macro that supports a scale parameter (giving 8 macros in total).
    
    This is not very extensible or future proof! 
    
    So we need to come up with a better way...

::

    !define Batch(e_alias, e_label, e_techn) AWSEntity(e_alias, e_label, e_techn, #D86613, Batch, Batch)
    !define Batch(e_alias, e_label, e_techn, e_descr) AWSEntity(e_alias, e_label, e_techn, e_descr, #D86613, Batch, Batch)
    !define BatchParticipant(p_alias, p_label, p_techn) AWSParticipant(p_alias, p_label, p_techn, #D86613, Batch, Batch)
    !define BatchParticipant(p_alias, p_label, p_techn, p_descr) AWSParticipant(p_alias, p_label, p_techn, p_descr, #D86613, Batch, Batch)

.. todo ::
    refine the scale, raw macros

Updating the puml files to support minimal macro
-------------------------------------------------------

Using AWSSimplified.puml as a reference, we can create an AWSBare.puml
file.

::

    ' Styling
    ' ##################################

    hide stereotype

    !definelong AWSEntityColoring(e_stereo)
    skinparam rectangle<<e_stereo>> {
        BackgroundColor AWS_BG_COLOR
        BorderColor transparent
        Shadowing false
    }
    !enddefinelong

    ' Overwriting Elements
    ' ##################################

    !definelong AWSEntity(e_sprite, e_color)
    rectangle "<color:e_color><$e_sprite></color>" 
    !enddefinelong

For each icon puml file e.g. Batch.puml

::


    !define Batch(e_sprite) AWSEntity(e_sprite, #D86613)

.. |image0| image:: awslabs.png
