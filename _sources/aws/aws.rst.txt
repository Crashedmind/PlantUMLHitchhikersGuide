*******************************************************************************
Create Real Life AWS Diagrams
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
.. _AWSArchitectureBlog: https://aws.amazon.com/blogs/architecture
.. _AWSArchitectureBlogSample1: Helping Global Remote Working with Amazon AppStream 2.0 https://aws.amazon.com/blogs/architecture/bbva-helping-global-remote-working-with-amazon-appstream-2-0/
.. _AWSArchitectureBlogSample2: https://aws.amazon.com/blogs/architecture/building-a-scalable-document-pre-processing-pipeline/
.. _AWSArchitectureBlogSample3: https://aws.amazon.com/blogs/architecture/serving-billions-of-ads-with-amazon-elasticache-for-redis/
.. _Deployment: https://plantuml.com/deployment-diagram

.. note ::

    In this section we'll put PlantUML to the test by seeing if we can recreate some real diagrams from the AWSArchitectureBlog_.

    We'll show the original image from the AWSArchitectureBlog_, and the PlantUML version for comparison.

    **We're aiming for architectural equivalence (not image reproduction).**

We take the 3 most recent entries that show architecture diagrams on the front page of AWSArchitectureBlog_ as at May 2020.

#. BBVA: Helping Global Remote Working with Amazon AppStream 2.0 https://aws.amazon.com/blogs/architecture/bbva-helping-global-remote-working-with-amazon-appstream-2-0/
#. Building a Scalable Document Pre-Processing Pipeline https://aws.amazon.com/blogs/architecture/building-a-scalable-document-pre-processing-pipeline/
#. Serving Billions of Ads in Just 100 ms Using Amazon Elasticache for Redis https://aws.amazon.com/blogs/architecture/serving-billions-of-ads-with-amazon-elasticache-for-redis/

This sample of 3 diagrams is quite varied in complexity and features.

We'll approach them in order of complexity.



AWSArchitectureBlogSample1_
===============================================================================

Original
-------------------------------------------------------------------------------

.. figure :: ./High-level-digram-1-Smadex-1024x584.png
    
    AWSArchitectureBlogSample1_

PlantUML Equivalent
-------------------------------------------------------------------------------

.. uml:: 1.7.puml
    :align: center

.. literalinclude:: ./1.7.puml
    :linenos: 


Select an icon library
--------------------------------------------------------------------------------
These are recent diagrams (April, May 2020) so use the newer AWS icon set from AWS i.e.

* This one: https://github.com/plantuml/plantuml-stdlib/tree/master/awslib
* Not this one https://github.com/plantuml/plantuml-stdlib/tree/master/aws

ref: https://github.com/awslabs/aws-icons-for-plantuml

Gather the icons we need
--------------------------------------------------------------------------------

* For the EC2 icon on right of diagram; for AWS icons, Orange is AWS Compute so we look at the compute icons. 
* Use our github trick to find "users"; they are in General.
* The green box isn't an AWS service - it's showing a mobile/laptop client.
* We need "Traditional Server" for "Ad Exchange"
* For the box we'll use a Deployment_ Diagram shape; ```package``` or ```cloud```


.. note ::

    ```autonumber``` does not work in these diagrams. So we will manually number the arrows.

.. todo ::

    ask @Arnaud about autonumber of sprite diagrams


.. uml:: 1.puml
    :align: center
    
.. literalinclude:: ./1.puml
    :linenos: 



Find Icons
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. uml:: 1.1.puml
    :align: center
    
.. literalinclude:: ./1.1.puml
    :linenos: 
    :emphasize-lines: 7

Add Text To Icons
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. uml:: 1.2.puml
    :align: center
    
.. literalinclude:: ./1.2.puml
    :linenos: 
    :emphasize-lines: 7-10    

Simplify The Icons
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. uml:: 1.3.puml
    :align: center
    
.. literalinclude:: ./1.3.puml
    :linenos: 
    :emphasize-lines: 3

Connect The Icons
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. uml:: 1.4.puml
    :align: center
    
.. literalinclude:: ./1.4.puml
    :linenos: 
    :emphasize-lines: 13-17

Change the Layout: ortho
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. uml:: 1.5.puml
    :align: center
    
.. literalinclude:: ./1.5.puml
    :linenos: 
    :emphasize-lines: 8,9    

Change the Layout: polyline
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. uml:: 1.6.puml
    :align: center
    
.. literalinclude:: ./1.6.puml
    :linenos: 
    :emphasize-lines: 8,9        

Add A Box: package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. uml:: 1.7.puml
    :align: center
    
.. literalinclude:: ./1.7.puml
    :linenos: 
    :emphasize-lines: 12       













AWSArchitectureBlogSample2_
===============================================================================

Original
-------------------------------------------------------------------------------

.. figure :: ./Pre-processing-pipeline-architecture-SM.jpg
    
    AWSArchitectureBlogSample2_
    
PlantUML Equivalent
-------------------------------------------------------------------------------

.. uml:: 2.8.puml
    :align: center
    

.. tip ::
    In general, I recommend starting a diagram without forcing the arrow directions to let PlantUML optimise the layout; then tweak the result.
    
    Because we are trying to compare to an existing complex diagram, I will force the layout to match the original - but only up to a point that allows clarity and comparison.

.. tip ::
    Because there are a lot of parts to this diagram, I built it step-by-step in sections to validate as I went - which makes it easier to fix a typo, or get feedback as we go.
    Not all steps are shown here - only the final ones - but the PlantUML source code files for each step are in the directory with the source and documentation.

First Pass
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. uml:: 2.6.puml
    :align: center
    
.. literalinclude:: 2.6.puml
    :linenos: 

Second Pass: Tweak
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
#. For clarity, force the cloudwatch branch to go horizontal and connect from left to DLQ.
#. Use ```together``` to group the SQS and File processing icons.
#. I did not change the boxes line style or colour. 

.. uml:: 2.8.puml
    :align: center
    
.. literalinclude:: 2.8.puml
    :linenos: 



AWSArchitectureBlogSample3_
===============================================================================

.. figure :: ./BBVA-uses-AWS-Transit-Gateway-to-build-a-hub-and-spoke-network-topology-2.png
    
    AWSArchitectureBlogSample3_

Gather the icons we need
--------------------------------------------------------------------------------

.. tip ::
    When using ```listsprites``` limit the number of library categories you include to make it easier to search category by category.
    Simplified off (by commenting out the simplified header) so we can see the icon name.

.. uml:: 3.1.puml
    :align: center
    
.. literalinclude:: ./3.1.puml
    :linenos: 



Add Text and Simplify The Icons
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. uml:: 3.3.puml
    :align: center
    
.. literalinclude:: ./3.3.puml
    :linenos: 


Connect The Icons
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


.. todo ::
    finish aws 3 diagram - figure out best way to do boundaries
    https://github.com/dcasati/kubernetes-PlantUML uses the c4 type boundary macros 

