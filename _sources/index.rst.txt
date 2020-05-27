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


.. todo ::
    skinparam pathHoverColor green





.. showcase-begin-content

.. |playbutton_index| image:: ./play.png
                  :target: http://www.plantuml.com/plantuml/svg/SYWkIImgAStDKU3YAYueoYn9LL39JImgoynJY3OqCgWmD37HDpIBLQZc0j1YTykjipeOWCzxDPX_7Kh2tFybRIJILB7PAtJIxvrfkfonyo1vGKpxh-ByCeVhlytNv-oC--_Wm_iG_3_oty1UsAjxN8x-7XRMkeUDvTsVmavKunxthELFOUigkoz_0dlhtjaRVVmHBEp2TS_SwT_3swvxpLLs7yDhrztpAXyVms7XkcNUTHk0jc5nOrJuZIknSBZB0BWFnpttBeTmlSquODw6_HqMOK_k9eGmGhkm51ntNOc5mz6VONLXjzL1tNtOodfHdy798Y00xy0-MdYwUx3aUC049aWRi0lntkbzsHq-I9TVNDY1nRt0RXyUvqh9Q5rXtyD2_hBJaf-AHycTh-e6FBnmBtY_PFbrq6om1FicFBpu2Upb5wbPfxmDXyzWV_WGJSd0U_0mFuTzRxRPEx0RwaTmq9y-P0Ia_OgFz2aSv6Skc8W2zoquV0vBNDS08lKjsCM_WAF09XlmaVu6zh-5VHBPmf9VmYB_5WuAVx9awdLXmcThxVmjVE_r_gF04QAe3BLMPB4tuG--5eF2YNkZMhAaL1Hw2_xWGK3XWBt3P2VDMx3Alt_MqypBSZjF2yDx-4ZlUos8BkX9aaVIl4fV52OY9gWF5Xdv7UmCV9Mbh91ogIEbJ6tQ8iW8a12Wf52844aEQaLYJaT-1_UuA5d0c4jvW47VifsEHIv9fM5AfK85WL5iQWt2E3UzXRs5PsAgY5A85-sMG-GSOynCIKwF2NZ22DIzarXuezSnPKqfuT-RDXzJJDZoNBLYVS9u7a-Oa5ZXTTAth4sRFQpnxJOrPcYexWYiO6HY1eNT6jRaYiYiRYnnOsCUaT8tZEqEDsgCc0USIiaBEZxKcc8YAdBlalTJrjURAgp8qvNm0YPYoccqkbO4nBg4WOOh90uvvU0r8UNuZxyuXUbApZjy4X8aD-2CX8qXNs6PgSJC86rEG6LeafW14OhGQzV0_GRdauWXz06xMg4nbbktMTWcjCoHYb4VyJDYpN8BSdYXZVfqqnqkPsidrpcTKa6TdnVu59GLhqA760KiQIuIWux-Kcmg9QaxKtzWUi2rSpjF0eLx1a90IA_iT6Uevc41Gid2YfmhGWx-cH1pvTQmfFX8w1Rs4pu5RfmdJ4CX9i1IgwgMdI50mZhP7xegFOj5RX9-qix2BKruVBR820EkrAIjqdj0KfRlQOrgjh3GCEcOAxMVaFR5zmKC_MGSCW_O8GyAILwuDM5NcSMyojh-MWfmipbrZDt0Q60QtD2_UXMtiHoAsdYT-O5maOKcrIvqwqkuTc6amrzP6aqypFx_M2I5xHsqASWB-W9pL1W4qHP_LHHulEW4MgRcIjpQclQ7Nz5IY8N9Fs4ckSbVohTPy1eMwldHUcnf-Q8CgMBJCB6bJ_w6yGTM1xz86jxaKDjv8Ii-fd5-o2mX45hcxeYNX3nlDPM2bZwP7l3nXCKb-9h_fGKcbE5UQwqq_v619pm3kcw97UPUEEe9N5EoKqiKCh3EuqO0zOlc2KrWlD5KKaQQHLfPw1H4zlByhCju4fgnn8IFCucL9WG3o_t8yhM8pE9EM6WJ0NCgf5112oijhdn7XoYPj3IZe5wPiMdu2UUcVNO3xeM8snE-qrXI0KGiDxYXoBFSHrALEL9IgZNhCBxpW0FLKdBi0dUep1PMsW249UUIywNLZHkNQ51n2vmoAp77LD3CGIfkmZfMD-5UvmAXy9ec0AIcUR84E62RLEN20RV6HfLn16VWeqzOPI8MU4rFQkR9nYDREEMAZVBXMM0Jmkp5NC8m90ClwVQK6sCDtZa39vd7CXXtu0lCaEtpVw01knUO1BxBXZP53C1PE0FoMKLuXNbM-meVPYSH0AaPU4dFfQXXYMwcA9nIGOIYm2jCLGPuWREu4vRa6tpljxgTizDCEALSOR31kIjCDRbR8e5xWLqbQSoQ_eRFXZb7R-0w7_cbnnRMAHWEju3vl6pQCX0tfZNzA1hIuMno8sMTpO6jKT7XhU1ssoqMe7_IaAAx9F6YhWC6As-kuSKsjIAIj9NMSd2t724iXFkR9ca1vwh2MYQwD5JYTdECh2gsCe3Gx-3_qMftEwwhEXp0xy_J1FnXSmcawwtEkszCd9OqqpLhh-tvNumgMSgle8P1XZGRBF27RiQHl5dW1bksOhAMwlHdE1EFq9-v2Na4Zi_z1bkus91LVTJVmHW5kwmgOdGiZ7TuZKnPcEMwUBV-7s3w3hPiwZ9nMUYsts6AWosgfPXCH7FdvF0ZtPz5xs-r1KVWNq-r1KMBJXa7lK_w3ekgNc4WFaFf_Zgb6tmFYS5CY5XixtQ7VKsumhp2zzpXUpOMOJ9O-sxq7Ru72IqqWjjVmcQFpAzGsknB_89q1huECURixTQFSDxly3VfhRKY8zhwXpGLaL9_b_PtT_RsWVV7v_hiQFp0PS5EHDmVxx6zcAUhQ8-7SyweK-gz-TegR17HChVmJPX_0WRfVO1C2FdjJbU6sGyf8l7m1YJJpAlfiX-DY0g6mtwwaWrENy8v0pD4mpXS631yXc5Ke4J3CDpVm7wUQEjECAoOCpxd-jrrE9iS2biolE1qWyr5-14OSC9tsGTizMno_Ej4ov3JpJKOVW3EVbpfyiZroDXSmb69XiqbN6MFknCcoC7mtDkiyjFEYpk240fdG5vWo6jMbrMsIFXuhCjENraB0DVQLRSmk1Gbm-2PV0duNxA-LPSj1S69UYl-8dc-l7MBjLjmss9Ws9ATUtsu7_5oeSxUKB5o14nfIsLVv9LEgxjRMXx5505ZJa1roEBoUzmj-sEu5RQqfH2O411DRcpmJSxkFYmLRHPYO64okpvCFkcxkvlRS1i9Wdd8281sKkJoZ9CMmCKrE0V2cORS68o-hLlkKd8uHS9JxW8BxIoMntJPt60O3QFsSDbncF5vxfBT3O95sFVJcUoSIX7Mc3lFGoLjJpXc0H6VwvIIc5neeT7SaQxvvSQirHlvN0yvInz8PNn5ZsxsueR05kGvrq-vxrK9FToQmGLURavR1Em_hulSMsMQuL9DLXYWZzOEMe9WCldSO6Qnuw9Q79O1D_75RBA1y3PWborSUwsAI3DrtWcv96u7WcAoqMO3bG7JsGjKNlT2zkbN6BofdYqeiA0KWor-IGEMR46mPK0glisq49zD1zy1keqZeR2tE2VjGN_9UOHm2VmAX4lrTWlFY66p029i1vF7zo8BXiD7vfc_Y8fFXJABnHiao1GxrIe7mDxcBENSSVlFFH_tHJDnB2ppyTwgJA2rUA6ymIWK2Iixx8zdXqNr2YSG38JB0llZzLpKNfKqkp0CiIFc2vnzUM9lB99d_iBYO5JHKjGGNqPo9lz6efwZXaW0KV1sF7OL2B9NH0XXROyJXS66CLxk6US3hdCDVoiHXi5oWnFW9pX16CnyJ6vAwudg2GjVfpfb284jeiku7EOJzjAh5hW3EU4fhx2AFaifViG6d-DAorJx8kvoJXw8W-tnpmLa1XmkzPGXUm13OPFFnmCWbtgKUg_djx8W4XF6_RYg3uoUTzLwEqfrNkfHyMXhoXe6OxMBCUquojVQ1cRkJ5alSBMsTmtzVznwxVl3Z3O--7YFj94oP4khpIhVm___tpzjd45h8p4CXU_pAyImaDlCFOImi8HDe2cba5EQWp9MR7LiETXomz0_NwVJGW-zYCTxJtpw1Mhoo7B5X0467uk1z-QCmsXJB6B-HHyJt1mhrUgSVpqMmGpjQhZdIvjmMg_-pC5wrN-wwxPf92g1fuj2l7plBQ7TmOspWocMXO7NaXMKl8T0a50TfHS1TLX7cbWiQ0GIYvOWJ5MfAvanXzewqu0b4-p0uHl9Gi76oXBgsfcTsBeVy3jxKKdgM4Quonbl8noFJlMQbtq_9CoEJ60ndULAEtSS-oUFeeVzmvPrS8v7Ilb_OKFz8-ajfl6GgxF7mR5G_jNid0OFsytpvdG2bgo4fklgfT3y9J4b-0y0
                  :width: 40 px
Imagine 
===============================================================================

.. tip ::

   |playbutton_index| **Press play** 

   

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

|playbuttonindex3| Blah Blah Blah... **play**!

.. |playbuttonindex3| image:: ./play.png
                :target: http://www.plantuml.com/plantuml/uml/VLNlQkGs4F-kfvWB77NWuetthd-Q3-NI59h0fLt8XdufB8eqNelOaf7acAKK-XfzlJv9PoHxDybo-M2FD7z-C_ERyUxd4AMFGzSAyKvZRIo22t952cXYxCF5Ok7bM6vDR8Q78Q1NpaQqiLIkMrnv6HhKdR5wiMgbZVUtNyvSZpQW6ho9E-bLOoAgE7XSdXcA3OjEXeXUl3DMjOFUfrjSkQvpjkpfV6oyfymBsRPVCLzBhqVfyGsNMnFK6-Oxz4zlfhWpyHcy-AQ4M-btO098-0MViAM-FHWBiK5OUQS75I6Yx4gu8qqZsV4FOigD0QfpM5s1j9eUkBJQEwEXRvp5af5_TWyP-5PQkJt0NYhb1Xl3X7kTOCb9pL1cjSUuUU9xOEtD6hR33iR6GUlS8-dgY3uXXjHs2HonRd07D2ABNBbBTejnTFuHQFWVKf8d8q52RJoEHCRiTcC9a7nBGSm03ok8wBP8DWz_2U9mmxkpsNf4kz4pNGLJ-05EM9oGV4uRt_Uydfo-nc2jZCRPK72dvCo2WwZRzHIVXmgNlA774BJEnc88cowpN13j54HlZdt1DIkcMH3EtzmarMOK7hMfCJn6rnUzef3gnsLPVVT3MPNLEKCSnf-wlPfgQcNF8Pry5RFCQTKiidUUSM5w5apIpihEABXPiL-sGbNn9PrVXicyR4Tnqn9IQQy3yueKMRngAZdVFn1F0qnaBy_Byq_mPNrt642cZ3ZxBM-Jc9XY0ZUZyTZo5BmR8kKPJMqkLo_pCDGKEnL5-rZGG_hVwvfWW2xiTKqYUymhMim7idvRbH-_BvUVgFAFnvYgTOCkqfjiyqg_z1CYVVLdPpz1houWkC5JSkKq7WmJnMnLHhRGeJPI2DghPEua1TR6IfkinjPkRyj3lO0aG57LWLBoPYTpdi45VwIrsGxv0n0YHoMFp9wOIdYkoe8rp9KG6Mj_fwhsv_vm58BUwJRJACHyIkf45-cSYuJslZOjqbfXSGeUhKQFcWg83Sn_3q190rKDxwT3SVgdNJS8roQgfZ6FwF_xvzy0lmv68qIt3nIV2I_zz0hnFm00
                :width: 40 px


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
   color/color
   layout/layout
    

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




.. caveat-end-content



