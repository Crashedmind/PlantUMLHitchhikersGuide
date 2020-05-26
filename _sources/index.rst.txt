*******************************************************************************
Welcome to The Hitchhiker's Guide to PlantUML!
*******************************************************************************

.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _AgileModeling: http://agilemodeling.com/essays/barelyGoodEnough.html
.. _AgileModelingBP: https://tdan.com/best-practices-for-agile-documentation/18936

.. comment 
   this link causes link error to fail : false positive
   masteringbusinessanalysis.com/mba084-agile-modeling-with-scott-ambler/ causes link check errors but link is fine
   so replace with related link

.. logo-begin-content

.. figure:: plantumllogo.png
    :width: 120px
    :align: center
    :height: 120px
    :alt: alternate text
    :figclass: align-center

    Where system diagrams meet system reality

.. logo-end-content




.. showcase-begin-content

Imagine 
===============================================================================

.. tip ::

    Imagine being able to 

    #. share a model or diagram between all members of the team that they can all understand and contribute to and edit
    #. draw diagrams like below automatically from a text description.
    #. describe a system before you build it, when you're building it, and as you maintain it into the future - keeping the description and the system current, and in sync.
    #. maintain that text version in a source code repository beside the code for the system it is describing

    Imagine having a diagramming tool that

    #. fits with a developer workflow, and developers are comfortable using
    #. enables **lightweight just-enough** AgileModeling_ in a way that meets AgileModelingBP_ 
    #. fits with modern practices of Continuous Integration Continuous Delivery - and "everything as code" including diagrams.

    Well that's what PlantUML gives you, and more...


PlantUML Diagram Examples
===============================================================================

This guide walks through creating PlantUML diagrams, including the ones shown here.

+-----------------------------------------------------------------------------+	
| **Diagram of a Typical Network**                                            |
+-----------------------------------------------------------------------------+ 
| .. uml:: NetworkUsersMachines/NetworkUsersMachines6.puml                    | 
|    :scale: 100%                                                             |
+-----------------------------------------------------------------------------+ 
| This uses the Plantuml Stdlib Open Security Architecture icon set.          | 
| See :ref:`Create a Diagram of a Typical Network`                            | 
+-----------------------------------------------------------------------------+ 
                           
+-----------------------------------------------------------------------------+	
| **Diagram of an AWS Architecture**                                          |
+-----------------------------------------------------------------------------+ 
| .. uml:: aws/2.8.puml                                                       | 
|    :scale: 100%                                                             | 
+-----------------------------------------------------------------------------+                                    
| This uses the AWSlib icon set.                                              |
| See :ref:`Create Real Life AWS Diagrams`                                    | 
+-----------------------------------------------------------------------------+                                 


+-----------------------------------------------------------------------------+	
| **Diagram of a Kubernetes Architecture**                                    |
+-----------------------------------------------------------------------------+ 
| .. uml:: kubernetes/k1.puml                                                 | 
|    :scale: 100%                                                             | 
+-----------------------------------------------------------------------------+                                    
| This uses the Azure and Kubernetes icon sets.                               |
| See :ref:`Kubernetes`                                                       | 
+-----------------------------------------------------------------------------+          


+--------------------------------------------------------------------------------------+	
| **Diagram of a Global Widget Production System Using C4**                            | 
+--------------------------------------------------------------------------------------+
| .. uml:: C4/acme_c1.puml                                                             | 
|    :scale: 100%                                                                      | 
+--------------------------------------------------------------------------------------+ 
| This uses the :ref:`C4 Lightweight Software Architecture Description Method`.        | 
| See :ref:`Using C4 To Architect ACME Global Widget Production`                       | 
+--------------------------------------------------------------------------------------+ 








.. showcase-end-content




.. comment
    Sphinx is expecting 3 spaces under toctree i.e. it does not work with 4

.. toctree::
   :maxdepth: 2
   :numbered:
   :caption: Introduction

   about/AboutPlantUML
   about/AboutThisGuide
   about/future
   


.. toctree::
   :maxdepth: 2
   :numbered:   
   :caption: Using Standard Library 

   NetworkUsersMachines/NetworkUsersMachines
   aws/aws
   kubernetes/kubernetes
   gcp/gcp
   
   C4/c4acme

.. toctree::
   :maxdepth: 2
   :numbered:   
   :caption: PlantUML Features

   PlantUMLSpriteLibraries/plantuml_sprites
   scale/scale
   procedures/procedures
   PassSpriteAsParameter/PassSpriteAsParameter
    

.. toctree::
   :maxdepth: 2
   :numbered:   
   :caption: Understanding Standard Library 
   
   Stdlib/StdLibOverview
   StdlibUnderTheHood/StdlibUnderstanding
   Stdlib/StandardisingStdLib

.. toctree::
   :maxdepth: 2
   :numbered:   
   :caption: Standardising Standard Library 

   Stdlib/stdlibRequirements
   Stdlib/StandardisingStdLib2





.. toctree::
   :maxdepth: 2
   :numbered:
   :caption: Example galleries

.. toctree::
   :maxdepth: 2
   :numbered:   
   :caption: Annex Standard Library C4
   
   C4/c4
   C4/C4Stdlib   



.. toctree::
   :maxdepth: 2
   :numbered:
   :caption: Annex
   
   github/githubFileFinder
   DocumentationAsCode/JourneyDocumentationASCode

.. toctree::
   :maxdepth: 2
   :numbered:
   :caption: ToDo
      
   todo   
                    



.. caveat-begin-content

.. todo::

    Add instructions for user to provide feedback

.. warning::

    This is an initial draft that likely contains typos, and will likely change.
    If you do find an issue, or would like to suggest a change, then submit an issue on Todo




.. caveat-end-content



