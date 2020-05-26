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
#. Bob is an Accountant in the Accounts team. He has Mac and an iPhone.
#. They connect to the office server, and via a firewall to the Internet.

There 3 types of element with different properties:

#. Users: Role, Name, Team
#. Machines: Type, IP address, OS 
#. Network Equipment: Type, IP address, and e.g. product model and number

Select an icon library
-------------------------------------------------------------------------------
The OpenSecurityArchitecture library has a nice set of users and network components so we'll use that.

.. tip ::
    To see all stdlib icon libraries - do TBD
    

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
                :target: http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuNBAJrBGjLDmpCbCJbMmKiX8pSd9vt98pKi1IW80
                :width: 40 px


Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. Take a look at some other stdlib libraries
#. What happens if we don't include any libraries?
 

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
                :target: http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuNBAJrBGjLDmpCbCJbMmKiX8pSd9vt98pKi1IW80
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
                :target: http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuNBAJrBGjLDmpCbCJbMmKiX8pSd9vt98pKi1IW80
                :width: 40 px

Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. TBD







Create the diagram by connecting things together
-------------------------------------------------------------------------------

Now for the fun bit...

#. Mary is a Developer in the Product team. She has a Windows 10 PC and an Android phone.
#. Bob is an Accountant in the Accounts team. He has Mac and an iPhone.
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
                :target: http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuNBAJrBGjLDmpCbCJbMmKiX8pSd9vt98pKi1IW80
                :width: 40 px

Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
#. Add some text to describe the connection from firewall to cloud





Change the Layout to Vertical
-------------------------------------------------------------------------------

We want the diagram to be vertical, with the cloud at the bottom and the users at the top.

.. tip ::
    We use "-->" to connect the icons so they are arranged vertically

We can specify a connection direction as follows:

.. csv-table:: Tools Used
    :header: "text", "Direction"
    :widths: 10, 50

    "->", "horizontal left to right"
    "-->TODO", "vertical top to bottom"
    "-up->", "vertical bottom to top"
    "-down->", "vertical top to bottom" 
    "-left->", "horizontal right to left"
    "-right->", "horizontal left to right"



.. uml:: NetworkUsersMachines5.puml
    :align: center
    :caption: *Use --> to connect vertically* 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./NetworkUsersMachines5.puml
    :linenos: 
    :emphasize-lines: 37-57

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton5| Press to play around with this diagram source online.

.. |playbutton5| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuNBAJrBGjLDmpCbCJbMmKiX8pSd9vt98pKi1IW80
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
    :caption: *Use together keyword to group our icons* 

Source
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. literalinclude:: ./NetworkUsersMachines6.puml
    :linenos: 
    :emphasize-lines: 18, 24, 34

Play
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

|playbutton6| Press to play around with this diagram source online.

.. |playbutton6| image:: ../play.png
                :target: http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuNBAJrBGjLDmpCbCJbMmKiX8pSd9vt98pKi1IW80
                :width: 40 px

Explore
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

#. What happens if we put a "together" around the network elements too - line 33?
 



Conclusion
-------------------------------------------------------------------------------


.. todo::

    Write up Conclusion

.. todo::

    autogenerate online code links via script doing searchNreplace with plantuml PTE output