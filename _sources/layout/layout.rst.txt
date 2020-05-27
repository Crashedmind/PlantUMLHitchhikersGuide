******************************************************
Layout
******************************************************


.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _listsprites: https://plantuml.com/#
.. _together: https://forum.plantuml.net/4387/please-provide-together-keyword-group-diagram-nodes-together


.. tip ::
    *It's true that when diagram is big (or very big) manual placement could be useful. However and unfortunatly, this is against PlantUML concept*
    https://forum.plantuml.net/977

    Wrangling diagram elements to an exact position or layout is not what PlantUML is for. 

    However, there are **some layout tweak mechanims that should be used sparingly**. These are described here.


Arrows for Layout
===============================================================================

We can specify a connection direction as follows and this affects the diagram layout:

.. csv-table:: Arrow Syntax
    :header: "Text", "Direction"
    :widths: 10, 50

    ``->``, "horizontal left to right"
    ``-->``, "vertical top to bottom"
    ``-up->`` or ``-u->``, "vertical bottom to top"
    ``-down->``  or ``-d->``, "vertical top to bottom" 
    ``-left->`` or ``-l->``, "horizontal right to left"
    ``-right->`` or ``-r->``, "horizontal left to right"
    ``--norank]>``, "make a connection less important"
    ``--[hidden]>``, "hidden"
    ``--->`` or ``---->`` or ``----->`` ... , "varying arrow lengths; add dashes to make line longer"

.. tip ::
    The order in which diagram elements are defined can also impact how they are laid out.


.. tip ::
    Arrow head stypes per https://plantuml.com/sequence-diagram are for sequence diagrams only i.e. won't work in our component diagram examples.


up down left right
===============================================================================
.. uml:: arrows.puml
    :align: center

.. literalinclude:: ./arrows.puml
    :linenos: 



left to right direction
===============================================================================

.. uml:: left2right.puml
    :align: center

.. literalinclude:: ./left2right.puml
    :linenos: 


top to bottom direction
===============================================================================
.. uml:: top2bottom.puml
    :align: center

.. literalinclude:: ./top2bottom.puml
    :linenos: 


hidden
===============================================================================

.. note ::
    Note that the location of E is determined by a hidden arrow. Whereas F is floating i.e. not connected by an arrow so it can go anywhere.





nodesep and ranksep
===============================================================================

.. uml:: ./nodesepranksep.puml
    :align: center

.. literalinclude:: ./nodesepranksep.puml
    :linenos:
    :emphasize-lines: 3,4


.. uml:: ./nodesepranksep1.puml
    :align: center

.. literalinclude:: ./nodesepranksep1.puml
    :linenos:
    :emphasize-lines: 3



.. uml:: ./nodesepranksep2.puml
    :align: center

.. literalinclude:: ./nodesepranksep2.puml
    :linenos:
    :emphasize-lines: 7

together
===============================================================================

D,E are forced together.

E-C is specified as a very long arrow

.. uml:: ./together.puml
    :align: center

.. literalinclude:: ./together.puml
    :linenos:
    :emphasize-lines: 7-10, 18


linetype polyline ortho
===============================================================================

Either of the following can be added to a diagram:

* "skinparam linetype polyline"
* "skinparam linetype ortho"

See :ref:`Create Real Life AWS Diagrams` for practical examples of where these are used.


.. _AWSExample: http://www.plantuml.com/plantuml/uml/VL1BRnD13BxFhp1x8KXa8mfS8bGrH1Ng0GbfUPmdCsxMYkV1F99MLVyxJfPLAhJailRuUtpstkIYKwcErIloXgj5-AGFcMcpMFtgri6vuAydiOvSPBedj6qK_GH9rB4MN6Zc_r5Ss11VP6pHOz9yYV8bXHhlJF3v1KkzpZloKIVjWCbZUOm8-vZD9103FnuVQW8BgVH1gQZDJcyH6haTrXogRU19tQwlPftJ5X_UGZCqq67Qay569j2yKSzA_SYOykpqbU6fZkZtf2qL2bxpKOTfjhAt3wRNVej2MLaONwFYw-cVpOOYiszrmvHxJA1ZX93WW9kHEoJ3t8Q3dr_3e5d2knP-KgQI_vh1FD6sBy8uXo_XgeMkw5H0LtFSK9t1is2uUGdlM_XC5XB-hfWBBAJBCVYCQc30dF6-lDZXWxZtuI29uvB_MdviuSv5ySaIBew6oUoaaiz5Cqk7U_G5diPGii_g1hsjZly0

As at May 2020, it looks like there can be an issue using ortho. Specifically the label being too distant from the line.

* In our AWSExample_ the label "4. Show Ad" is too far from the line to be useful.
* issue seen by other users: https://forum.plantuml.net/1608/is-it-possible-to-only-use-straight-lines-in-a-class-diagram
