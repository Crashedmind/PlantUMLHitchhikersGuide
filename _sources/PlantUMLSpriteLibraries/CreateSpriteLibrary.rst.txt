======================================================
Create A Sprite library
======================================================

Create Sprites by converting OSA icon libaries
----------------------------------------------------

`Open Security
Architecture <http://www.opensecurityarchitecture.org/>`__ (OSA) is a
useful resource for security architects providing a catalog of
controls, patterns, and requirements from numerous standards, governance
frameworks, legislation and regulations. See "`why have
OSA? <http://www.opensecurityarchitecture.org/cms/about/why-have-osa>`__\ ".

Resources include a `security architecture icon
library <http://www.opensecurityarchitecture.org/cms/library/icon-library>`__
available under a "`Creative Commons share-alike
license <http://www.opensecurityarchitecture.org/cms/about/license-terms>`__\ ".

These icons are available as png or svg images. 

Here we'll convert them to sprites so we can use them with PlantUML.


Converting the icon set to PlantUML Sprites
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1. Download the `security architecture
   icons <http://www.opensecurityarchitecture.org/cms/library/icon-library>`__
   and extract them into a directory e.g. "osaicons".

.. todo ::
    add info on a standard way to create sprites




Example
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. uml:: ./osa.puml
    :align: center

.. literalinclude:: ./osa.puml
    :linenos:

All Icons
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Below is what the icons look like - and the associated code.

.. todo ::
    add info on what osa icons look like


PlantUML HyperLinks
----------------------

PlantUML supports hyperlinks in output SVG images. This allows diagrams
to be linked together, and for a user to easily navigate by clicking
around per `Shneiderman's
mantra <http://www.ifp.illinois.edu/nabhcs/abstracts/shneiderman.html>`__:

    *Overview first, zoom and filter, then details-on-demand*

.. todo ::
    fix svg link


Clicking the image opens up the target ``svg`` image. This target image contains hyperlinks.

.. image:: ./links.svg
       :target: ../links.svg

.. literalinclude:: ./links.puml
    :linenos:
   