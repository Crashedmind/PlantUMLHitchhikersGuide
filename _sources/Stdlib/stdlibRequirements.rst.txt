*******************************************************************************
Standard Library - What We Have And What We Want
*******************************************************************************

.. todo ::
    put this stuff in tables to make it clearer

Observations on Standard Library
===============================================================================

#. Marcos use define and definelong which are deprecated per below

#. DRY (Don't Repeat Yourself). The macros are repeated 

    #. within a file -repeat the macro to add each new parameter
    #. across files - the macro content is largely the same - but the macro name changes to specify the icon to use

#. Close Coupling

    #. Macros are defined in the icon file for each icon

#. Lack of consistency    

    #. icon sizes

        #. some have multiple sizes
        #. for those that have one size, it is not standard/common with the other stdlib libraries

    #. icon files

        #. some break up the icons into categories sub-directories, some don't
        #. some have an ```all.puml``` file that includes all sprite content per category, some don'target

#. There's no way to scale the icons from the macros (the !define statements) except for Material. Plantuml does support scaling per https://forum.plantuml.net/4267/scaling-of-the-sprites-or-images. Support for scaling stereotypes is available since `March 2019 <https://forum.plantuml.net/4267/scaling-of-the-sprites-or-images?show=9086#c9086>`__.

#. At least 3 parameters are required and are rendered in the diagams  ```!define Batch(e\_alias, e\_label, e\_techn)```.
    
    #. In other words, the marcos force a user to specify things they may not care about e.g. to specify color in this macro, the user needs to specify the preceeding parameters also

        ```!define WHATEVER(_alias, _label, _shape, _color) ENTITY(_shape,_color,whatever,_label, _alias,WHATEVER)```    
    
    #. So if we wanted a colored or scaled icon only (with no label or technology), we have to implement it ourselves.

#. Some libaries have an ```all.puml``` that includes all icons and their macros for a given category/subset of icons. This allows including all icons by including one file - rather than an include per icon.

#. The superset of parameters provided by the macros are

    #. sprite
    #. color
    #. scale (material library only)
    #. shape (Type 1 (e_type), 4 (_shape))
    #. technology
    #. description
    #. label

Overall, the PlantUML Stdlib lacks consistency and therefore user friendliness.
We need to change this to empower the user with PlantUML.

.. todo ::
    get material scaling macro


What a User Wants In A Standard Library
===============================================================================
#. Consistency of macros, files, sizes
#. Specify the things they care about
    
    #. The current superset of parameters provided by the existing macros should be supported

        #. sprite
        #. color
        #. scale (material library only)
        #. shape (Type 1 (e_type), 4 (_shape))
        #. technology
        #. description
        #. label    

    #. Default values specified when the icons are built, but the ones the user cares about can be overridden by the user in their diagram file (at runtime)

#. Decoupling of the sprite (the image), from the decoration (text, shape, color, scale etc...)
    
    #. To benefit from other people's work e.g. if a new parameter or decoration/theme is added they like, they want to use it in their diagrams

#. Grouping of icons into categories.

    #. A user can include a file for that category that incldues all the icons (and not have to include a file for every icon)

#. Future Proofing

    #. uses supported PlantUML features, and can be easily changed in the future.

#. To be able to easily contribute their icon set to stdlib

