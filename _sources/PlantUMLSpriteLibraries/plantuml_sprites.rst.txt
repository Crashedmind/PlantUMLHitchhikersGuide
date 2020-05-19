.. _Deployment: https://plantuml.com/deployment-diagram
.. _creole: https://plantuml.com/creole
.. _sprites: http://plantuml.com/sprite


======================================================
Use Images in Diagrams
======================================================

.. tip ::

    Given we want diagrams that communicate quickly and clearly, using images (rather than just shapes) is very effective.

    To add an image to a PlantUML diagram, we can: 

    #. use an image (jpg, png, etc...) 
    #. use Deployment_ diagram elements
    #. use sprites 

        #. the builtin sprites_ 
        #. create our own sprites_

Let's look at all of these in detail.

.. note ::
    For clarity, sprites will be referred to as icons.
    Image formats, like png, jpg will be referred to as image files.


Images
===============================================================================

Add Images To A Diagram
-------------------------------------------------------------------------------


This uses the image tag which is part of PlantUML creole_ Legacy HTML support per PlantUML specification:

.. code-block:: 

    Some HTML tags are also working:

        <b> for bold text
        <u> or <u:#AAAAAA> or <u:[[color|colorName]]> for underline
        <i> for italic
        <s> or <s:#AAAAAA> or <s:[[color|colorName]]> for strike text
        <w> or <w:#AAAAAA> or <w:[[color|colorName]]> for wave underline text
        <color:#AAAAAA> or <color:[[color|colorName]]>
        <back:#AAAAAA> or <back:[[color|colorName]]> for background color
        <size:nn> to change font size
        <img:file> : the file must be accessible by the filesystem
        <img:http://plantuml.com/logo3.png> : the URL must be available from the Internet

.. BeginPlayingExample 
    pumlsource: ./image.puml
    emphasize-lines: 9
    caption: Adding a PNG image to a diagram
    explore: Change the image to one you select from a different URL.
    explore: Change the foreground or background color of the image.
    explore: Change the size of the image.
    explore: How would you share a PlantUML diagram with images in it for another user to edit?

.. uml:: ./image.puml
    :align: center

.. literalinclude:: ./image.puml
    :linenos:
    :emphasize-lines: 9

.. EndPlayingExample


Connect Images In A Diagram
-------------------------------------------------------------------------------

.. todo ::
    Connect Images In A Diagram



Deployment Diagram Elements
===============================================================================

Review The Deployment Diagram Elements
-------------------------------------------------------------------------------
PlantUML supports sprites_ small graphic elements that can be used in diagrams.

Deployment_ diagrams define several sprites.


.. BeginPlayingExample 
    pumlsource: ./deployment_diagram.puml
    emphasize-lines:
    caption: Deployment diagram elements
    explore: Change the 
    
.. uml:: ./deployment_diagram.puml
    :align: center

.. literalinclude:: ./deployment_diagram.puml
    :linenos:
    

.. EndPlayingExample


Use The Deployment Diagram Elements In A Sequence Diagram
-------------------------------------------------------------------------------

Below is an example using some of these - in a sequence diagram.

.. BeginPlayingExample 
    pumlsource: ./keysequence.puml
    emphasize-lines:
    caption: Adding a PNG image to a diagram
    explore: Change the 
    explore: Change the foreground or background color of the image.


.. uml:: ./keysequence.puml
    :align: center

.. literalinclude:: ./keysequence.puml
    :linenos:
    :emphasize-lines: 4, 5, 6, 7, 9, 18, 20

.. EndPlayingExample

In this diagram, we're using some PlantUML keywords:

#. autonumber: to automatically number the sequence steps
#. box: to highlight domains: trusted in green, untrusted in green
#. group: to group sequence flows. And these can be grouped within other groups.


Standard Library Sprites
===============================================================================

PlantUML includes a Standard Library. Contents of the library come from third party contributors.

#. See http://plantuml.com/stdlib for what is supported in official release of PlantUML
#. "-stdlib" option lists the builtin icon libaries


.. code-block:: 

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


So Why Do I Need Sprites?
-------------------------------------------------------------------------------

Sprites are monochrome (16 shades/levels max), versus image files which can be infinite color at high resolution.

But we can easily change a sprite's characteristics via PlantUML e.g. color and scale.


Example Builtin Sprites AWS
-------------------------------------------------------------------------------

`Plantuml for AWS <https://github.com/milo-minderbinder/AWS-PlantUML>`__
uses the `icon set from
AWS <https://aws.amazon.com/architecture/icons/>`__ and converts these
to sprites for use with PlantUML.

::

    https://github.com/plantuml/plantuml-stdlib/tree/master/aws


.. note ::

    AWS-labs has since updated the AWS icons, and submitted a new icon set to PlantUML.

    ::

        https://github.com/plantuml/plantuml-stdlib/tree/master/awslib 

Simple Example
-------------------------------------------------------------------------------

.. BeginPlayingExample 
    pumlsource: ./aws_nested-components.puml
    emphasize-lines:
    caption: Simple AWS Example
    explore: 
    EndPlayingExample

.. uml:: ./aws_nested-components.puml
    :align: center

.. literalinclude:: ./aws_nested-components.puml
    :linenos:


More Complex Example
-------------------------------------------------------------------------------

.. BeginPlayingExample 
    pumlsource: ./aws_comments-architecture.puml
    emphasize-lines:
    caption: Simple AWS Example
    explore: 
    EndPlayingExample

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

Start With a Png Image
-------------------------------------------------------------------------------

Here we use a 100x100 person icon 

.. figure:: ./C4person100.png
   

Convert to sprite of different resolutions as follows
-------------------------------------------------------------------------------

You can use the PlantUML GUI as described in sprites_, or use the command line:

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
   





.. todo ::
    look later at some more exotic options
        https://github.com/executablebooks/sphinx-panels
        https://sphinx-book-theme.readthedocs.io/en/latest/launch.html
        https://stackoverflow.com/questions/20303335/ipython-notebook-plantuml-extension