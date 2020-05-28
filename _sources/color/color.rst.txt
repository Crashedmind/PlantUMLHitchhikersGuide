******************************************************
Colors
******************************************************


.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _listsprites: https://plantuml.com/#
.. _together: https://forum.plantuml.net/4387/please-provide-together-keyword-group-diagram-nodes-together


Hex Codes and Pre-defined Colours
===============================================================================

Any Color hex code can be used e.g. "123456". See https://www.google.com/search?q=color+picker

Alternatively, a color name can be used e.g. "blue"

Below is a procedure to show the colours/colors (depending on which part of the world you're in)
This uses the colour parameter 

* as an alias (so we can draw different versions of the rectangle)
* as a <<stereo>> (so we can apply skinparams to that rectangle only)



.. note ::
    This was inspired by https://plantuml-documentation.readthedocs.io/en/latest/formatting/color-names.html which is a whole lot prettier than the version here.
    The main purpose here was to show how this can be done with a procedure.

    If you're feeling playful, go make a pretty version with a procedure and let me know so I can update this guide and give you credit.


    |playbuttoncolor| Press to play around with this diagram source online.

.. |playbuttoncolor| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/XPPBK-D64CVl-XGEjOViAS0-3YcAMcCUk6AmotQMujXesj94esap3pjAYkyUsva5qjEgSCA_Nyz3y_XBttm05s9hYgBuAThdI07LOEseH1KT3ZvSEjYEo93x-KD9XgBxM1I-qNOD3jg1mpA0hGmE_Yu6wUy9ogPo5Aqwj3ixImtFpmVflxTISWhT_vRv6XHjjQtU5mKNyRNYuj3HijPbOz7xztKdXwANedYRQvA3zsNW1qTd-r_krn_mx9V3x_EZtTAWLQ-BKXHhA1keS72BVuv8eTyz_Rk5EZe-NgsEZuy-_WVkKGRtQBLYyEJqq-SlNndy-kNpfzCJNdcWsK2dfuS-NzuckbVHyNaEPxF9U3HSZgVth8-XqILUc8YSsw2V8pxKEcJgEOA0Md3QPhL_HSVPnU-ByVtLOi4nwWevq_uvPj10sUJCbZMgeMd9gan65D1tJGO35uwsbhFeJFT0nFiTWS8WT3wgmGM7qUU2IZ8GCauEJCxioj0M7HyXIQzDmx7JhIVBQGSSNO9hUBS9zrJVa55evwGavw0JCQALkLJ-MmsD5lWTL6W326Pgz0RxHfcwijRIRESeqGMObgma4Fg6M1W8wUx8ZYqCSoYvPNJFaRH7mUK7DWboO2la0d4zqxOHyABff6dhDaquevXHKfLuCg-rmmkdouPpGmwC52VNvD07QOslOrbx3OpUWBR-YHnnNfCFqW3xeviX-JGBpvycbhD7D8QskU4Tt9B5xXAt6Gx2xeplPfEhkwlxfPJLOwiqs3agWLV4uOOSdufqnIQmGQlGoNY_nRxEtDPAopB1bkoergiLPKfNTOhAd0lnbqG7LkAlsvVsG2fnqCaSqVO8gK7Qf9nBWP4CGkyeuirBIaeC9b6M0T7qTTkpH2qAI9wspTZTT3d-BftGbDKPTKIMGrGwjliFXvtM5aMTFrGIKhedDOjkRUHMR6UOP6dExDffM_MtPhdDxB_9dT_SEwriVZEIic7a4DgC-z3DAH-8oXAyjWpVmmR-81wBoNGCJOsQG8aPrHkHxNu_SIwyYHBCdrxSnDdjus8y6auu1eDoQYUNTePpSL-I4tObkJLqi5kpDHS8PJsBgrN6NUGeZusPYIr7j5NYQrGynFbCv-IxzCNAU0TI8YoMy-7owkQHOr3AeDHHIZaEhHA75UvNmeiQZU5OexMGGRD1nw6OcdqNbWSfuvXnc-LZ_stlozhbrUZsVZgPPckx1Ci9Wk6erZuOv9HQ2CHXpu4MFmuVQeISwO0IMxJKS26zFHByiJh5I_4DhOgjAVu1
                :width: 40 px



.. uml:: ./1.2.puml
    :align: center
    :caption: Using a procedure to show colours

.. literalinclude:: ./1.2.puml
    :linenos:
    :emphasize-lines: 17, 27



Colors keyword
-------------------------------------------------------------------------------


.. literalinclude:: ./0.puml
    :linenos:
    