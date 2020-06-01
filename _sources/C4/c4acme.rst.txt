.. _c4acme-label:

*******************************************************************************
Using C4 To Architect ACME Global Widget Production 
*******************************************************************************

.. tip ::
    
    See :ref:`c4plantuml-label` for explanation of C4 and PlantUML Stdlib support for it. 

C4 ACME Global Widget Production
===============================================================================

Your mission, if you choose to accept it, is to design the ACME Global Widget Production System.

#. ACME has its **own production sites**, and uses **3rd party production sites**.
#. All sites are connected to a **central production host**
#. Each production site consists of several workstations
#. Monitoring and Analytics is in the scope of what we are creating/changing - SupplyChain and InventoryTracking are not


C4 ACME Context
-------------------------------------------------------------------------------

.. uml:: acme_c1.puml
    :align: center
    :caption: *C4 ACME Context* 

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbuttonc4acme1| Press to play around with this diagram source online.

.. |playbuttonc4acme1| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/hPNRQlD64CVlzHHJqGzi-DhGD9SXnBLD4aYSu0Ec430RQMmlbdR5x4YEAO6-Hb-lJz9TIuxah6dQ85tjOURtdncFTwuD2-8yJO8Vf8gIF4Q0o_x5MVzYqTUAyPL_pkpjLNrzgPTB6U7Pp22PizmWLHR1VU_tnzbqCR-RtYxkXpV3qQ3J3OA09IS8Kvr1WWKcK74Xbc958eMb9kZr7uPma-WNaS1SnYjaU28Tvn5BhIpZoMffrUb5ARhpnwr2-Wvksx23_J5yX_3oHnVN5Jmh6AF9j3Bo9K6dr3JNIzZkjGn8LORGk9r8nX2w1-bVAMuekvqWthMcNWFz289WiZECwU8tdQjOqAupnbGpMgbo4NRXZo00-vM67GSfbxVQiBLhKDr9Q8y690iqLGmDMHjrJubaPqvTGYnO06k820KZ46QQs8JTflhUdMLahChxEYoZA6ICfgI8lOeqTX63i6Tc_Q85nL18t9OcFq7PTLAjW331GYWlccFj1wqaQx8ELg_UXFNEm8TYFAkPoxKtdy04gP0H7kUp6BvoPv9dMRBhhuLK5jNO7UML2MBZofEA3GAliQhW2U2TAb2nfjsKHBGfu_NE7BoV6zOf4ennYOGgmWeM16-1_OQAaJAI1kl-EFnFhBlVrdw_xEtdcZOJ5ixe5-lNtBemcWo3d6VxVXQm8ctNTJDRjlt-1Nv-33____1F14R70gCl2WHlfujxU0airV_JDklR3D5QjbzVdzr-UKj-kzNTLtQCoM9sel6yfsk2AZPDXVBDSH8LD-oUffstIXjzbLRbwkhOMghUZzu2h8L4grm77mUrnnkZU-HDES65YklvPoIZBsGilYHRm_y2_fnNnrgFAmyt42ogSIZh69h3mFTnkhMj_yxx7eUhWrDpYldMzQLBOgar8y6tfKnGYHGxNI1KCHB6i9MyXgT4A9uzt4E1P5m5lbMBJlTPJTS8jvAZzLfkaFx-yoy3DxcC4LY_EmR1jGNcQV8F
                :width: 40 px


Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. There was a last minute decision to put InventoryTracking in scope for the system we're creating/changing. Update the diagram.


Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./acme_c1.puml
    :linenos: 







C4 ACME Container
-------------------------------------------------------------------------------

.. uml:: acme_c2_workstation.puml
    :align: center
    :caption: *C4 ACME Workstation* 



Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbuttonc4acme2| Press to play around with this diagram source online.

.. |playbuttonc4acme2| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/TL7lQXf14F--Jp6L1XJIX4W-Xf3qb1ZmZnX52W7PtCxb5lTsPNTE6qgXhz7NwvDqxZpjUTZze7lx-pE_cNa893tbcH6Vj8rDhX3WBhgzZcvNaRE4t-bgm-ZzULXgYxv9k7D9ecEyNWJquJeFHuOOFdwRBEQhvVDyi1hsd_hZNhiZmbhRZVGoWrHQjVEQ22qaqWGKGf0cWt2i1JqjtmjkuZmyHgC-BBLwHuAbysjkXRIp8FYyV0J2RFNLvLP9_z4ky9SzVWcj6hlLWHy2-4mvhRFjnpZ3oGQz9ESluN035jrzBdgvXrSB4_ibQC9_y2vriF5EvJ66Ab8BEg8qtaUf9vX6R5VxXcdKufUUrrkMKuemBRrAZ6tPD5nnNNxTQiMK156zoNWDvC1L6Ge2pybYJA5uZz6IbwPk5Seat36Vaso3_8thysyHusWooWtfZS6geN16kB2QRbXJ_XVYQXqt5RT1xLRKRetQFKyTLzHnZJgkg3-5cA5PpHhBQauuIZ5UXvC1C9fp7wMyrrm9zt_OGbqahO9dcpYO8NcDMsds1lkfLHCuJAq9TVyFZKyWaJX7wE4YqGQjpB3T0OzMeKS5EqqfJ8sqj1WDOOi-5C4kgakxyshdAS90KvocUet-pw_V0PvohH387ONYWVtopFm5
                :width: 40 px


Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. Add another hub and several Units to the Workstation PC.
 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^


.. literalinclude:: ./acme_c2_workstation.puml
    :linenos: 









C4 ACME Component
-------------------------------------------------------------------------------

.. uml:: acme_c3.puml
    :align: center
    :caption: *C4 ACME Analytics Component uses an ELK/Elasticsearch stack* 

.. uml:: acme_c3_monitoring.puml
    :align: center
    :caption: *C4 ACME Component Monitoring uses AWS services* 



Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbuttonc4acme4| Press to play around with this diagram source online.

.. |playbuttonc4acme4| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/dLRjRjis5_wlg-0ReB03D761uFqJT4NzaQPPdRIhqXOO1WJ7vB74cI8raegH3WDs6xkzNSb8YRATfWoT2Z3F8Vayv-FG_7XjB6ZRL2BB1kClEJ6sMIv9YHgpmK-9B_iVbrGq31ijo4jOcn5LLQNaSUtilNeucy_UcT7FS0jjyoZgIZ7ylHS1-H1wZX8rY55ZK9kk3TWeb0gEqWQH0hk2KA4Qjb5IX4ejkC3WOxSJJM465XPWS3IkuAkI7sVvLWkaVJYp2PV6WgIuepw1VtcN_pBVCh_jHyEVggfkBFe2dGambjC9WYU9rVV6WfqdcM5O2tLNeRGxweyOWheMd8BbIkxgALF1pbm1cu00IRaiHkCjVpk1EZQ-HxXpg1OCjjh-b4wyQIJrRh_fHbSkjqf3qVy7yfED4XXfmgAXAxH1xCSw5q0vwlkzfr51qvBVOY_Z-I5jDBTt5mobTTBNJN2_6hvq5-FB8ABUutnFhb5Nt1YkfDdLVz2QLW9z4q_diZrCSjItdA89DPcgGdAhxlTY8LoXNIkzuhAOAcbHsXaALq1zrny3gh7u_vFxlNG-gUf6yXbB47UMqpwLitoZn7nUWeG2_Uw_LafiQk3FvIzWQVbWe7S-25luYPSRmoMNICxcu_pwOdhpuTFbd61dQHCSUHb6Hb1N_XTyVc--lZ7e_xKxQXIzGB2cQwCOwXFjsiSnDrpUh9e5QeaMpVV6udp5CCIwgqVnID7_7fbV-LzqFiZWCVHIFYMh5PTsepo2jAXhpKsVnyEHA7V55o0XY2XAgABWikZbOpXZmPGR9Ogie3Pj4qUWrQv8GSPnXcFLDeyWR5-7NJsEjq1NNHl5DBNb5GOHKEuRq19aWOGgeJHHIs9G8BN8oC9PAxHg92EcX1f9QMrjJaUZMe2qZdzCLRNp53XY70eDLMPMNDRWD0BKAZtPs9csFhwKt2BPHHMEdKPfovT0qy25dmDzbmHIq2mDyfiqZL9LhMGw3O-KLYkHnB7mDam2ktC_2LjoWMcG4Wnr6kQQj37kj_GIQ1ef5Kk3QWU08etxey4cZMhtIXAbaLgGXTZ7djBxHDSOfF5LTT_WMf6m9RSRCEnEg_fxZnGQKMQ3FVw1BrvCtanEd6tt49ZEtt-Q3M5j3icVMKRSDxuS__h-AZyPcfERxW7v_62k2aEQMYXWoBnJVr4V76PPM08Ihl7UnW0O8mT-4G-UauDD8Bu3XLS8MdfyV4nidzh3iwL6lU_vqlbak8H6MC9DTtuGFzo_4VApySVfss68CsyFJnTDfn1mNjjdprSNSB_F3bl-_FrvVZtEtmxduJfmh0-W3RQaQmtIB9Mk3fvBnGBbtSLaV3KUlcll8mV_p4q3WdlRRM279FkhgzEcnEI8gRKyUaLwBwVa8wo9S3qFt0oJ8ysBqZhWlKnEju4W8pEmu5dtCLjg5zXfY_Chy9dZEdCXBPMogCapVp18g71uI3HAXjhPN7DRaWz-6VnRwnQrVrEJPq4P7luchqiaRxcbPSbNgF_z-nz3pXlEq7leYTbhPy-jO_OV
                :width: 40 px

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./acme_c3.puml
    :linenos: 




Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbuttonc4acme5| Press to play around with this diagram source online.

.. |playbuttonc4acme5| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/dLHHZ-8s47xdLxWddSHAlVA0-bQTQc2xHnjWk-64LDtBuCm65sS6ESuYMbNgt-ZVwoyv9mH2sBF87G-UcSptZMS-en6zxpGfKoHOM2D-Wdq-K9nbJEzV9-B9R_dWLtY1wlXXLsGcX9fpWd-UJ8ry3Nr0GWjcKEHey-giiM6eCXh9rUOMMAvYPRX8piujGiPhRV1Ol1K4HvY0WpNaE90P_CNqD8aRhoPruKn6cd87fF32_Gh-x13_7ZNCwpZO_fYpNU6m5EZUGEwq6Y6K9BFzqhUce-vb4jmPFcH8xiBzbaAmsncjm6ccI_zMgRfEn92Cm00fJUb0DlmcWJRqlKEx4MJh11glE-LeVYb8LQErm-3BnOujfAV_G3myEpNZDc5Tg2swsdHZFHXG6cqx-ZegMBNHBtYouVbG5LQxmpH1SjwMkXaDf2hffd9Mc-3jONv9tg7DT9vhflpI_yPgbWsMHtYSMRLCOhGlMc5UQpBcbBJZTXHgOOvkptQhAHqpEIGtGUC5j8VJ6k32uO_3TXGgrbtTm3oIm1oSLgTHxkEp4xfp1WGfPaXkoMpE6fHxUGLERLvzw5ne5LUafGLjsb7uFJ3F8VLYrhV6yxZnJgpSgxq32vbGNXyc92UjvVsO3LinCg2sNyAC_FVKSa794RZQQ8SNGE84Rs4WxL08hDFFe0AuwbUg4Iq-Jlf-Q5NASlTtJ_I44CT3FZv6qx5SJXVpQ24d8nd9-VZ-gMyOadMz_BuNRsGq4X6d-Pkx8sic_rZCus4_7lfaF1IWbDUp1V7hJSv64za_xZEFEph2UD0d0af4XivgrJ2EdIwVv3JgjrwnxE1nAanJ_gADYhIIo_67_lKVgDNjFAxptYkxHj_1dBs0zRxtJGd7Oh6dSi4bcIP_Lw-gSAc6UFVklRY-g4B5mt2kdZsORuqRXbN7TQQ1bwFvr_sdzypiq8gtpzeWGORzEs6H4hIOYBrs6_5eWDp7MIHUq9QBJxojdVxT9rfkK7pGll96Rz7-_-z_kNWeT8B2yPdO-zdNApBp6G00
                :width: 40 px

                
Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./acme_c3_monitoring.puml
    :linenos: 




Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. Add a component diagram for the Production Host


