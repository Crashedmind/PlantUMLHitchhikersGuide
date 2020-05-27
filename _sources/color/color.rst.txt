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

Any Color hex code can be used e.g. "123456"

See https://www.google.com/search?q=color+picker

Alternatively, a color name can be used e.g. "blue"

Below is a procedure to show the colours/colors (depending on which part of the world you're in)
This uses the the colour parameter 

* as an alias (so we can draw different versions)
* as a <<stereo>> (so we can apply skinparams to that colour only)

.. uml:: ./1.2.puml
    :align: center
    :caption: Using a procedure to show colours

.. literalinclude:: ./1.2.puml
    :linenos:
    :emphasize-lines: 17, 27

.. note ::
    This was inspired by https://plantuml-documentation.readthedocs.io/en/latest/formatting/color-names.html which is a whole lot prettier than the version here.
    The main purpose here was to show how this can be done with a procedure.

    If you're feeling playful, go make a pretty version with a procedure and let me know so I can update this guide and give you credit.