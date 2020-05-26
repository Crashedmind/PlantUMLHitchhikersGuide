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

 
Find Icons
-------------------------------------------------------------------------------

.. uml:: 1.1.puml
    :align: center
    
.. literalinclude:: ./1.1.puml
    :linenos: 
    :emphasize-lines: 7

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws1| Press to play around with this diagram source online.

.. |playbutton_aws1| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/ROqnoi9044RxFSNyHI1f_bn096AXXOAWOcEpIIRiuEnks9qrhTVmUfx4BKG4xGQ-z-OrKNIGP5dzaUiuzGWpFKMcjbwSzajlhNVpxoqFOnAiDVF_cEqVYFKjyIUXcAB4CP1WL6hmNZ10CMJ8QOjb1G5TZm5xc4WCx5WxEMutSCKGoJieNaTPdTt18An9EcFeWk5nkqTO9SfryMzHDVbVBZy1_
                :width: 40 px


Gather the icons we need
--------------------------------------------------------------------------------

* For the EC2 icon on right of the diagram; for AWS icons, Orange is AWS Compute so we look at the compute icons. 
* Use our github trick to find "users"; they are in General.
* The green box isn't an AWS service - it's showing a mobile/laptop client.
* We need "Traditional Server" for "Ad Exchange"
* For the box we'll use a Deployment_ Diagram shape; ```package``` or ```cloud```


.. note ::

    ```autonumber``` does not work in these diagrams. So we will manually number the arrows.


.. uml:: 1.puml
    :align: center
    
.. literalinclude:: ./1.puml
    :linenos: 

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws2| Press to play around with this diagram source online.

.. |playbutton_aws2| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VOw_2i8m48VtF4ND544iE8jKYgDJ5UTBSsZWafHBegzlg8lGqE7-SD_tW-jY0axPaTXOFr8ss1pX4ydgzlmO-k1SyASbAs3A2LiWsaybNL5Sq9PMZITwPA0_HLpwWogrQoI1Hf9bIJY-v5RS8t9KSw_G6uEnoGOFD22_aTNYKabTvnVLRrIuwD2RxEWB_
                :width: 40 px




Add Text To Icons
-------------------------------------------------------------------------------

.. uml:: 1.2.puml
    :align: center
    
.. literalinclude:: ./1.2.puml
    :linenos: 
    :emphasize-lines: 7-10    

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws3| Press to play around with this diagram source online.

.. |playbutton_aws3| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VOxDIiKm48NtUOgngmZY1TSYztBfKX2gk9uqGnkO_319R1_VMAa85HV9WUzy9-IS2qgfdjMD2oDNI_28IsPdJfVtuHgzZ-7fsBKYrK8dPBvFRVs7ugDn_AynKI11_gMe_lgWsxc3Rl1eQOM1vCEDr3K2tQrwooHPRtSZM-xLgw1rnSM0_3KYqGVIp8k5VXrd3DFFcy_RH_LtDFPI3Riyam2c155W8RExwap1Li-V_
                :width: 40 px

    

Simplify The Icons
-------------------------------------------------------------------------------

.. uml:: 1.3.puml
    :align: center
    
.. literalinclude:: ./1.3.puml
    :linenos: 
    :emphasize-lines: 3

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws4| Press to play around with this diagram source online.

.. |playbutton_aws4| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VOvDImCn443l-ol6FKKG2vv5MagFWX35ysGpjWEJ3oQ9xSythYm8hZqa0s_UWzcMYbfRaE66uoJD4ppYkGYxpUxTxbC8AJwjxYo7BFp1vEzpxrUaNkTMQOCY_oaXEPQhnf4YASelPJZi7qn_Tp3QW9ukO4a_UQAn4nXlXxT2MipyTpBFPVMgwBboYYZV4QdvGxgvyt2uJ2UCHrh2v_bGypCwUsbEk9n80NE6f70cjxZ3bg9lGRu0_
                :width: 40 px

Connect The Icons
-------------------------------------------------------------------------------

.. uml:: 1.4.puml
    :align: center
    
.. literalinclude:: ./1.4.puml
    :linenos: 
    :emphasize-lines: 13-17

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws5| Press to play around with this diagram source online.

.. |playbutton_aws5| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VP5FIyD04CNl-HHZJn5CYbKlHKfhwS638CG_vqrssWpExiRTJLCGlxlJXj0YrKjcClDxyrx8F4JbOsiukI1RSQiHxbKNcChnuhrOEcESdPtT5MGQfZMXpXlHdu54tRGHnuhvByIualXVOeCMlU8J95aj9sbXbCRT5Opw1WhqMwfm91CONIQl0Nr83q-P7EgmUl5AKoHd5Uz5wDE5NksgMjaD2hBGCBmDYgT3oBGlCdjkIwPGemVLDE0yT5WEREyCcNQTpMRGQwPmdSCR1OeXwIUGUThKKOYZ-HGcEHJxtm6ghVO9a-FoAEW_U0etEJoG1e-VBOO8O-b2usp0f2SWOrp7amotShrsdJWE8N-VlClXqJHo9uYvNAoOgW-fP4DKpDBX5cs4hy6Kz7SoHwjRmpy0_
                :width: 40 px

Change the Layout: ortho
-------------------------------------------------------------------------------

.. uml:: 1.5.puml
    :align: center
    
.. literalinclude:: ./1.5.puml
    :linenos: 
    :emphasize-lines: 8,9    

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws6| Press to play around with this diagram source online.

.. |playbutton_aws6| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VL9BZzCm4BxxLmoz42IIYWKk5LfjgNhWW8GK7cSddZQZZX_OJjCAyT-PD4IjKDbBPZpVunihVafPnznRLY_8jTmRX0zwI4pDSlsZtdXhlNkyYzLa0zEEq5H1z7T8eWvzngLc_X_5-eRuMSOU7KRDDnJr4jA1ND1HMs1ocCy18NW-ZmTr3_GnTrwfxUQXgAqsU7eDYwc16kEHMbp811QlrBU4CHMNhqmkTOQ-HcqeatUQHn76OcssfxRJRez2MHkOJxFYy-LsnLHazgLlc5A74NG8u2CCsCpSAHbAumTNFiAaMS6R2hvJefp-ca4PQTzbOLp3L_1GGJt-Hz1zEswehk1LC5ru1Myh-4W68lxiCMLOIfU2TmdLn82ISPTlTdWdxfqV975Uyb_BznLyia5yaeIBOylK7gIIa-V5B1qUqMNuDOUI-QsUq9dnuQa__
                :width: 40 px

Change the Layout: polyline
-------------------------------------------------------------------------------

.. uml:: 1.6.puml
    :align: center
    
.. literalinclude:: ./1.6.puml
    :linenos: 
    :emphasize-lines: 8,9        


Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws7| Press to play around with this diagram source online.

.. |playbutton_aws7| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VL9BZzCm4BxxLmoz42IIYWKk5LfjgNhWW8GK7cSddZQZZX_OJjCAyT-PD4IjKDbBPZpVunihVafPnznRLY_8jTmRX0zwI4pDSlsZtdXhlNkyYzLa0zEEq5H1z7T8eWvzngLc_X_5-eRuMSOU7KRDDnIL3kI2Zje2ayDy3WZ1ytayg9Tm1_KnTrwfxUQXgAqsU7eDYwc16kEHMbp811QlrBU4CHMNhqmkTOQ-HcqeatUQHn76OcssfxRJRez2MHkOJxFYy-LonLHazgLlc5A74NG8u2CCsCpSAHbAumTNFiAaMS6R2hvJefp-ca4PQTzbOLp3L_1GGJt-Hj1zEswehk1LC5ru1Myh-4W68lxiCMLOIfU2TmdLn82ISPTlTdWdxfqV975Uyb_BznLyia5yaeIBOylK7gIIazV5B1qUqMNuDOUI-QsUq9dUyXy0_
                :width: 40 px


Add A Box: package
-------------------------------------------------------------------------------

.. uml:: 1.7.puml
    :align: center
    
.. literalinclude:: ./1.7.puml
    :linenos: 
    :emphasize-lines: 12       

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws8| Press to play around with this diagram source online.

.. |playbutton_aws8| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VP3BRnD13CRlyrUOlH0aiX45BX6g6g8AzO24j3pEpewRjU9vC8-cLTN_7IVBAfK8lUnuxD_tVPwzoWLJgKxCA_QzL4lm2VTPUBDO_UhMmRdWBy_EEdPH-9R9jb7rPo1LnrfeWIB_GrpOiBn8RCbJGda9-P92ZJTzyFaPPI3ls4TCw43OKtc81378m-5YNf-RXbI6O4p4VeTRWaOV2Mi9rJRmQAxN5xFEeQNxjz2C1NIKxhYdHZlGl35Fnlp8bFBi-DNcyPoctnDQBXmyoa57QRQor_VzW7vBYgmiJBT9yVNuSsRZeRrlTIES1qg0CK98iAVDn8x9CBTXx-UNC6gMyAw5dvovvBzcC4-y7OeIf_0bNBJG5Km5iFQ73SrfU1ACRrx2-nO-iuL4lolb0WkjSWm-ana9c0lTbcSxV53t8UmrSLpoNykFBToug3vPmzMn5-vtUhBF1KMqeZlo1HwdKBPFvegyhKx-0000_
                :width: 40 px












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
-------------------------------------------------------------------------------
.. uml:: 2.6.puml
    :align: center
    
.. literalinclude:: 2.6.puml
    :linenos: 


Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws2_1| Press to play around with this diagram source online.

.. |playbutton_aws2_1| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/hLPDR-Cs4BtpLqnpaGhKkrZxMYpMTPp0G98sK84S2reQoq8eKg2e66xH_zwHA5AoGwbeDm4SYU-zcQ7cW-2tsd1jcbAm7mgPYYP3-9cVQb7iFwzVaeqgIoM_1hcaA2jH70hCFbLa7n2HTTKO_Co5c9AKQb-8MKME4ZKNSv9xhPfgbofPpwaIepJFPsCzSacA4gLPo-nUlQ6MNAQp9fkcDgf4lPLvRpeV83qM4X-GQrd8V4xwXEQaz2kfQ2yR9GsvlaLHqAREStQttF0zhsStlQweSYatXP8xSfphxlL_M2HFoNz8JB9DjYKlN13wYroBtDigiyXLgUikx5S9whSYnMJrgP8vYwOsyvnOtZbzuEK-uvVOThDaqLITDq8rsGitwT4QpNo35LpNCo7P8tz5RUdeqRRt-hVTFJTuucUBpzPs42-jsbTqtMXAnx_buBd11ZiHOpN5gBZc9GZQfZbN29KIvtR18WYmIfkZeheOLO70Wu4QqzOni6ZnFN-iukah9GSe_t_iP6tQVCDVhAzxl9CvrcqW-gwVuCOlWTOt1C3DZrwxEJQopPsLkXNygjCZ6Mb-RVStO-5kYfDLOdXEngHSb_nFiajMq6FmIvE-ed5UABCn_UpE1Zr1O37e4k_ap3PVR1-_woBFKRTcBmbO37eGxXhPvVZArD6BfbfyXN62s7ZHytvhpB_18bCdITmeOSn_icV75UahJv6F7rPwbxa7hdEyAmHsURhCOCT1IrvaqPac9HTYmhJZPapfKyLKM4i6Z1ab9VOR7kMFS9ACjkiu81B8BGcSauiEy9_W34ZKOLTkhFhAnQxaEMwKV4DTKqKiwjg6f1qFWw3tyhwpgBgPWepNHyoweOUzQcJ6zTaFwEt3CysbEqTYMduXQteu9sDgEKsjFEM6S9H6M7GjPllsiZ4cPJw3yxAhWZFsBi8WdwWmcy3jo0Htuv5Ga63zsGHkWuI_nKE1CBCz4gXy82ykSbjp_qL1UXdSoi2l64NSAsDK-R67oSnHtYMWlZZ9BNHva7UZJJ_QvHqlHCqFIDMrpGeE2KnpVvxO31lCEj-1CyKBR7Je9C4ZOISFg56ck9DlAkLkbXqA7fwSPtiXYErZs8PTUv6_JyIM7u31X33emTQEpFnLfhVowy78Gx2LMQKAQNfRrdQGxuTtoMxfvJozcg7PEsYO0jS6ZCtEW_VkzUx5C-5Qip0C2u67DlvaPTaauoFQih5eKkcZ31LaqV3kQL-NOGe_zZB7XejoFBmEZT5XfnRpq_EKnFJxCcXerNUBkrB7xeNWxWbFoXI7_fPhnUFGiB27pHZorQDOhFtd4UUSVKEPDQNu1m00_
                :width: 40 px



Second Pass: Tweak
-------------------------------------------------------------------------------
#. For clarity, force the cloudwatch branch to go horizontal and connect from left to DLQ.
#. Use ```together``` to group the SQS and File processing icons.
#. I did not change the boxes line style or colour. 

.. uml:: 2.8.puml
    :align: center
    
.. literalinclude:: 2.8.puml
    :linenos: 


Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton_aws2_2| Press to play around with this diagram source online.

.. |playbutton_aws2_2| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/hLPTRkCs47xdAQO15bQ0UXSRlmQBTPsV6aZI3RH5NWeKj3IMYL2aG54nqiK2lKQlrvDq98gKR4lgmoQ08l6RRsR8RuOqFvUM6rlbalqaL2Ah5E6IxqifDX-MJ_5AvxbMdmPjiSWBARO2q_S5-G-GoBkeB7xWKevHShqHSfAHeKB3vHJbrkYgM2TQbLEis6h3iybSzrmH8qTbbogzrIze55V9fCkgAgtEqLohh7MTJf3iXC8xv4O9bKrH7z3kjNac5irbfPMbq5Se1KtgTShlYbk-uUNaf9S5LIxXLcYrfi2PQJvx7itVpDVlrfM0pRo4JUcn7SLeNaI2yU9zeJ8s6uaTFyRExeFUyNoJyaFiUdN1PcD5M4bTfK_S9ZldDA1yV1rVvrn8HpWMEoRQFNz6uyopUzTxoo_hMsvnpryTFYbyHxvmx23tiZ8an_zfy5XXXGs9iP9o5Dpm72HDqxuM28MMh_M0pM30getTQQgBrGL8t5eeCQa30vlDV-IF5Jnv9d60zFzphKfRwmtVM5ltQAqoBEj4jAwVuImCWSPd1C3PUU2kTfMgjNDKFuBVJB8Z9yEF_RupDjnDKRo8BS_8cPZBdFz5Vl42MWn-gP9dj3uAAHlHusRMyGa2Xq4ZlASprtoHUtqr8ilGr6vFCJWCMX1kAjLeVEJgpVEgc7-2la2iFsZjOMeiVC4yrNj5jfvWB2mPBhsvNvAsz9HwztQrjpf3kqC3txoATznaU2CaDfeTgjdOe3OUAEfTuvnBEUBQs2PSQTboBAqp3ZWpqYSA4-vfIJXHUjFrDY0ZK5WY-207tH2Mu1s8r617OHpxACGwvnckj7f1Kr9n7EfRYAYD7Jf26-MaoxxNbKurfBpSOTgS0B3HbKgvUGsxzUhkqHMjKIIYuKTofvUFqZTTZ9iMtXHsP4z7c3VjHfruqXcZD2VXDEsqueoTPEZe8oLc8xZRNOEp2SXfaf46O2EuIpAybW0Df9bi4dPQ-LDTGkQwvc55W-QBRYg3zWMZZ1jjhSxVzc2PEDSR0Sg3Ozr1XwTwixVfeLdUS25BlaNtgq80UEHaEuS3nIbiCQrZ3nqgWU2oGqCPF1FMQei6LO9hzQ8JxZUpHw659pQqknr4xjLDmuq3ALmk8cVlWCw5C6Z1se_SmhsczGhZpYb0SAtIGWjbMrzMTr3eXnEnQ_F5j7anOMOdKBSBV1imDhaVGlJ0zn_1CbnhDWp3NEAspZzQMJPg2HbTsIQ8bpxBSHtPCN1C3PNgzkNRtlLOTu-Eki-kLHfiNsDXFpt44JqVEmwDVE-rD-x8Vn3SlE51Mx5jBy6Et4_TzG7rHn_tQjG9MVql83u3OrkjBHfujnKI5SynEWSgG8e6KzWBkuClaYlx-_qT-9_PT-r7TFw7-hf3-5LGhfqWcV_z-vyIRYkH8bWT7DbdYbVbyZy0_
                :width: 40 px


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
-------------------------------------------------------------------------------

.. uml:: 3.3.puml
    :align: center
    
.. literalinclude:: ./3.3.puml
    :linenos: 


Connect The Icons
-------------------------------------------------------------------------------


.. todo ::
    finish aws 3 diagram - figure out best way to do boundaries
    https://github.com/dcasati/kubernetes-PlantUML uses the c4 type boundary macros 

