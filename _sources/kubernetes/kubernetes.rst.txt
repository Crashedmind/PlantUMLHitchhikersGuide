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



Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_kub1| Press to play around with this diagram source online.

.. |playbutton_kub1| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/bPPHJ-Cu4CVVyocyVTcij903xkcUDWtiWfPZUnHEEWa9JUsXjUhOMNi2z4xttS-9qzOvQ9Nc0UAP_yypiMS6lZW2ItMfaYTZ22txNi_GQYHqRA90qz7zxzU9uw2GbV3AJduv_PMzI46Bn2sbhi12oPJqmAf2LXcrQXQHJnk13YiFHaOBUjaP_VEHvN_N5fCF0fyy75OJdnDR45Nkjoopy78ybxIePxL3ouqcr7JCJPdTIWvMc1k95Qgi9O_Ql7tQcKM5u30xFJh9X7IK91-avgeMM5kr3HEmmfIbqSULD-oJJMLPAVaaKGJf3gtVhQe90vDNrHJji-GOc07868WlzgirWTHeNG0swrkSIqTsTGYylVG1UPu3mGmSTknw-TNOYN4qjpZzu_e0lZ2kDEvyTW0o_QdMbhqKFl-eEcGYAsmgq-q3hWHgahGAICv9FkEvjCZ9x3_F6wGNOtrvpmDwRK2CGO7cQFTnK-IrtGJyZgi_eLQqbo1ZORuk4cLcdM4mqzCd7wD-N_TVP1hOX8A30vBPSWDkUx04HsZVQRz-b8XzB9gjNyCn34JUTEKUxCTqccrDUIK3CfYuqlC3YObPfmLDAR5HgCmH0yS4FflAvKg2IxXH2Zb9enqR5KgY9fPNdP2tQtWhl4HLic81be9muTT1bYXy8aQ6MJbV41FI1cWpSbapSun6JIvvh-PJ0F6PZHvqwtpGmSqs_f5tVlD526hqANb_3AN0hLVbnMqZBa2305RuY3Q6mWX8UVlIHWmsTZxknuZx95tYwhbvYLFqJjPwtt9nLwQWPYtM61_qshmpntZcfEwdQjcBLqAhGJreuLtCaR7eTcmHpw0KX6bKLrbntYNEDiuuxtw3nhTLgBhfgyUngNrmVymy63mS0y4u-iJ-IPX_UcMVzbPzC9zSDNdu31gi_N439ReAE6vZQlVL6aqNMdXj-yhyUuZMFRssIQMUMtJEgtq0zWq8Ns0L1VetsHrg37mP8ZLlUmBvRei-RNnnuf4GOu3uz13ncHSEpFwUfFBAvfTSiUwlh1lq1Gqp-1k2F7p5DY-VsIsgD9erdrbexVp-xjBB6cyxDuBl_vNHk5XTpIq8zEfMtl9H1x9kcpxRXRaTvyMe2JVzwwPOxn1DDAzh-_7oxcuIwnfPw-ag9vR4MstS_OllPnNP-rS-I7RMoOAkp_k1i6EJizuP-PjYwtyotXU72HY52hCY355X-18jgsgt2FJZ_PlZxWkLyi8lg4LTgly0_
                :width: 40 px

I made 1 minor change to the source 

#. Added ```skinparam linetype polyline``` as the "RBAC" text overlapped the "Kubernetes Cluster" and polyline generally improves layout.


.. uml:: k1.puml
    :align: center

.. literalinclude:: ./k1.puml
    :linenos: 
    :emphasize-lines: 4, 11, 31

