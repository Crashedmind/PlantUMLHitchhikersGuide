*******************************************************************************
Thoughts For The Future
*******************************************************************************



.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _plantuml.github.io: https://plantuml.github.io
.. _plantumlGuide: http://alphadoc.plantuml.com/toc/asciidoc/en

.. uml:: mindmapfuture.puml
    :align: center
    :caption: *Some thoughts on what could be done in the future... no more than thoughts as of now for me... but you...*


A Showcase Template Site
===============================================================================
#. As a user who wants to draw a diagram, I'd like to be able to browse to a site, select a category e.g. "AWS" and see a selection of existing "AWS" diagrams. 
#. As a user who has drawn diagrams, I'd like to be able to share and showcase my diagrams on a site, for a given category e.g. "AWS" diagrams. 
#. As a user who draws or uses diagrams, I'd like to take part in a "best of" competition where the best entry for a given category is selected by the community.

Hyperlinked Interactive Diagrams
===============================================================================
Per *Overview first, zoom and filter, then details-on-demand* :ref:`C4 Lightweight Software Architecture Description Method`, PlantUML_ supports the creation of svg diagrams which can contain hyperlinks.

Hyperlinked connected diagrams would be powerful and in theory are supported already (though I have seen png produce better diagrams that svg.)

Svg images can also use CSS characteristics like dynamically changing on hover per https://plantuml.com/svg.


Machine Processing Of Text Files
===============================================================================
Having a diagram source as a text file is powerful because it allows for machine processing e.g.

#. If standard building blocks are used, it allows automated analysis and recognition of the diagram text source, and recommendations to the user e.g. 
   if an arrow text includes "TLS" to indicate the link is secured, then an external program can provide recommendations on TLS protocol version, cipher-suites etc...
#. As companies move towards standard architecture icon sets (AWS, MS/Azure, Google,...), it is possible to process an existing architecture diagram image with optical recognition (and machine learning) and create the text (plantuml) equivalent.



Architecture Icon Sets
===============================================================================

Companies like AWS, Google, Microsoft publish architecture icon sets for building architecture diagrams:

#. https://aws.amazon.com/architecture/icons/
#. https://cloud.google.com/icons
#. https://www.microsoft.com/en-us/download/details.aspx?id=41937

These establish a shared lexicon of understanding and allow users to focus on the things they're trying to do.

**Do you (personal, organisation, company) have an icon set for building your (architecture or other) diagrams?**

These icon sets are easily imported to PlantUML.


Security Modeling
===============================================================================

A security model consists of:

#. Assets
#. Domains
#. Interfaces
#. Data Flows
#. Threats and threat actors

All of these fit well with PlantUML capabilities and allow for the **same tool and diagrams** to be used for general and security discussion and analysis. 

Today, it is common to use different tools and diagrams for security modeling. They may be meaningful to the security folks, **but if they're not meaningful to the rest of the team then they're missing the point**.



Github Actions and Workflows
===============================================================================
Github Actions and Workflows are relatively new and powerful. 

I used some to generate this guide e.g. automated link checking on commit.

They could be used for various things:

#. Easy automated creation of icon sets without a user having to install or understand tools e.g.

   #. organise and sanitise the images you want to create sprites from as svg/png/whatever
   #. upload to your github repo
   #. get back the icon set in your repo
#. Easy automated build of documentation on commit e.g.

   #. source for this document and diagrams is committed to github
   #. document html is built with sphinx and plantuml and document is published.
   #. This is trivial to implement - but I did not feel it was worth setting up until the first version of the document was published.



Guide for PlantUML_ Diagrams
===============================================================================
The scope of this guide is stdlib icon diagrams only per :ref:`Scope` - not the traditional UML diagrams.
It's the guide I wish I had when using PlantUML for diagrams.

Documentation of the undocumented features in PlantUML is required. 
And **YOU** can document them in the plantumlGuide_ 

That said, much of the documentation should start and live in the source code using e.g. javadoc. 

It would then be relatively easy to extract and render to rst/md/html or anywhere else.

This would be a prerequisite to a user-centric guide that can live and grow. 

Interactive Notebook Guide
===============================================================================
Interactive Notebooks e.g. https://jupyter.org/, are a good format to describe PlantUML features. 

PlantUML support is available https://pypi.org/project/IPlantUML/


