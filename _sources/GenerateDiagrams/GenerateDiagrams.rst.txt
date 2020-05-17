*******************************************************************************
Generate diagrams from PlantUML source files using GithubActions_
*******************************************************************************



.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _listsprites: https://plantuml.com/#
.. _together: https://forum.plantuml.net/4387/please-provide-together-keyword-group-diagram-nodes-together
.. _GithubActions: https://help.github.com/en/actions
.. _GithubActionsCoreConcepts: https://help.github.com/en/actions/getting-started-with-github-actions/core-concepts-for-github-actions
.. _UsageLimits: https://help.github.com/en/actions/getting-started-with-github-actions/about-github-actions#usage-limits
.. _GithubCommunity: https://help.github.com/en/actions/getting-started-with-github-actions/using-community-workflows-and-actions
.. _Running: https://plantuml.com/running
.. _PlantUMLActions: https://github.com/marketplace?query=plantuml 


.. note ::

    In this section we're going to look at some recent new ways ways to convert PlantUML source files (puml) to an image.

    We are going to use GithubActions_ to **automagically** generate png and svg files from our puml files when we upload them to Github.

    **automagically** because you don't need to install any software to do this - it just happens every time you upload new puml files.
        
    There are many other listed in Running_
    


Github Actions
===============================================================================

* GithubActions_ “Automate, customize, and execute your software development workflows right in your repository with GitHub Actions. You can discover, create, and share actions to perform any job you'd like, including CI/CD, and combine actions in a completely customized workflow.”
* **Workflows** "Workflows run in Linux, macOS, Windows, and containers on GitHub-hosted machines, called 'runners'."
* **Events** "A specific activity that triggers a workflow run. For example, activity can originate from GitHub when someone pushes a commit to a repository or when an issue or pull request is created."

See GithubActionsCoreConcepts_:.

These are free up to the generous UsageLimits_.

You can create your own actions or workflows, or use or repurpose ones from the GithubCommunity_.

* You can create more than one workflow in your repository. 
* You must store workflows in the .github/workflows directory in the root of your repository.

.. note ::

    At at May 2020, there are 4 PlantUML actions in the GitHub Marketplace: https://github.com/marketplace?query=plantuml 

Explore
-------------------------------------------------------------------------------

#. How many PlantUML actions are there now in Github?
#. What are the differences between them?



PlantUML GitHub action
===============================================================================
Here we will use https://github.com/marketplace/actions/plantuml-generator 
"This action runs the PlantUML tool to generate images from PlantUML text diagrams"

Specifically: 

#. You add the git Workflow file to your repository. This calls one or more GithubActions_
#. You upload some PlantUML source files (puml) to your repository
#. Automagically, you get back some png and svg image files in your repository! (in 30 seconds or so depending on how many source files you uploaded)
#. You can upload more files - only changed files will generate new png/svg files

Source
-------------------------------------------------------------------------------


Action
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

On https://github.com/marketplace/actions/plantuml-generator, there's a link to the https://github.com/cloudbees/plantuml-github-action.

This uses a Ubuntu OS with PlantUML installed

.. literalinclude:: ./Dockerfile
    :linenos:
    :emphasize-lines: 1, 9

This file lives here: https://github.com/cloudbees/plantuml-github-action/blob/master/Dockerfile. 


Example Workflow
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This generates png and svg diagrams and commits them to your repository.

.. code::

    '**.puml' #matches zero or more of any character


.. literalinclude:: ./workflow.yml
    :linenos: 
    :emphasize-lines: 28, 32, 34


Our Workflow
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We made some changes relative to the example provided - highlighted below

.. literalinclude:: ./PlantumlGenerate.yml
    :linenos: 
    :emphasize-lines: 28, 32, 34


Explore
-------------------------------------------------------------------------------

#. TBD


Play
-------------------------------------------------------------------------------

|playbutton1| Play time! Here we're going to play in GitHub.

.. |playbutton1| image:: ../play.png
                :width: 40 px
 
#. Select or create a GitHub repository to use.
#. Copy our workflow PlantumlGenerate.yml to 



.. figure:: github1.png
    :figclass: align-center
    
    create .github/workflows directory

.. figure:: github2.png
    :figclass: align-center
    
    copy workflow.yml to .github/workflows/

.. figure:: github3_upload2.png
    :figclass: align-center
    
    upload puml files; using web interface in this case to commit
    




.. todo::

    section on add some color to icons by user, machine, network
    add a boundary


Conclusion
===============================================================================


.. todo::

    Write up Conclusion




    
