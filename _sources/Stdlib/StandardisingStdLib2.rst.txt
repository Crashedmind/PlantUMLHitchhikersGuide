.. _FunctionPointer: https://www.geeksforgeeks.org/function-pointer-in-c/

*******************************************************************************
Standardising Standard Library 2
*******************************************************************************


.. todo :: 

    this salt diagram does not work so use png for now
    
    .. uml:: stdlibFileLayout.puml
        :align: center
        :caption: *Plantuml Stdlib File Layout* 


Plantuml Stdlib File Layout
===============================================================================

.. figure :: stdlibFileLayout.png



.. csv-table:: Plantuml Stdlib Terminology
   :header: "Term", "Meaning"
   :widths: 10, 50

    "**PlantUML Stdlib**", "Plantuml Standard Library  

        i.e. https://github.com/plantuml/plantuml-stdlib"
    "**Library**", "Plantuml stdlib consists of several icon  **libraries**       

        e.g. awslib, elastic, azure…"
    "**Category**", "Each icon libary consists one or more icons **categories** 

        Category is a subdir / grouping of icons within an icon library

        some libraries don’t sub-divide the icons - so the category is the library"
    "**Icon**", "Each category consists one or more **icons**

        An Icon is a decorated sprite e.g. a coloured sprite in a rectangle with all the text and colour"
    "**Macro**", "The pre-processor code applied to a sprite
    
        i.e. the define/definelong or function/procedure associated with a sprite to make it an icon
        
        The call from the user puml file is a macro."     
    "**Sprite**", "A 2D bitmap"     


  

**Do we need individual sprite files? e.g. awslib/ARVR/Sumerian.puml and associated png (or svg), as all info is in puml file**



Plantuml Stdlib Themes, Styles, Layouts
===============================================================================

.. csv-table:: Plantuml Stdlib Themes Terminology
   :header: "Term", "Meaning"
   :widths: 10, 50


    
    "**Diagram**", "Everything you see. Everything represented by the puml file"
    "**Style**", "A collection of attributes that specify the appearance for a **single icon**. 
    
        A style can specify attributes such as font color, font size, background color, and much more. 
    
        Optional.        
    
    If present, a style takes precedence over a theme"
    "**Theme**", "A type of style that's **applied to the entire diagram** - not just an individual icon. 
    
        A collection of coordinated styles that determine the color, background attributes, and the fonts used on a layout. 
    
        Themes also enhance the appearance of a layout and give all your layouts a consistent look. 
    
        A theme does not control the placement or behavior of fields or objects on a layout. " 
    "**Layout**", "An arrangement of fields, objects, pictures, and layout parts that represents the way information is organized and presented."


    

