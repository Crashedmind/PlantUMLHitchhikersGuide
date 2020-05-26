.. _stdlibreqs-label:

*******************************************************************************
Standard Library - What We Have And What We Want
*******************************************************************************

Observations on Standard Library
===============================================================================

.. tip ::

    The Observations, Requirements, and User Stories here allow us to create a new 
    PlantUML Stdlib to empower the user per todoref


.. csv-table:: Observations on Standard Library
   :header: "#", "Observation"
   :widths: 5, 50

    "**OBV_DEFINE_DEPRECATED**", "Macros use define and definelong which are deprecated per below"
    "**OBV_DRY**", "DRY (Don't Repeat Yourself). The macros are repeated 
        
        within a file -repeat the macro to add each new parameter

        across files - the macro content is largely the same - but the macro name changes to specify the icon to use
        "
    "**OBV_CLOSE_COUPLING**", "Macros are defined in the icon file for each icon
    
        the parameters, and order of parameters, is fixed" 
    "**OBV_CONSISTENCY**", "

        icon sizes

            some have multiple sizes

            for those that have one size, it is not standard/common with the other stdlib libraries

        icon files

            some break up the icons into categories sub-directories, some don't
            some have an ```all.puml``` file that includes all sprite content per category, some don'target       
        "
    "**OBV_NO_SCALE**", "There's no way to scale the icons from the macros (the !define statements) except for Material. 
    
        Plantuml does support scaling per https://forum.plantuml.net/4267/scaling-of-the-sprites-or-images. 
        
        Support for scaling stereotypes is available since `March 2019 <https://forum.plantuml.net/4267/scaling-of-the-sprites-or-images?show=9086#c9086>`__.
        "
    "**OBV_NO_TEXTATTRIB**", "There's no way to change the size, colour etc... of the text description, label, technology fields
        "        
    "**OBV_3PARAMS_MIN**", "At least 3 parameters are required and are rendered in the diagams  
    
        ```!define Batch(e\_alias, e\_label, e\_techn)```.
        
        In other words, the macros force a user to specify things they may not care about e.g. to specify color in this macro, the user needs to specify the preceeding parameters also

        *!define WHATEVER(_alias, _label, _shape, _color) ENTITY(_shape,_color,whatever,_label, _alias,WHATEVER)*
    
        So if we wanted a colored or scaled icon only (with no label or technology), we have to implement it ourselves."
    "**OBV_ALL_PUML**", "Some libaries have an ```all.puml``` that includes all icons and their macros for a given category/subset of icons. 
    
        This allows including all icons by including one file - rather than an include per icon.
        "


.. note ::
    
    The following software principles should apply 

        * Loose Coupling, High Cohesion (Consistency)
        * DRY (Don't Repeat Yourself) 
        * Open/Closed Principle (OCP) “open for extension” but “closed to modification” i.e. not have to change old macros to implement new behavior. New Macros are defined instead, that don't break existing user code (SOLID).
        
        


Macro Definitions
===============================================================================
Macros define the following 

    #. The superset of parameters 

        #. sprite
        #. color
        #. scale (material library only)
        #. shape (Type 1 (e_type), 4 (_shape))
        #. technology
        #. description
        #. label
    #. Fixed

        #. Text Size 
        #. Text Order



What a User Wants In A Standard Library
===============================================================================


.. csv-table:: What a User Wants In A Standard Library
   :header: "#", "Requirement"
   :widths: 5, 50

    "**REQ_CONSISTENCY**", "Consistency of macros, files, sizes"
    "**REQ_ONLY_CARE**", "Specify the things they care about

        Default values specified when the icons are built, but the ones the user cares about can be overridden by the user in their diagram file (at runtime)
    "
    "**REQ_DECOUPLE**", "Decoupling of the sprite (the image), from the decoration (text, shape, color, scale etc...)
    
        To benefit from other people's work e.g. if a new parameter or decoration/theme is added they like, they want to use it in their diagrams
        
        Future Proofing with backwards compatibility: new functionality can be added to the sprite library, but the user's existing code will still work with this new library
        "    
    "**REQ_CATEGORY**", "Grouping of icons into categories.

        A user can include a file for that category that incldues all the icons (and not have to include a file for every icon)
        "
    "**REQ_CONTRIBUTE**", "To be able to easily share / contribute 
    
        their icon set 

        their theme or style or layout
        " 


User Stories
===============================================================================


.. csv-table:: User Stories
   :header: "#", "As a User, I want X, so I am empowered to do Y"
   :widths: 5, 50

    "**US_HIGHLIGHT**", "To highlight certain parts of a diagram
    
        so I can show the relevant or important parts in the context of an overall diagram

        e.g. a diagram may have 10 icons/components, but I want to highlight the ones 
        being discussed or changed in my current system
        "
    "**US_THEME**", "To use, or create, a theme, 
    
        so I can create diagams consistent with my other (personal, organisation, company) documentation.
        "
    "**US_ICONSET**", "To use, or create and contribute, an icon set easily
    
        so I have all the icons I need for my diagrams
        "

