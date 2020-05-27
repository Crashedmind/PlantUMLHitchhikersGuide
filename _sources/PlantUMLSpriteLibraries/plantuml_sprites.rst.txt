.. _Deployment: https://plantuml.com/deployment-diagram
.. _creole: https://plantuml.com/creole
.. _sprites: http://plantuml.com/sprite
.. _openIconic: https://plantuml.com/openiconic

======================================================
Use Images in Diagrams
======================================================

.. tip ::

    Given we want diagrams that communicate quickly and clearly, using images (rather than just shapes) is very effective.

    The following table lists the options to add an image to a PlantUML diagram.



.. csv-table:: Options to add images to PlantUML diagrams
   :header: "Option", "Builtin", "Details"
   :widths: 10, 10, 50
    
    "Deployment_ Diagram Elements", "Yes",	"These are ~20 shapes"
    "Creole openIconic_", "Yes", "e.g. <&person>, e.g. <&cloud>"
    "Standard Library sprites_", "Yes",	"These are part of PlantUML - but submitted by the community"
    "Create our own sprites_", "No",	"You can convert and use any image. You can also submit to PlantUML for inclusion in Standard Library"
    "Images", "No",	"jpg, png, etc... using <img>tag to add images you specify via file or URL"
    
Let's look at all of these in detail.

.. note ::
    For clarity, sprites will be referred to as icons.
    Image formats, like png, jpg will be referred to as image files.





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
    explore:  
    
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
    :caption: Using database, control, boundary Deployment Diagram Elements

.. literalinclude:: ./keysequence.puml
    :linenos:
    :emphasize-lines: 4, 5, 6, 7, 8, 9, 18, 20

.. EndPlayingExample

In this diagram, we're using some PlantUML keywords:

#. **autonumber**: to automatically number the sequence steps.
#. **box**: to highlight domains: trusted in green, untrusted in red.
#. **group**: to group sequence flows. And these can be grouped within other groups.
#. **note**: to add a note to the diagram.




Standard Library Sprites
===============================================================================

PlantUML includes a Standard Library. Contents of the library come from third party contributors.

#. See http://plantuml.com/stdlib for what is supported in official release of PlantUML
#. "-stdlib" option lists the builtin icon libraries


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
   




Create A Sprite
===============================================================================

It's easy to create your own sprites from existing icons.

Start With a Png Image
-------------------------------------------------------------------------------

Here we use a 100x100 person icon 

.. figure:: ./C4person100.png
   

Convert To Sprite Of Different Resolutions As Follows
-------------------------------------------------------------------------------

You can use the PlantUML GUI as described in sprites_, or use the command line:

::

     java -jar plantuml.jar -encodesprite 4 C4person100.png > C4person4.sprite
     java -jar plantuml.jar -encodesprite 16 C4person100.png > C4person16.sprite
     java -jar plantuml.jar -encodesprite 8 C4person100.png > C4person8.sprite


C4person4.sprite file:

.. literalinclude:: ./C4person4.sprite
    :linenos:
   

.. note ::
    You may have noticed there are more than 4 different values in C4person4.sprite
    This is to make sprite definition as compact as possible. For sprite with 4 colors, each pixel can have 4 values.
    If you group pixels by 3, it means that you have 4*4*4 = 64 possible values by pixel's group.
    If you use characters 0-9, A-Z, a-z and _ and -, you have exactly 64 values. 
    So each character encodes actually 3 pixels at once.

.. _scalebigsmall-label:

Create Diagram With Our Sprites
-------------------------------------------------------------------------------

.. uml:: ./bigsmall.puml
    :align: center

.. literalinclude:: ./bigsmall.puml
    :linenos:
   
.. note ::
    In this example, we created a big (100x100) icon, and a small (16 x 16) icon.
    
    The optimal way to change an icon size is to use one icon of sufficient resolution - not too big or small, (e.g. 48x48) and then use the
    scale option to increase or decrease its size.
    
    See :ref:`scale-label` for details. 





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
    :emphasize-lines: 9, 11

.. EndPlayingExample

.. tip ::
    
    You can scale an image. In the diagram above, we made the image 0.5, and 1.5 times bigger using the ```scale``` keyword.




So Why Do I Need Sprites?
-------------------------------------------------------------------------------

Sprites are monochrome (16 shades/levels max), versus image files which can be infinite color at high resolution.

#. But we can easily change a sprite's characteristics via PlantUML e.g. color.
#. Many large companies are moving towards simple monochrome icons e.g. the AWS went from https://github.com/plantuml/plantuml-stdlib/tree/master/aws to https://github.com/awslabs/aws-icons-for-plantuml. Similarly, kubernetes, GCP, Azure architecture icons are simple.
#. They are also smaller in size.