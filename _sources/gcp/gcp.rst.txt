*******************************************************************************
Google Cloud Platform‎
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

    In this section we'll look at a Google Cloud Platform‎ icon set https://github.com/Crashedmind/PlantUML-icons-GCP. 

    PlantUML will access it directly from this repository (It is not part of PlantUML Stdlib.)
    
    This a Type 2 PlantUML stdlib per :ref:`PlantUML Stdlib Overview`:

    The original icon set is from https://cloud.google.com/icons (which says "*We are currently in the process of updating our product icon set*.")

    


===============================================================================

Original
-------------------------------------------------------------------------------
.. figure :: ./Minecraft_Blog_Arch-1.png

This diagram is from https://cloud.google.com/blog/products/gcp/brick-by-brick-learn-gcp-by-setting-up-a-minecraft-server
    

PlantUML Equivalent
-------------------------------------------------------------------------------

.. uml:: gcp4.puml
    :align: center
    
.. note ::
    The icons could be put into coloured boxes as shown in :ref:`Create Real Life AWS Diagrams`
    

Find icons 
--------------------------------------------------------------------------------

We can see all the GCP icons here: https://github.com/Crashedmind/PlantUML-icons-GCP/blob/master/Symbols.md.

.. uml:: gcp1.puml
    :align: center
    

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_gcp1| Press to play around with this diagram source online.

.. |playbutton_gcp1| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VO_1QWCn34Jl_eha0xAwzvIoXH98O2yzByfQNGjisLWo_VqA2iqXa9COyMQaEQjXjr5oE4RwPg73vxmihW_9hEaRGCUVQMTBupwK-bR5I6pQQe6veoQAXIN2ab7iwtOziHDwyX0eg4OT8gk58ykMH_nF1vzpBQNAr5o6P-3zigB4zOPRyg_MAs4NbXqmvp_BisEvE2wuKo6n5w0VRiFe1V61XdTKqWSJilVGrjb8mvaa-l8N
                :width: 40 px

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. literalinclude:: ./gcp1.puml
    :linenos: 



Gather the icons we need
--------------------------------------------------------------------------------

In addition to the GCP icons, we need:

* users, clients, mobile icons; we can use the awslib for these
* timer: we can use material stdlib for these 

    * I used :ref:`GitHub File Finder` to search for "timer"

.. uml:: gcp2.puml
    :align: center
    

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_gcp2| Press to play around with this diagram source online.

.. |playbutton_gcp2| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/fPDHRnCn3CVVyocylkoGkkPzGcZZn7Y0GaMPUApIYzjQooMdnCTzVTnatTfnPI0gzLmxV__g_EMxIMmYzwrJ5nOtv14-rek5vB1ZxjArrj4Ciotnhb_t2MCJFAFdMHDQNKUJTcXRybOldF5yF_zyHQ98LmBHhKcCKLjAh2x8DwwtJtGjiGvj6_oia_JtSpdiUaPTkz3RrLtl6oO1dr5_GHv2V22_FJHGnC4uj_hMEqol_KU9gmz-InxFY9SSejaU1YhPerRfI_LzXn1uXn6o0J2GS-0HBN00CGjX4qFxA4bi7Qr1lj54mdGDQzCyzDqKzXQdAJIEq7EQgKlzFCbRCoHfqRS_biMwTwDdIsexHnj2cwSR4HtkBVwSaxHXJUwFYYrwZCOTIPIwtqzVvUSK9dUHqDiqaPymUQFc6LcL8BL3lSvthKgGsYUoeE7h8FXHoPmyDj5i-8YXNgn9zI9ViebxVOwmnFYpmBCCdcH2UXKKkZr7mdzWRgsLBdc2WUBIE4MTRcPrcahBN48jNfpSgOYWY3BbU6Mha-o4yJulONgUfOWoO-orgiQAg-mnnca6D-FWGmla5k7_FRxuzMzq-Tn8aspfBm00
                :width: 40 px

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. literalinclude:: ./gcp2.puml
    :linenos: 



Connect The Icons
-------------------------------------------------------------------------------

.. uml:: gcp4.puml
    :align: center
    

In this case, we took an icon from a different stdlib library (material) and wrapped it in our template so it looks consistent with the other icons.


Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_gcp4| Press to play around with this diagram source online.

.. |playbutton_gcp4| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/fLJHJ_is47xFNt6_l92VrDRQ7X5Ki0gcQUjMKH0FW2etlgPU7JkodLLiud_VnLQXBGumhLBjNEwx-yxVdNFXFBU-hLNsJU1AQeIV9xCPsR3sld6dZ5c-7LNIhzjbwz2MHdlKVbIQcaqiTsiKjTI2pHJN_cxwsr0ImWqf2QkvysYPaCvdtwGkLIjUipFQ9wQkZHurPBxtaxDfFRA9CgrONBUwz98Izw1_HxyrTYDrjGkG5hTSgSLDgz1znX7tnPMkI80UyDmRowjTGT72YCtOINQxHZ1-ZHQ20B2LIe565E0Da5W8AsjgY13dXP9BeB_bLg8xXIKlDsqpW4vYDu1IIHBPZR8JzbR96Tyw2c6Nz_CetJZfcykwKN8bKOJg4g3TkKcVFaXjbb9zYAXGe-Lg3xA7gRb7AybRna9JBYzhjBlG4qVDQxZbDQcYqJyt28rHpvsHGS9fh5yRYlEcwHHU6kz9NY4jXa61h255gKEG_oe5CFXZI-Ncy4y6zBlhL2x2Ee3ysfBOmkNq2Fdt09W4_Oku3Gvox60lsHl5bAegBL_v6E1sFDEWOX4tYkkbU4qGGVq4CBFcJpfYnn3IU5DXcAd8U7HTYYDxxhdjEC8ESxH_nGC56Bp2YFrBoKn3iTtsFrDT2a6Hj0A7s8t-J2zXFRoonQ4vY89DIB23GqOGH12bYvdsxtEnRntc-IdSKFTMM0HHddGZ4f-X8lLo4Ng1Tf371mlNzrIY9ndso7On46A8yxznH547UTo_pX353ajtiRYk50Bav-THZKSDqyl5xI_Jgvj2SBkfBAB-_gWPEtFoRppzuSVnmyGQ3RVSRPxEMFTop1Zam1t45DsOqoyrfp1yM4iXK3-9uHWImvSbtlK6nJ7hOuhW_kvaxpAbO_RKpZxm9QjC4_SKF3ww0aaj4gW3CvxXOEPZCwX6uh3aJB5_3A2-X2yhkTCTo8u_buJyHCei3WiCs_T7kY10Mwj_0G00
                :width: 40 px

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./gcp4.puml
    :linenos: 
    :emphasize-lines: 1
