

.. _Deployment: https://plantuml.com/deployment-diagram

======================================================
Plantuml Sprites
======================================================
PlantUML supports `sprites: <http://plantuml.com/sprite>`_ small graphic elements that can be used in diagrams.
   
Given we want to make diagrams communicate quickly and clearly, using sprites (rather than just boxes) is very effective.

You can 

#. use the builtin  `sprites <http://plantuml.com/sprite>`_
#. create your own sprites




Builtin Sprites - Deployment Diagram Sprites
----------------------------------------------

Deployment_ diagrams define several sprites.

Below is an example using some of these - in a sequence diagram.

.. uml:: ./keysequence.puml
    :align: center

.. literalinclude:: ./keysequence.puml
    :linenos:


Builtin Sprites - Standard Library Sprites
----------------------------------------------
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
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

`Plantuml for AWS <https://github.com/milo-minderbinder/AWS-PlantUML>`__
uses the `icon set from
AWS <https://aws.amazon.com/architecture/icons/>`__ and converts these
to sprites for use with PlantUML.

::

    git clone git@github.com:milo-minderbinder/AWS-PlantUML.git

Simple Example
~~~~~~~~~~~~~~

.. uml:: ./aws_nested-components.puml
    :align: center

.. literalinclude:: ./aws_nested-components.puml
    :linenos:
   

More Complex Example
~~~~~~~~~~~~~~~~~~~~

.. uml:: ./aws_comments-architecture.puml
    :align: center

.. literalinclude:: ./aws_comments-architecture.puml
    :linenos:
   





Create a Sprite
------------------------

It's easy to create your own sprites from existing icons.

Start with a 100x100 person icon png
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. figure:: ./C4person100.png
   

Convert to sprite of different resolutions as follows
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


::

     java -jar plantuml.jar -encodesprite 4 images/C4person100.png > C4person4.sprite
     java -jar plantuml.jar -encodesprite 16 images/C4person100.png > C4person16.sprite
     java -jar plantuml.jar -encodesprite 8 images/C4person100.png > C4person8.sprite


C4person4.sprite file:

.. literalinclude:: ./C4person4.sprite
    :linenos:
   

Create Diagram with our Sprites
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. uml:: ./bigsmall.puml
    :align: center

.. literalinclude:: ./bigsmall.puml
    :linenos:
   

Create Sprites by converting OSA icon libaries
----------------------------------------------------

`Open Security
Architecture <http://www.opensecurityarchitecture.org/>`__ (OSA) is a
useful resource for security architects providing a catalog of
controls, patterns, and requirements from numerous standards, governance
frameworks, legislation and regulations. See "`why have
OSA? <http://www.opensecurityarchitecture.org/cms/about/why-have-osa>`__\ ".

Resources include a `security architecture icon
library <http://www.opensecurityarchitecture.org/cms/library/icon-library>`__
available under a "`Creative Commons share-alike
license <http://www.opensecurityarchitecture.org/cms/about/license-terms>`__\ ".

These icons are available as png or svg images. 

Here we'll convert them to sprites so we can use them with PlantUML.


Converting the icon set to PlantUML Sprites
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Download the `security architecture
   icons <http://www.opensecurityarchitecture.org/cms/library/icon-library>`__
   and extract them into a directory e.g. "osaicons".

.. todo ::
    add info on a standard way to create sprites




Example
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. uml:: ./osa.puml
    :align: center

.. literalinclude:: ./osa.puml
    :linenos:

All Icons
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Below is what the icons look like - and the associated code.

.. todo ::
    add info on what osa icons look like


PlantUML HyperLinks
----------------------

PlantUML supports hyperlinks in output SVG images. This allows diagrams
to be linked together, and for a user to easily navigate by clicking
around per `Shneiderman's
mantra <http://www.ifp.illinois.edu/nabhcs/abstracts/shneiderman.html>`__:

    *Overview first, zoom and filter, then details-on-demand*

.. todo ::
    fix svg link


Clicking the image opens up the target ``svg`` image. This target image contains hyperlinks.

.. image:: ./links.svg
       :target: ../links.svg

.. literalinclude:: ./links.puml
    :linenos:
   