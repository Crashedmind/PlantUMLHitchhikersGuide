

.. _Deployment: https://plantuml.com/deployment-diagram

======================================================
Plantuml Sprites
======================================================
PlantUML supports `sprites: <http://plantuml.com/sprite>`_ small graphic elements that can be used in diagrams.
   
Given we want to make diagrams communicate quickly and clearly, using sprites (rather than just boxes) is very effective.

You can 

#. use the builtin  `sprites <http://plantuml.com/sprite>`_
#. create your own sprites


.. todo ::
    add note about png files


Builtin Sprites - Deployment Diagram Sprites
===============================================================================

Deployment_ diagrams define several sprites.

Below is an example using some of these - in a sequence diagram.

.. uml:: ./keysequence.puml
    :align: center

.. literalinclude:: ./keysequence.puml
    :linenos:


Builtin Sprites - Standard Library Sprites
===============================================================================

Some standard libaries are available for PlantUML:

#. See http://plantuml.com/stdlib for what is supported in official release of PlantUML
#. "-stdlib" option lists the builtin icon libaries

.. code ::

    aws
    Version 18.02.22
    Delivered by https://github.com/milo-minderbinder/AWS-PlantUML
    
    awslib
    Version 3.0.0
    Delivered by https://github.com/awslabs/aws-icons-for-plantuml
    
    azure
    Version 2.1.0
    Delivered by https://github.com/RicardoNiepel/Azure-PlantUML
    
    c4
    Version 1.0.0
    Delivered by https://github.com/RicardoNiepel/C4-PlantUML
    
    cloudinsight
    Version 0.0.1
    Delivered by https://github.com/rabelenda/cicon-plantuml-sprites/
    
    cloudogu
    Version 0.0.1
    Delivered by https://github.com/cloudogu/plantuml-cloudogu-sprites
    
    material
    Version 0.0.1
    Delivered by https://github.com/Templarian/MaterialDesign
    
    office
    Version 0.0.1
    Delivered by https://github.com/Roemer/plantuml-office
    
    osa
    Version 0.0.1
    Delivered by https://github.com/Crashedmind/PlantUML-opensecurityarchitecture-icons
    
    tupadr3
    Version 2.0.0
    Delivered by https://github.com/tupadr3/plantuml-icon-font-sprites



Example Builtin Sprites AWS
-------------------------------------------------------------------------------

`Plantuml for AWS <https://github.com/milo-minderbinder/AWS-PlantUML>`__
uses the `icon set from
AWS <https://aws.amazon.com/architecture/icons/>`__ and converts these
to sprites for use with PlantUML.

::

    git clone git@github.com:milo-minderbinder/AWS-PlantUML.git

Simple Example
-------------------------------------------------------------------------------

.. uml:: ./aws_nested-components.puml
    :align: center

.. literalinclude:: ./aws_nested-components.puml
    :linenos:
   

More Complex Example
-------------------------------------------------------------------------------

.. uml:: ./aws_comments-architecture.puml
    :align: center

.. literalinclude:: ./aws_comments-architecture.puml
    :linenos:
   



.. todo ::

    add note about scale - no need for different sizes
    redo this example with play explore etc...

Create a Sprite
===============================================================================

It's easy to create your own sprites from existing icons.

Start with a 100x100 person icon png
-------------------------------------------------------------------------------

.. figure:: ./C4person100.png
   

Convert to sprite of different resolutions as follows
-------------------------------------------------------------------------------


::

     java -jar plantuml.jar -encodesprite 4 images/C4person100.png > C4person4.sprite
     java -jar plantuml.jar -encodesprite 16 images/C4person100.png > C4person16.sprite
     java -jar plantuml.jar -encodesprite 8 images/C4person100.png > C4person8.sprite


C4person4.sprite file:

.. literalinclude:: ./C4person4.sprite
    :linenos:
   

Create Diagram with our Sprites
-------------------------------------------------------------------------------

.. uml:: ./bigsmall.puml
    :align: center

.. literalinclude:: ./bigsmall.puml
    :linenos:
   
