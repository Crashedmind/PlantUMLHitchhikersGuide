.. _scale-label:


******************************************************
Scaling Sprites
******************************************************


.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _listsprites: https://plantuml.com/#
.. _together: https://forum.plantuml.net/4387/please-provide-together-keyword-group-diagram-nodes-together



Scaling Sprite Options
===============================================================================


.. uml:: ./scale1.puml
    :align: center
    :caption: Different syntax for scaling sprites

.. literalinclude:: ./scale1.puml
    :linenos:
    :emphasize-lines: 17, 19


Revisiting :ref:`scalebigsmall-label`
===============================================================================

In :ref:`scalebigsmall-label` we created a large sprite 100x100 sprite, and a small 16x
16 sprite.

Here we create 1 48x48 sprite and scale it by x2 for large, and by 0.33 for small.

.. uml:: ./bigsmallscale.puml
    :align: center
    :caption: scaling one sprite bigger and smaller

.. literalinclude:: ./bigsmallscale.puml
    :linenos:

