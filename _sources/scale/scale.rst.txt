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

The option on line 17 is the one given on https://plantuml.com/sprite.


Revisiting :ref:`scalebigsmall-label`
===============================================================================

In :ref:`scalebigsmall-label` we created a large sprite 100x100 sprite, and a small 16x
16 sprite.

Here we create 1 48x48 sprite and scale it by x2 for large, and by 0.33 for small.
We use the `*X` option, instead of `{scale*X}` option.

.. uml:: ./bigsmallscale.puml
    :align: center
    :caption: Scaling one sprite bigger and smaller

.. literalinclude:: ./bigsmallscale.puml
    :linenos:
    :emphasize-lines: 56,57

