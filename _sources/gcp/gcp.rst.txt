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


.. tip ::
        
    We can take a sprite from any sprite library and apply a selected library styling.

    In this case, we took a sprite "ma_timer" from a different stdlib (material).

    We used the macros from the GCP library to color and style the icon to match other GCP icons.

    * EntityColoring("Backup")
    * Entity("Backup", "Backup","Cron Task", "darkgrey", "ma_timer", "Backup")
    
    These macros can be found in  
    https://github.com/Crashedmind/PlantUML-icons-GCP/blob/master/source/GCPCommon.puml
    
    "ma_timer" is not a Google service so we don't colour it blue.

    Alternatively, we could write the style at a lower level but that's more work e.g. 

    'rectangle  "==Backup\n MA_TIMER(darkgreen)\n//<size:12>[Cron Task]</size>// " as Backup

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_gcp4| Press to play around with this diagram source online.

.. |playbutton_gcp4| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/fLLHRzis47xNhxZg9IfWXzWUWzHe9ZJ3i7aBwXHzQ0k35Yyo5ueKI6f6DlI_xqH6TcHJHeOPi2Zolhll-1rFVEyyjxvhLFP6u8FK23-NTtSqXwtthRjYpFBTPItzjjjq3crbj4VjBolJiD9ojqNHI2tOdUBQVrh-DfU4S7CAmXhkF5ecfFFP6wahrObzT4PZQPh6wCkMfgTsChQTHrOgqudrRQShBodm1Fftz3jZ7wMk1mTfSSULMd_i5Bhp7CEu_g1h4c02lFB6ydf8ACwUiHcxoEwt2CPlqK8G07PIAT280hm14WlXmPhc6UAyK783zBVSIdHNiE7LOzVEe9VOpQ1IaaHsbza5EsHopNUENDZDvrMKRf6qhMJJAlaWKOJi4g1XtwJF5AGn6wdE8chKQBbw0Nc1QRX7AybQnKHJ9YyRj8FhXQFYjTpoXbJHw9zQXDQeftwIGS9ehDyQylEcxHNU6Ez9NY4jXeC2MKkAKeKW_rKAOF37ZjBDuPyCwFUfLxa8pndajvR45YwdLyZV1a0Pz2_YC1l5663VimF5ahAgB7_mqS4HpscOFOW2lEHQ1gcBE4JRD07SMVCdRR5d2DxUr1ZEL6GyQfVYQBxotFRyOOGLsh_YXW8CzZ1YVrKmqv9lF_pFK3T2a2SzWKEindIax-4vRjbYF9r5mKeIRBJ92888ed0XqgYVYz5i5EUdqA7ka5W4KPna8LAVeIArk0wrG3lBdr_WzZEbwAt45sI33mGVulnl757KMHx7rpD4iSFZOhWFubtmcWjWeynck0MSwMo5Hv_z6BXlMQvhXG3vktTHvwyQbZVh-r-M7puMWjl7sYBgjryrOzTE_erNF_ou-59Qe-6UkyTlrwnVN306EN07CSGXTTghz4-bKSPANHTvjDCM3yRzuWpsR_cUe5zzpkAfVs_uEdoz3kZOh_HBDHpClsob4AY_YVa24bsK9TREEL6dJ355yFGnoquYHPypnoOxOqjccIQUI7XnrCifBHAeyJJkOTIyiHYK8t5OCgROpmEeBk6A87Ew0jdHXpq2pocPnTC2y-vqH-y9G3tnBm00
                :width: 40 px


Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./gcp4.puml
    :linenos: 
    :emphasize-lines: 1


