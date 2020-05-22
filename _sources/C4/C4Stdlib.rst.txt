*******************************************************************************
Using PlantUML Stdlib C4 Lightweight Software Architecture Description Method
*******************************************************************************

.. _c4plantuml-label:

C4
===============================================================================
.. tip ::
    
    This section details PlantUML stdlib support for C4.

    See :ref:`c4-label` for details of C4. 

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


.. uml:: ./C4-PlantUML/C4_ComponentDiagramSample-bigbankplc.puml
    :align: center

.. literalinclude:: ./C4-PlantUML/C4_ComponentDiagramSample-bigbankplc.puml
    :linenos: 

Class
-------------------------------------------------------------------------------


.. note :: 
    We could then add the Class diagrams for the different Components.




