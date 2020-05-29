*******************************************************************************
About this Guide
*******************************************************************************

.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLStdlib: https://plantuml.com/stdlib
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _PlantUMLStdlibRFC: https://github.com/plantuml/rfc-for-standard-plantuml-stdlib

.. _Twice: https://en.wikipedia.org/wiki/Joseph_Joubert

.. include:: ../index.rst
   :start-after: logo-begin-content
   :end-before: logo-end-content

The Story
===============================================================================

I, @crashedmind, wrote this guide as part of my own "Journey to Documentation as Code" where I landed on PlantUML and Sphinx as the main tools for proposing, analysing, documenting, maintaining software systems based on working with thousands of engineers across the globe.

I am a regular user of PlantUML and I believe in its current and future potential (:ref:`Thoughts For The Future`).

I had initially contributed the OSA icon set to PlantUML Stdlib. Specifically I generated the icon set and published it in my github. I was pleasantly surprised that it was picked up and included in the PlantUML Stdlib.

Some time later I was working on a project that used an Elastic stack, and I needed the Elastic icon set for PlantUML. So I created that - and submitted via an email and PR.

I was thinking about adding more icon sets I needed, and trying to better understand the macros people had defined as part of their stdlib icon sets.
That's described in the "Understanding Standard Library" section (:ref:`PlantUML Stdlib Overview`).

So, I contacted Arnaud to see if anything like this was on the roadmap. 

In the subsequent 3 weeks, the idea to standardize the Stdlib was discussed, the idea for a guide was born, and 3 weeks later the first version of the guide was released.
This 3 weeks was initially planned as a break as I changed employer.
But I enjoy playing with techie stuff, and my thoughts were consumed by improving PlantUMLStdlib_.
So the 3 weeks became an opportunity in my career to give something back to the PlantUML, and open source community, and to learn about PlantUML.


To enable the StdLib standardisation, I suggested the *keyword arguments* and Arnaud produced a release to play with next day - and this became part of an official release:
* https://plantuml.com/news 

    * 17 May, 2020: Use keyword arguments with the preprocessor (V1.2020.10). (Thanks to Crashedmind for the suggestion !)*
    * See :ref:`understandingstdlib-label` for more info.

The effort to date has led to an PlantUMLStdlibRFC_, where the PlantUML user requirements for stdlib, and the proposal will be captured.



Scope
===============================================================================
The scope of the guide is the PlantUML Standard Library (PlantUMLStdlib_); the Library
that allows creation of icon diagrams like those shown in :ref:`PlantUML Diagram Examples` .

The scope is NOT the various UML-type diagrams that PlantUML is better known for.
https://real-world-plantuml.com/ is a good resource to learn these by example.

Skinparam has not been detailed as it is likely to change per https://plantuml.com/style-evolution.


Goals
===============================================================================

#. Create a user-focused guide for PlantUMLStdlib_ that enables you, the user, to deliver maximum value with PlantUMLStdlib_.
#. Create a guide that was better than anything that existed and that I, @crashedmind, would be happy with.
#. Grow PlantUML; this guide and other information, the tool, and the community.

Principles
===============================================================================

The Principles on which this guide are based:

#. Deliver Value to the user
#. Learn by Playing: The examples include a link to allow you to edit and play with them easily - no setup required.
#. To teach is to learn twice.
#. Open Source - The Network Effect - anyone can and should contribute to this guide. 
#. It must be fun to write it - and to read it.
#. Documentation-Of-Code Documentation-As-Code: documentation of the examples, and the example source live together in the same directory in Git. 



.. _delivervalue-label:

Deliver Value To The User
-------------------------------------------------------------------------------

.. tip ::

    "Users want powerful tools that amplify their capabilities and enable them to do their tasks."

    http://www.ifp.illinois.edu/nabhcs/abstracts/shneiderman.html

This guide is focused on enabling you to do what you need to do - empowered by PlantUML.
So it is outcome focused.

In my professional role building products in the software industry, I tell my team members: 
*The customer cares about what they are trying to do - not your product.*

This tweet illustrates this graphically:


.. tweet:: https://twitter.com/UserOnboard/status/408372844876165120




So the examples focus on what we're trying to do - and explain only the parts of PlantUML that are necessary to do it.
        
Learn by Playing
-------------------------------------------------------------------------------

Each chapter in section "Using Standard Library" has an outcome - the diagram(s) to be created and understood by the reader e.g. :ref:`Create a Diagram of a Typical Network`.

Each step in each chapter has 

    #. An outcome - the step heading
    #. Source code - for the diagram
    #. Play - where you can test the diagram and play with it.
    #. Explore - where you can confirm your understanding by trying things as you play.



To Teach Is To Learn Twice_
-------------------------------------------------------------------------------
 If I knew all this info already, I would have no interest in writing this guide. 

 It was the quest for knowledge that drove it, and the quest for a solution to a problem that consumed my thoughts (making PlantUML StdLib simpler, standard, and more friendly and powerful to the user ).

 There's no better way to learn than by writing a guide for others - and having the master on hand to provide insights as you go - and the community to share their knowledge. 
 
 I expect to learn from feedback on this guide.

Open Source - The Network Effect
-------------------------------------------------------------------------------
PlantUML, and all the :ref:`Tools-label` required to write this guide are Open Source. 

Moreover, the first release is intended as a seed to be grown by the PlantUML community.


It Must Be Fun To Write It - And To Read It
-------------------------------------------------------------------------------
Happy People are Productive People are Happy People!

Documentation-Of-Code Documentation-As-Code
-------------------------------------------------------------------------------

As part of the Agile, and Continuous Delivery, movements, software, and the models that describe software, are necessarily coming closer together.
PlantUML is one way to enable this.

See :ref:`JourneyDOC-label` for more details. 




.. _Tools-label:

Tools Used
-------------------------------------------------------------------------------

The source for this guide, the diagrams, and the tools to create them, all live in the same repo.

Sphinx and PlantUML (running in Docker), and GitHub, are the primary tools used for this guide. 

PlantUML source is stored in files in the same repo (as the tools and documentation).

* The sphinx documentation source is ReStructuredText because it is more powerful than Markdown especially in a guide like this that references many source files.
* sphinxcontrib.plantuml extension allows building the plantuml diagrams automatically at the same time the documentation is built for html (or other) output.

I used Visual Studio Code, with jebbs.plantuml extension, on Kubuntu, as my work environment. 

The Sphinx and PlantUML toolchain runs on demand at build time in Docker.

Github 

* hosts the documentation and diagram source and the toolchain Dockerfile.
* separate repo stores the output html served via Github pages.
* GitHub actions and workflow are used e.g. when output html is committed, it triggers a link checker that auto-creates an Github issue for the project if a URL link is broken.

    * In the future, I may move the toolchain Docker to a GitHub action+workflow so the html is built on commit.


Credits
===============================================================================

#. Arnaud for giving us PlantUML. And for being receptive and responsive; from my initial contact asking questions, to subsequent interactions providing suggestions.
#. The people who created stdlib icon sets and macros to date from which I learnt a lot: :ref:`PlantUML Standard Library Overview`.
#. The active PlantUML community for asking and answering questions - both of which informed this guide.

Feedback
===============================================================================

This is an initial version; fixes and features will be added over time.

To submit a suggestion, create an issue on https://github.com/Crashedmind/PlantUMLHitchhikersGuide.
These will be reviewed and ranked periodically, and then resolved.
 

|playbutton_kub1| **Hit the like (star) button and subscribe (watch)!**


.. |playbutton_kub1| image:: ../play.png
                :target: https://github.com/Crashedmind/PlantUMLHitchhikersGuide
                :width: 40 px