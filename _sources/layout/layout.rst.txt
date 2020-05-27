******************************************************
Layout
******************************************************


.. _vision: https://www.scaledagileframework.com/vision/
.. _PlantUML: https://www.plantuml.com/
.. _PlantUMLPreProcessor: https://plantuml.com/preprocessing
.. _listsprites: https://plantuml.com/#
.. _together: https://forum.plantuml.net/4387/please-provide-together-keyword-group-diagram-nodes-together


.. tip ::
    *It's true that when diagram is big (or very big) manual placement could be useful. However and unfortunatly, this is againt PlantUML concept*
    https://forum.plantuml.net/977

    Wrangling diagram elements to an exact position or layout is not what PlantUML is for. 

    However, there are a minimal set of layout tweak options that should be used sparingly.


 
.. todo ::
    this chapter is WIP 


https://mrhaki.blogspot.com/2016/12/plantuml-pleasantness-customize.html


listsprites

allow_mixing
skinparam pathHoverColor green

arrows
===============================================================================

hidden
hide unlinked

dashed arrows and boxes

https://forum.plantuml.net/4949
skinparam arrowThickness 4

a-[thickness=20]>b: some text
b-[dashed,thickness=20]>d: some other text
nodesep and ranksep 

https://forum.plantuml.net/4181
class foo
foo --> bar
foo -[bold]-> bar1
foo -[dashed]-> bar2
foo -[dotted]-> bar3

top down left right

https://stackoverflow.com/questions/49945174/plantuml-component-diagram-layout-control


arrows first letter only
https://mrhaki.blogspot.com/2018/06/plantuml-pleasantness-setting-arrow.html

line length
https://mrhaki.blogspot.com/2016/12/plantuml-pleasantness-align-elements.html

hidden lines
https://dzone.com/articles/plantuml-pleasantness-layout-elements-with-hidden

nodesep and ranksep
===============================================================================

.. uml:: ./nodesepranksep.puml
    :align: center
    :caption: Nodesep and Ranksep

.. literalinclude:: ./nodesepranksep.puml
    :linenos:
    :emphasize-lines: 2,3

together
===============================================================================

linetype
===============================================================================
skinparam linetype polyline
skinparam linetype ortho

ortho line style. labels removed https://forum.plantuml.net/1608/is-it-possible-to-only-use-straight-lines-in-a-class-diagram

