.. _networkusers-label:
******************************************************
Create a Diagram of a Typical Network
******************************************************


.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _listsprites: https://plantuml.com/#
.. _together: https://forum.plantuml.net/4387/please-provide-together-keyword-group-diagram-nodes-together

.. note ::

    In this section we're going to create a full network diagram by walking through it step by step.
    
    Each step has 

    #. An objective - the step heading
    #. Source code - for the diagram
    #. Play - where you can test the diagram and play with it.
    #. Explore - where you can confirm your understanding by trying things as you play.

 
    



Example Network Diagram
-------------------------------------------------------------------------------

.. uml:: NetworkUsersMachines6.puml
    :align: center
    :caption: *Here's one we made earlier - and you can too* 

Here we have a typical network diagram:

#. Mary is a Developer in the Product team. She has a Windows 10 PC and an Android phone.
#. Bob is an Accountant in the Accounts team. He has a Mac and an iPhone.
#. They connect to the office server, and via a firewall to the Internet.

There are 3 types of element with different properties:

#. Users: Role, Name, Team
#. Machines: Type, IP address, OS 
#. Network Equipment: Type, IP address, and e.g. product model and number

Select an icon library
-------------------------------------------------------------------------------
The OpenSecurityArchitecture library has a nice set of users and network components so we'll use that.

.. tip ::
    To see all stdlib icon libraries, browse to https://github.com/plantuml/plantuml-stdlib
    






View all the icons with listsprites_
-------------------------------------------------------------------------------

#. Create a blank diagram that includes the icon files we're interested in
#. Add a "listsprites_" statement 

.. tip ::
    listsprites_ lists all the sprites in the files you include in your diagram source

.. uml:: NetworkUsersMachines1.puml
    :align: center
    :caption: *Using listsprites to show all icons in a library* 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./NetworkUsersMachines1.puml
    :emphasize-lines: 11
    :linenos: 

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton1| Press to play around with this diagram source online.

.. |playbutton1| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VP2nQdCn38LtFuKp198XCVpZFmKoD4C3WJHR5zVMhKLj-IB9lNJhQ_Jr-YHreKs7qhiTpgV31zg9UjPMiZ6B20CIs2h-r0kRL4VvxnpxQVk8cjf34-1GIO5q6sfnU_QI81Qaw4xParwEjviw0Wc4ngWldaD2XQ2DuTy6-rPSyQB0Pe4KSejNdTlNKYfjnvv_mqitEv_p7_ZWEKwUOURaY19cy1duULPnHeKVR3AAoiYz56E6MXNOBWVCGBx0QcqPA093j1Dgij_FiTqXMCakly9gVKzt2Um1DQI4Jy3lhszYRnfsjTRhqEo0ugVu0m00
                :width: 40 px


Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. Take a look at some other stdlib libraries e.g. awslib_ 
#. What happens if we don't include any libraries?

.. _awslib: http://www.plantuml.com/plantuml/uml/ROqnoi9044RxFSNyHI1f_bn096AXXOAWOcEpIIRiuEnks9qrhTVmUfx4BKG4xGQ-z-OrKNIGP5dzaUiuzGWpFKMcjbwSzajlhNVpxoqFOnAiDVF_cEqVYFKjyIUXcAB4CP1WL6hmNZ10CMJ8QOjb1G5TZm5xc4WCx5WxEMutSCKGoJieNaTPdTt18An9EcFeWk5nkqTO9SfryMzHDVbVBZy1 

Gather the icons we need
-------------------------------------------------------------------------------

#. Create a diagram with the selected icons 
#. This allows us to see and review the icons first with the icon name
#. It also confirms everything is working before we connect them together.


.. note ::

    We're using a Blue theme, so our icons appear blue by default. Yours may appear yellow.
    

.. uml:: NetworkUsersMachines2.puml
    :align: center
    :caption: *Select the subset of icons for our diagram* 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. tip ::
    We can't have the icon on its own e.g. "<$osa_user_green_developer>" would not work

.. literalinclude:: ./NetworkUsersMachines2.puml
    :linenos: 

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton2| Press to play around with this diagram source online.

.. |playbutton2| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VPB1Qjmm48RlVWe56feS4aEFeOH02isXAGjjRWMZIl-kXvL7PZIowQslqTVharIki0iDkmV3_FFDx_b1yv3KYkOXDCs5nvuO9YQxAmtJguxfhct5phS7qZv_pmdY8YjORrqSsaUngOSVY7sx2vRrvVdJJHp12IuBwGyhhYU5qonuTqF5czh19eKq5yGkPB-jQn_ZC4I-7Klz6huaI6j3E86VhFZP2iwCF5DoP_0No0GvDq2AVxXvQvP8gIcuowNg3W9mvp4Xn15oPzw_ESNk_tSjJQiKELNR2VZALnw462brWsLxM9UU7RbVed_0H0url4SwQXohTPDrLR3ZYghQ2EtwoAXaLPKao5IJRAek_GoTenphqhy1kfa4OGadCMirdQRrz-KArx5IrjwU1BCDOGMhhdJvN8ZPBtWJ9T8-HeMOopq5i1rmTMq4x27mPYRjpNhIPe8aYcmkQy5Nrz_uQm_pHEhwdewGtpz_9VCnauVHk1cR1x1VpkKF
                :width: 40 px

Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. Change the server type to a different type of server
#. Change the Operations user type to a different type of user




Decorate the Icons
-------------------------------------------------------------------------------

#. We use the default functions defined as part of stdlib that decorate our raw sprites
#. This makes them much more visually appealing.

.. uml:: NetworkUsersMachines3.puml
    :align: center
    :caption: *Decorate the icons for our diagram* 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./NetworkUsersMachines3.puml
    :linenos: 

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton3| Press to play around with this diagram source online.

.. |playbutton3| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/XPF1QXin54NtynMA8LI6nWDTTXL8eLaqnT1cLp2AT6qzh966fwSPkkjlzFVw9PM9uuGsSbO-ddCbtSTehhCObZA4hhjms5A4IjciwmFbHSRyiU_PpAiTYIyF9ODjYe8eAvk6_ePDzd03HTUlWuboV_VbAes86ROmoK_3rfF0Ic5ykAAwDlU3oGBkBYZQKDpfkFuc3KEAgx7o__8-WtiJGaFV6dQpOPo9t56sP_Gty0G-5o31i-wwT-hGANVLRqgbpOw1k76O4D88rYtnNYs2UK1OL11OlrZ-kySXPOHIpBfftjwblYsAo7apc6XsO7tUlzQh3la94rayZkcGzv96_O8RDO8Pdu8LspbQ-nIXdx6Ho-09h4_OAFiLCYVU7yiUYczcOeJ3b9oAW7LRDOwkrruVVnk9BJ5c4u9--QUHjI4Lfq_qsXZRb0IiBhSK4Cq0lLICwC1mQYRnwkbBKnCuKuhgyWXw-ID-zr2t9DPxseF__FgTrUT23ahIQM5tZUWUR_5V
                :width: 40 px


Create the diagram by connecting things together
-------------------------------------------------------------------------------

Now for the fun bit...

#. Mary is a Developer in the Product team. She has a Windows 10 PC and an Android phone.
#. Bob is an Accountant in the Accounts team. He has a Mac and an iPhone.
#. They connect to the office server, and via a firewall to the Internet.


.. uml:: NetworkUsersMachines4.puml
    :align: center
    :caption: *Connect the icons* 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./NetworkUsersMachines4.puml
    :linenos: 
    :emphasize-lines: 35-53

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton4| Press to play around with this diagram source online.

.. |playbutton4| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VLJTRkis3BxNK_0KE9WBd3fnpjdFUZ6ShWFM0iqMe2bsCo1G9JeMQak69DV8tLvZhxSd6MbPMTjW3H2H8lbzb3uH_XgYz77eMY4-QAoDHN11RYW0JOnzk5mil1pBlOdDy3W4zChPY3QModMBQoz3WxepLYyshRJnONrtuNgq0TNWJJn8hneJKSN1u-h243OiEXaYUl71MDKE-jXkSUswpjco9_yq-K2T5x9j_oTz8xqUfSTtIjOcg7VIz-YVtsrnR-8BUl5D2Mlf3s02IFW5dx6bUtim5cA3iF5E3of2HDcLS4-HHdBX7wIK6mDKIzXSWxIQ_d1bjNT6GzyuYoKp_-mU4_5QMhd_Z_PAAJVO66RUcqIxbYfJcSsHu_QPzu6ZjrlO3mSO6mUjSqyKgoFwYJ5Crow14Ti63w2SjSWdTrFUOXoTVm9w_4zJasSZGK9jF8uaHYwxjKH8jQKWPO0VAmWIRiS3izjxHBlJMQE2TVi4PspEoBxKYlT7CS_Ett9mL4RZR2ZuUbJCXa5qnUsCJoy9LpoMfnGqmyPY2BikILkGrWIYbR6l1ER0_034G_UYanc5wMOQmrDqVT4hggf-N9NLTp-KLLaj6PMVEUqsr_CnMjapf9DlCAlKIMMJgjDR5gPdmxeShEoCWjiDrwKiL1Ll9lyrJAQXEi7bOQkMRu5f58fatbngAdvu96a6cFLTBSlb5xZRtcVDiqg_fP6PLMB5TgFnsBBetWsHUeocDbURrpsOPeRE1wAPA-XFyT_hccY0DbnrGoPLv34iiaFPRwloy_VbwWkT-lCffshTe8jffLmUszTrWYSJBdw2Nbr2S8EdriffFCPdRJcfZ6oXGssa43H3dEqamMfZfPsInjOkfz9RNi9aGD61Wn0ymfnCmbzIArkR_P06NOY4uOAacfYxluY8P2d24eb4b7TqdEpsHq_GmdxMJOZiSNIIXqBEHUBvM9iMQOImE0UFLgD7JPrZ0_cJ3zGk66VXu-mKvt_QRODmOw9g6lE4_f-__Wxmws0qGdH7eFXAVFmvfT-_
                :width: 40 px

Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. Add some text to describe the connection from firewall to cloud





Change the Layout to Vertical
-------------------------------------------------------------------------------

We want the diagram to be vertical, with the cloud at the bottom and the users at the top.

.. tip ::
    We use ``-->`` to connect the icons so they are arranged vertically.
    
    See :ref:`Layout` for more info on arrows and layout.


.. uml:: NetworkUsersMachines5.puml
    :align: center
    :caption: *Vertical Layout* 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./NetworkUsersMachines5.puml
    :linenos: 
    :emphasize-lines: 37-57

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton5| Press to play around with this diagram source online.

.. |playbutton5| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VLNDRYCt3BxhARW15fq0ct7itVuqXsBJ56W29As1EEYbWA5870-H6McWdnY-zJNwUdsIKjACdSJO73oaI7uVgKz4yjK7wKBiEo4-Q6p885Wlbno0DeJ1NyncJcxh3OKsFaQFJbaJq8HQsNvsvQHlKVTaz6pPIHCUxcxFx836eugEmauwrL905QB3nHanrizwwGCwyO6CwgBUjvjTsRwtfXxOFqu-SEUPxBflfA-bqrlfy9sIE_BgdVGzkkTtMznJU44llglXJheTa0S9l-4pTdnl1sGWj0XBPtLK0GBAlePxZhGo5Vx5IjcjX_avBAz06iq_k3JQMT8mjDPWdPX_jO-5-4uQkJdGNYfbemb-vBtEj5oa9YfQxZbkdjFPf-ZD2ZPn1zlMGcVj4yUQW2up-dpj6X9YrU8Eb3K6q-Gsvms6hNLFm8__AJTv9WaI6dAuPJ6ciXl3X5nR2rO6qcDv8LYvTMHtlN68PgqdaQeat2SuIUQ4xKknqdclvidfMuuKbO6iyLMw7nSdaq1ynzM8Bqy9bsalZobuYScWz-k-Q5kns0pYRyA-KZW5nXTW7huOJqOAVQRKw9-27Qf1STNyvqKz_-6dUbxFpnFgyCxvWbVZ69qS4gINRp2BqabDfbINnwneI2RfiZEo9mKtorHNiZ2VfqFsNyDasQeZtBXjFDfRODc5gfWtbyh53uyiJOHHtyLvVVu5RbVt1ysBId-KdIagPSNMMtBO9T6TZO5xRAcXo-Nh7ebcX8u3yT9L_EFudqt3DC27L7NDfbHCUrXD3cU_dzUVVwmNNtZgpyUSghDHL_dBkMblNzS9aLOJpiv-WK5TWBVHSNDbDHuIexmfgqXsqACcAGIlKKxtae4D6MbobanZzxdoe1UG3IYUsdFBjCWvNVI_u7wceKqi-ov4GUMAefuOHtWPAYP7M2iX2jV-p5Fj_U7W2i7VV9fa56BoSZZBnJ5h0xDzRAX3NYciJi6XqUXGym2XXUb_071JprF3nz6fJlysgnRXce9gMtf2zzy__thuFP9627OF55-PB_zz5U9_
                :width: 40 px

Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. Arrange the diagram vertically with cloud on top, users on bottom
#. Arrange the diagram horizontally from left to right with users on left, cloud on right




Change the Layout by grouping icons together_
-------------------------------------------------------------------------------

Here we use the together_ keyword.


.. tip ::
    The together_ keyword allows you to specify what icons you want to group together.
    Like all layout options, minimize their use. See why in the Explore section.

.. uml:: NetworkUsersMachines6.puml
    :align: center
    :caption: *Group our icons* 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./NetworkUsersMachines6.puml
    :linenos: 
    :emphasize-lines: 18, 24, 34

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton6| Press to play around with this diagram source online.

.. |playbutton6| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/VLNlQkGs4F-kfvWB77NWuetthd-Q3-NI59h0fLt8XdufB8eqNelOaf7acAKK-XfzlJv9PoHxDybo-M2FD7z-C_ERyUxd4AMFGzSAyKvZRIo22t952cXYxCF5Ok7bM6vDR8Q78Q1NpaQqiLIkMrnv6HhKdR5wiMgbZVUtNyvSZpQW6ho9E-bLOoAgE7XSdXcA3OjEXeXUl3DMjOFUfrjSkQvpjkpfV6oyfymBsRPVCLzBhqVfyGsNMnFK6-Oxz4zlfhWpyHcy-AQ4M-btO098-0MViAM-FHWBiK5OUQS75I6Yx4gu8qqZsV4FOigD0QfpM5s1j9eUkBJQEwEXRvp5af5_TWyP-5PQkJt0NYhb1Xl3X7kTOCb9pL1cjSUuUU9xOEtD6hR33iR6GUlS8-dgY3uXXjHs2HonRd07D2ABNBbBTejnTFuHQFWVKf8d8q52RJoEHCRiTcC9a7nBGSm03ok8wBP8DWz_2U9mmxkpsNf4kz4pNGLJ-05EM9oGV4uRt_Uydfo-nc2jZCRPK72dvCo2WwZRzHIVXmgNlA774BJEnc88cowpN13j54HlZdt1DIkcMH3EtzmarMOK7hMfCJn6rnUzef3gnsLPVVT3MPNLEKCSnf-wlPfgQcNF8Pry5RFCQTKiidUUSM5w5apIpihEABXPiL-sGbNn9PrVXicyR4Tnqn9IQQy3yueKMRngAZdVFn1F0qnaBy_Byq_mPNrt642cZ3ZxBM-Jc9XY0ZUZyTZo5BmR8kKPJMqkLo_pCDGKEnL5-rZGG_hVwvfWW2xiTKqYUymhMim7idvRbH-_BvUVgFAFnvYgTOCkqfjiyqg_z1CYVVLdPpz1houWkC5JSkKq7WmJnMnLHhRGeJPI2DghPEua1TR6IfkinjPkRyj3lO0aG57LWLBoPYTpdi45VwIrsGxv0n0YHoMFp9wOIdYkoe8rp9KG6Mj_fwhsv_vm58BUwJRJACHyIkf45-cSYuJslZOjqbfXSGeUhKQFcWg83Sn_3q190rKDxwT3SVgdNJS8roQgfZ6FwF_xvzy0lmv68qIt3nIV2I_zz0hnFm00
                :width: 40 px

Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. What happens if we put a "together" around the network elements too - line 33?
 



Conclusion
-------------------------------------------------------------------------------

We went step-by-step through the creation of a network diagram. 

Looking at the source code for the diagram, there is very little redundant information. Most of the text appears in the diagram as text, the remainder is for the layout direction and the included icons.

Now that we have a template diagram, producing variants of it is even quicker as we just need to edit the relevant lines of text.