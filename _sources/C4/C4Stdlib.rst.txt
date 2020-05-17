*******************************************************************************
Using PlantUML Stdlib C4 Lightweight Software Architecture Description Method
*******************************************************************************

     
`C4-PlantUML <https://github.com/RicardoNiepel/C4-PlantUML>`__ combines
the benefits of `PlantUML <http://plantuml.com/>`__ and the :ref:`c4-label` model for providing a simple way of describing
and communicating software architectures - especially during up-front design sessions - with an intuitive language using open source and platform independent tools.

It also supports `C4 PlantUML Snippets for Visual Studio Code <https://github.com/RicardoNiepel/C4-PlantUML#snippets-for-visual-studio-code>`__


Example Big Bank
^^^^^^^^^^^^^^^^
.. note :: 
    The examples from `C4-PlantUML <https://github.com/RicardoNiepel/C4-PlantUML>`__ are used.

    Person sprites are added to the customer box to emphasize the user in the diagrams.

Context
~~~~~~~

.. note :: 
    The top-level diagram shows the big boxes in the system.

.. uml:: ./C4-PlantUML/C4_ContextDiagramSample-bigbankplc.puml
    :align: center


.. literalinclude:: ./C4-PlantUML/C4_ContextDiagramSample-bigbankplc.puml
    :linenos: 

.. note :: 
    More detail is then added.

.. uml:: ./C4-PlantUML/C4_ContextDiagramSample-bigbankplc-landscape.puml
    :align: center

.. literalinclude:: ./C4-PlantUML/C4_ContextDiagramSample-bigbankplc-landscape.puml
    :linenos: 




Container
~~~~~~~~~
.. note :: 
    We then drill down into the "Internet Banking" box.

.. uml:: ./C4-PlantUML/C4_ContainerDiagramSample-bigbankplc.puml
    :align: center

.. literalinclude:: ./C4-PlantUML/C4_ContainerDiagramSample-bigbankplc.puml
    :linenos: 



Component
~~~~~~~~~
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
~~~~~~~~~

.. note :: 
    We could then add the Class diagrams for the different Components.
