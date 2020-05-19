*******************************************************************************
Using PlantUML Stdlib C4 Lightweight Software Architecture Description Method
*******************************************************************************

C4
===============================================================================
.. tip ::
    
    See :ref:`c4-label` for details. 

.. include:: c4.rst
   :start-after: c4-intro-begin-content
   :end-before: c4-intro-end-content


C4 PlantUML
===============================================================================

`C4-PlantUML <https://github.com/RicardoNiepel/C4-PlantUML>`__ is included in PlantUML Stdlib. It combines
the benefits of `PlantUML <http://plantuml.com/>`__ and the :ref:`c4-label` model for providing a simple way of describing
and communicating software architectures - especially during up-front design sessions - with an intuitive language using open source and platform independent tools.

It also supports `C4 PlantUML Snippets for Visual Studio Code <https://github.com/RicardoNiepel/C4-PlantUML#snippets-for-visual-studio-code>`__

..

    https://github.com/plantuml/plantuml-stdlib/tree/master/C4

C4 Example Big Bank
===============================================================================
.. note :: 
    The examples from `C4-PlantUML <https://github.com/RicardoNiepel/C4-PlantUML>`__ are used.

    Person sprites are added to the customer box to emphasize the user in the diagrams.

Context 
-------------------------------------------------------------------------------
.. note :: 
    The top-level diagram shows the big boxes in the system i.e. the overall context in which a system operates.

    The grey boxes are external i.e. not part of the system we're defining.

.. uml:: ./C4-PlantUML/C4_ContextDiagramSample-bigbankplc.puml
    :align: center


.. literalinclude:: ./C4-PlantUML/C4_ContextDiagramSample-bigbankplc.puml
    :linenos: 

Context With More detail
-------------------------------------------------------------------------------
.. note :: 
    More detail is then added.

.. uml:: ./C4-PlantUML/C4_ContextDiagramSample-bigbankplc-landscape.puml
    :align: center

.. literalinclude:: ./C4-PlantUML/C4_ContextDiagramSample-bigbankplc-landscape.puml
    :linenos: 




Container
-------------------------------------------------------------------------------
.. note :: 
    We then drill down into the "Internet Banking" box. 

.. uml:: ./C4-PlantUML/C4_ContainerDiagramSample-bigbankplc.puml
    :align: center

.. literalinclude:: ./C4-PlantUML/C4_ContainerDiagramSample-bigbankplc.puml
    :linenos: 



Component
-------------------------------------------------------------------------------

.. note :: 
    We then drill down into the "API Application" box.

.. todo ::

    for some reason this diagram did not render to png - so include the png for now...

    .. uml:: ./C4-PlantUML/C4_ComponentDiagramSample-bigbankplc.puml
        :align: center


.. figure:: ./C4-PlantUML/C4_ComponentDiagramSample-bigbankplc.png

.. literalinclude:: ./C4-PlantUML/C4_ComponentDiagramSample-bigbankplc.puml
    :linenos: 

Class
-------------------------------------------------------------------------------


.. note :: 
    We could then add the Class diagrams for the different Components.

.. todo ::
    upgrade docker plantuml to latest to get elk, and named args




C4 ACME Global Widget Production
===============================================================================

Your mission, if you choose to accept it, is to design the ACME Global Widget Production System.

#. ACME has its own production sites, and uses 3rd party production sites.
#. All sites are connected to a central production host 


C4 ACME Context
-------------------------------------------------------------------------------


Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. uml:: acme_c1.puml
    :align: center
    :caption: *C4 ACME Context* 

.. literalinclude:: ./acme_c1.puml
    :linenos: 

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton1| Press to play around with this diagram source online.

.. |playbutton1| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuNBAJrBGjLDmpCbCJbMmKiX8pSd9vt98pKi1IW80
                :width: 40 px


Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. TODO
 






C4 ACME Container
-------------------------------------------------------------------------------

.. uml:: acme_c2_workstation.puml
    :align: center
    :caption: *C4 ACME Workstation* 



Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


.. literalinclude:: ./acme_c2_workstation.puml
    :linenos: 


Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton1| Press to play around with this diagram source online.

.. |playbutton1| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuNBAJrBGjLDmpCbCJbMmKiX8pSd9vt98pKi1IW80
                :width: 40 px


Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. TODO








C4 ACME Component
-------------------------------------------------------------------------------

.. uml:: acme_c3.puml
    :align: center
    :caption: *C4 ACME Component* 

.. uml:: acme_c3_monitoring.puml
    :align: center
    :caption: *C4 ACME Component Monitoring* 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./acme_c3.puml
    :linenos: 


.. literalinclude:: ./acme_c3_monitoring.puml
    :linenos: 


Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton1| Press to play around with this diagram source online.

.. |playbutton1| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuNBAJrBGjLDmpCbCJbMmKiX8pSd9vt98pKi1IW80
                :width: 40 px


Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. TODO


