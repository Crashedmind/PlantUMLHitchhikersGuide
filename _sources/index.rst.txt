*******************************************************************************
Welcome to Playing with PlantUML!
*******************************************************************************

.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing


.. logo-begin-content

.. figure:: plantumllogo.png
    :width: 200px
    :align: center
    :height: 100px
    :alt: alternate text
    :figclass: align-center

    Where system diagrams meet system reality

.. logo-end-content



.. caveat-begin-content

.. todo::

    Add instructions for user to provide feedback

.. warning::

    This is an initial draft that likely contains typos, and will likely change.
    If you do find an issue, or would like to suggest a change, then submit an issue on Todo



.. caveat-end-content

.. comment 
   this link causes link error to fail : false positive
   masteringbusinessanalysis.com/mba084-agile-modeling-with-scott-ambler/ causes link check errors but link is fine
   so replace with related link

.. _AgileModeling: http://agilemodeling.com/essays/barelyGoodEnough.html

.. _AgileModelingBP: https://tdan.com/best-practices-for-agile-documentation/18936

.. showcase-begin-content


Imagine 
===============================================================================

.. tip ::

    Imagine being able to 

    #. share a model or diagram between all members of the team that they can all understand and contribute to and edit
    #. draw diagrams like below automatically from a text description.
    #. describe a system before you build it, when you're building it, and as you maintain it into the future - keeping the description and the system current and in sync.
    #. maintain that text version in a source code repository beside the code for the system it is describing

    Imagine having a diagramming tool that

    #. fits with a developer workflow, and developers are comfortable using
    #. enables **lightweight just-enough** AgileModeling_ in a way that meets AgileModelingBP_ 
    #. fits with modern practices of Continuous Integration Continuous Delivery - and "everything as code" including diagrams.

    Well that's what PlantUML gives you, and more...


.. raw:: html

      <!DOCTYPE html>
      <html>
      <head>
      <style>
      div.gallery {
      border: 1px solid #ccc;
      }

      div.gallery:hover {
      border: 1px solid #777;
      }

      div.gallery img {
      width: 100%;
      height: auto;
      }

      div.desc {
      padding: 15px;
      text-align: center;
      }

      * {
      box-sizing: border-box;
      }

      .responsive {
      padding: 0 6px;
      float: left;
      width: 24.99999%;
      }

      @media only screen and (max-width: 700px) {
      .responsive {
         width: 49.99999%;
         margin: 6px 0;
      }
      }

      @media only screen and (max-width: 500px) {
      .responsive {
         width: 100%;
      }
      }

      .clearfix:after {
      content: "";
      display: table;
      clear: both;
      }
      </style>
      </head>
      <body>



      <h3>Some Examples</h3>
      
      <div class="responsive">
      <div class="gallery">
         <a target="_blank" href="networkusers.png">
            <img src="networkusers.png" alt="Network Users" width="600" height="400">
         </a>
         <div class="desc">Uses PlantUML Stdlib OSA icons as described here TODO. insert link to puml file</div>
      </div>
      </div>


      <div class="responsive">
      <div class="gallery">
         <a target="_blank" href="networkusers.png">
            <img src="networkusers.png" alt="Network Users" width="600" height="400">
         </a>
         <div class="desc">Uses PlantUML Stdlib OSA icons as described here TODO. insert link to puml file</div>
      </div>
      </div>

      <div class="responsive">
      <div class="gallery">
         <a target="_blank" href="networkusers.png">
            <img src="networkusers.png" alt="Network Users" width="600" height="400">
         </a>
         <div class="desc">Uses PlantUML Stdlib OSA icons as described here TODO. insert link to puml file</div>
      </div>
      </div>

      <div class="responsive">
      <div class="gallery">
         <a target="_blank" href="networkusers.png">
            <img src="networkusers.png" alt="Network Users" width="600" height="400">
         </a>
         <div class="desc">Uses PlantUML Stdlib OSA icons as described here TODO. insert link to puml file</div>
      </div>
      </div>

      <div class="clearfix"></div>

      <div style="padding:6px;">
      <p>See more examples in Showcase and RealworldPlantuml</p>

      </div>

      </body>
      </html>

.. showcase-end-content




.. todo::

    include extract from about plantuml chapter



.. comment
    Sphinx is expecting 3 spaces under toctree i.e. it does not work with 4

.. toctree::
   :maxdepth: 2
   :numbered:
   :caption: Introduction

   AboutPlantUML
   AboutThisGuide

      
.. toctree::
   :maxdepth: 2
   :numbered:   
   :caption: Stdlib

   PlantUMLSpriteLibraries/plantuml_sprites
   PlantUMLSpriteLibraries/PlantUMLSprites
   NetworkUsersMachines/NetworkUsersMachines
   PassSpriteAsParameter/PassSpriteAsParameter
   Stdlib/StandardisingSrdLib
   Stdlib/ContributingToStdlib   
   

.. toctree::
   :maxdepth: 2
   :numbered:   
   :caption: C4   
   
   C4/C4Stdlib
   



.. toctree::
   :maxdepth: 2
   :numbered:   
   :caption: New ways to Run PlantUML
   
   GenerateDiagrams/GenerateDiagrams
   GenerateDiagrams/GenerateDiagramsLambda
   

.. toctree::
   :maxdepth: 2
   :numbered:
   :caption: Example galleries


.. toctree::
   :maxdepth: 2
   :numbered:
   :caption: Annex
   
   C4/c4
   DocumentationAsCode/JourneyDocumentationASCode

.. toctree::
   :maxdepth: 2
   :numbered:
   :caption: ToDo
      
   todo   
                    
