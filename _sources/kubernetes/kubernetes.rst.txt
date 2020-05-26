*******************************************************************************
Kubernetes and Azure
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

    In this section we'll look at a Kubernetes and Azure icon sets https://github.com/dcasati/kubernetes-PlantUML.

    PlantUML will access icon files directly from this repository (it is not part of PlantUML Stdlib.)
    


===============================================================================

Original
-------------------------------------------------------------------------------

.. figure :: ./aks.png
    

PlantUML Equivalent
-------------------------------------------------------------------------------

I made 1 minor change to the source 

#. Added ```skinparam linetype polyline``` as the "RBAC" text overlapped the "Kubernetes Cluster" and polyline generally improves layout.


.. uml:: k1.puml
    :align: center

.. literalinclude:: ./k1.puml
    :linenos: 
    :emphasize-lines: 4, 11, 31

