*******************************************************************************
PlantUML Stdlib Overview
*******************************************************************************


.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _listsprites: https://plantuml.com/#
.. _together: https://forum.plantuml.net/4387/please-provide-together-keyword-group-diagram-nodes-together
.. _MigrationNotes: https://plantuml.com/preprocessing#ajlk3nchu0zkka0ybjng
.. _DefaultArgumentValue: https://plantuml.com/preprocessing#ae1b47605326b65f


.. tip ::
    
    See :ref:`githubfilefinder-label` for a handy hint on searching for icons.


PlantUML Standard Library Overview
===============================================================================
This overview is at May 2020.


`PlantUML Standard Library <https://plantuml.com/stdlib>`__ includes
several icon libraries from different sources (including myself) and
they are varied in functionality and how to use them.

The most recent addition is
https://github.com/awslabs/aws-icons-for-plantuml.

https://github.com/awslabs/aws-icons-for-plantuml (Amazon) builds on the
work of https://github.com/RicardoNiepel (MicroSoft):

1. `https://github.com/RicardoNiepel/Azure-PlantUML <https://github.com/RicardoNiepel/Azure-PlantUML>`__
2. https://github.com/RicardoNiepel/C4-PlantUML which builds on
   https://c4model.com/

   These in turn build on

      1. https://github.com/milo-minderbinder/AWS-PlantUML
      2. https://github.com/Roemer/plantuml-office


.. note ::

    There are now 2 AWS icon sets in PlantUML Stdlib:
    
    * The original one from 2018 with the older icon style: https://github.com/plantuml/plantuml-stdlib/blob/master/aws/INFO
    * The newer one from 2020 AWSlabs https://github.com/plantuml/plantuml-stdlib/blob/master/awslib/INFO that has the latest icons from AWS.


Broadly, the main groupings (based on macro definition) are per diagram.
Osa and Elastic are based on aws.

.. uml:: StdlibGroupings.puml
    :align: center
    :caption: PlantUML Stdlib Groupings Of Libraries Based On Similarity






Type 1 (e_type,e_color,e_sprite,label,alias,e_stereo)
---------------------------------------------------------------------------------------------------
AWS is one of the original stdlib entries - it's from 2017.
Some libraries, listed below, followed the same layout, or used the same tools to create the sprites.


https://github.com/plantuml/plantuml-stdlib/blob/master/aws/AI/AmazonLex/ contains 4 files:

* AmazonLex-sprite.puml 68x72/16 sprite
* AmazonLex.puml same as AmazonLex-sprite.puml but with macros
* AmazonLex_LARGE-sprite.puml 340x360/16
* AmazonLex_LARGE.puml same as AmazonLex_LARGE-sprite.puml but with macros

The macros look like: 

:: code-block::

    !define AMAZONLEX(alias) PUML_ENTITY(component,#2F74B8,AmazonLex,alias,AmazonLex)

    !definelong AMAZONLEX(alias,label,e_type="component",e_color="#2F74B8",e_stereo="AmazonLex",e_sprite="AmazonLex")
    PUML_ENTITY(e_type,e_color,e_sprite,label,alias,e_stereo)
    !enddefinelong


osa
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

https://github.com/plantuml/plantuml-stdlib/blob/master/osa

:: code-block::

    !define LEFT(alias) PUML_ENTITY(component,black,left,alias,left)

    !definelong LEFT(alias,label,e_type="component",e_color="black",e_stereo="left",e_sprite="left")
    PUML_ENTITY(e_type,e_color,e_sprite,label,alias,e_stereo)
    !enddefinelong

elastic
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

https://github.com/plantuml/plantuml-stdlib/blob/master/osa

:: code-block::

    !define APM(alias) PUML_ENTITY(agent,00BFB3,apm,alias,apm)

    !definelong APM(alias,label,e_type="agent",e_color="00BFB3",e_stereo="apm",e_sprite="apm")
    PUML_ENTITY(e_type,e_color,e_sprite,label,alias,e_stereo)
    !enddefinelong





Type 2 (e_alias, e_label, e_techn, e_descr)
---------------------------------------------------------------------------------------------------

Below shows what the macros look like for each icon

azure
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

https://github.com/plantuml/plantuml-stdlib/blob/master/azure/AIMachineLearning/AzureBatchAI.puml

.. code-block:: 
    
    AzureEntityColoring(AzureBatchAI)
    !define AzureBatchAI(e_alias, e_label, e_techn) AzureEntity(e_alias, e_label, e_techn, AZURE_SYMBOL_COLOR, AzureBatchAI, AzureBatchAI)
    !define AzureBatchAI(e_alias, e_label, e_techn, e_descr) AzureEntity(e_alias, e_label, e_techn, e_descr, AZURE_SYMBOL_COLOR, AzureBatchAI, AzureBatchAI)

awslib
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

https://github.com/plantuml/plantuml-stdlib/blob/master/awslib/ARVR/ARVR.puml

.. code-block:: 

    AWSEntityColoring(ARVR)
    !define ARVR(e_alias, e_label, e_techn) AWSEntity(e_alias, e_label, e_techn, #CC2264, ARVR, ARVR)
    !define ARVR(e_alias, e_label, e_techn, e_descr) AWSEntity(e_alias, e_label, e_techn, e_descr, #CC2264, ARVR, ARVR)
    !define ARVRParticipant(p_alias, p_label, p_techn) AWSParticipant(p_alias, p_label, p_techn, #CC2264, ARVR, ARVR)
    !define ARVRParticipant(p_alias, p_label, p_techn, p_descr) AWSParticipant(p_alias, p_label, p_techn, p_descr, #CC2264, ARVR, ARVR)


The BatchParticipant part supports adding icons to sequence diagrams
i.e.

::

    !define BatchParticipant(p_alias, p_label, p_techn) AWSParticipant(p_alias, p_label, p_techn, #D86613, Batch, Batch)

.. uml:: sequence.puml
    :align: center
    :caption: *Sequence diagram with icons* 


Type 3 (_alias, _label, _shape, _color)
---------------------------------------------------------------------------------------------------

office
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

https://github.com/plantuml/plantuml-stdlib/blob/master/office/Clouds/azure.puml

.. code-block:: 

    !define OFF_AZURE(_alias) ENTITY(rectangle,black,azure,_alias,OFF AZURE)
    !define OFF_AZURE(_alias,_label) ENTITY(rectangle,black,azure,_label,_alias,OFF AZURE)
    !define OFF_AZURE(_alias,_label,_shape) ENTITY(_shape,black,azure,_label,_alias,OFF AZURE)
    !define OFF_AZURE(_alias,_label,_shape,_color) ENTITY(_shape,_color,azure,_label,_alias,OFF AZURE)

cloudogu
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: 

    https://github.com/plantuml/plantuml-stdlib/blob/master/cloudogu/tools/ansible.puml
    !define TOOL_ANSIBLE(_alias) ENTITY(rectangle,black,ansible,_alias,TOOL ANSIBLE)
    !define TOOL_ANSIBLE(_alias, _label) ENTITY(rectangle,black,ansible,_label, _alias,TOOL ANSIBLE)
    !define TOOL_ANSIBLE(_alias, _label, _shape) ENTITY(_shape,black,ansible,_label, _alias,TOOL ANSIBLE)
    !define TOOL_ANSIBLE(_alias, _label, _shape, _color) ENTITY(_shape,_color,ansible,_label, _alias,TOOL ANSIBLE)
    skinparam folderBackgroundColor<<TOOL ANSIBLE>> White
    @enduml


tupadr3
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: 

    https://github.com/plantuml/plantuml-stdlib/blob/master/tupadr3/devicons/android.puml
    !define DEV_ANDROID(_alias) ENTITY(rectangle,black,android,_alias,DEV ANDROID)
    !define DEV_ANDROID(_alias, _label) ENTITY(rectangle,black,android,_label, _alias,DEV ANDROID)
    !define DEV_ANDROID(_alias, _label, _shape) ENTITY(_shape,black,android,_label, _alias,DEV ANDROID)
    !define DEV_ANDROID(_alias, _label, _shape, _color) ENTITY(_shape,_color,android,_label, _alias,DEV ANDROID)
    skinparam folderBackgroundColor<<DEV ANDROID>> White
    @enduml

Type 4 (_color, _scale, _alias, _shape, _label)
---------------------------------------------------------------------------------------------------

material
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: 

    https://github.com/plantuml/plantuml-stdlib/blob/master/material/access_point.

    1153 files (not in categorised folders)
    !define MA_ACCESS_POINT(_color)                                 SPRITE_PUT(                                   ma_access_point, _color)
    !define MA_ACCESS_POINT(_color, _scale)                         SPRITE_PUT(                                   ma_access_point, _color, _scale)
    !define MA_ACCESS_POINT(_color, _scale, _alias)                 SPRITE_ENT(  _alias, MA ACCESS_POINT,         ma_access_point, _color, _scale)
    !define MA_ACCESS_POINT(_color, _scale, _alias, _shape)         SPRITE_ENT(  _alias, MA ACCESS_POINT,         ma_access_point, _color, _scale, _shape)
    !define MA_ACCESS_POINT(_color, _scale, _alias, _shape, _label) SPRITE_ENT_L(_alias, MA ACCESS_POINT, _label, ma_access_point, _color, _scale, _shape)
    skinparam folderBackgroundColor<<MA ACCESS_POINT>> White

No Macros
---------------------------------------------------------------------------------------------------
The following macros are sprites only with no macros.

logos
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

https://github.com/plantuml/plantuml-stdlib/blob/master/logos/100tb.puml 

This one includes sprites only.

cloudinsight
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

https://github.com/plantuml/plantuml-stdlib/tree/master/cloudinsight

This one includes sprites only.

kubernetes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
https://github.com/plantuml/plantuml-stdlib/blob/master/kubernetes

This does include a https://github.com/plantuml/plantuml-stdlib/blob/master/kubernetes/k8s-skinparam.puml

Icons are grouped into a file based on resolutions and labels

* Different resolutions 64x63/16z, 128x125/16z, 256x249/16z]
* labeled or unlabeled






|image0| Example image from icons from AWSlabs icon files
[https://github.com/awslabs/aws-icons-for-plantuml]




Superset Of Parameters
===============================================================================

The superset of parameters in macros:

    * sprite
    * color
    * scale (material library only)
    * shape (Type 1 (e_type), 4 (_shape))
    * technology
    * description
    * label

These Text attributes are not parameters:

    * Text Size: where text size does vary in some libraries
    * Number of Individual Text fields
    * Order of Individual Text fields


