# Introduction
This is the *Natours* project from the **Advanced CSS Udemy Course**. I am mainly focused on organizing my code and refactoring my code so that it's maintainable in the future. Although the instructor, Jonas does a great job of introducing the concepts and does introduce organizational concepts such as BEM and the 7-1 file management system, I want to organize the code a little bit more.

Here I will detail the various organizational aspects that I hope to apply in my future projects. Most of it not all are ideas that I read about online and borrowed heavily from BEM, BEMIT, Atomic Design, OOCSS, and more. I take no credit for coming up with these ideas. However, I have renamed and combined a few concepts in a way that makes sense for me.

# Goals
+ Learn about CSS (float layout)
+ Become confident with using media queries
+ Use and become comfortable with Git/Github
+ Get accustomed to the basic Agile Method
+ Create a general organizational template/guide for future projects

# CSS Style Guide

## File Management System
I have created a 7 folder structure for my SCSS code. It's in alphabetical order. I have decided to singularize all of these folder names.

The folder system is largely based on the ITCSS folder system mixed with the 7-1 folder system in the SCSS guidelines.

+ ABSTRACT
  - Name taken from the [7-1 Pattern](https://sass-guidelin.es/)
  - A combination of the _Settings_ & _Tools_ section outlined in [ITCSS](https://www.creativebloq.com/web-design/manage-large-css-projects-itcss-101517528)  
+ BASE
  `Reset, 3rd party default styling, bare html elements`
+ BOX
  `The so called "Object" proposed by Nicole Sullivan in _OOCSS_ & also featured in _ITCSS_`
  `The structural, skeletal, non-cosmetic template and container where HTML items can live`
+ COLLECTION
  `Large components or a grouping of smaller components (atoms, molecules, cells)`
  `Components at the Organism or Pages level`
+ COMPONENT
  `Smaller components (atoms, molecules, cells)`
+ UTILITY
  `Utility or helper classes helping in (alignment, spacing, color, etc). Overriding class. Usually does 1 thing and does it well)`
+ VARIATION
  `States, Themes, and Animations`

## Sectioning
Use symbols `//`, `==`, `..` to create headings in your files. Use 15 symbols when creating regular headings *(Headings 1-6)* and use 30 `//` when creating the Table of Content. The Table of Content should exist in the HTML file after the `<head>`. It will also exist in the _main.scss_ file.

The `#` of the headings are based off of the Markdown syntax.

### HTML SECTIONING
    <!--///////////////
            #TITLE
    ///////////////-->

    <!--//////////////////////////////
              #TABLE-OF-CONTENT

              1. #Header
              2. #Header
     //////////////////////////////-->

    <!--===============
          #HEADER-1
    ================-->

    <!--...............
          ##HEADER-2
    ................-->

    <!-- ###HEADER-3
    ================-->

    <!-- ####HEADER-4
    ................-->

    <!--=== #####HEADER-5 ===-->

    <!--... ######HEADER-6 ...-->

### CSS SECTIONING

    /&ast;///////////////
          #TITLE
    ///////////////&ast;/

    /&ast;///////////////////////////////////
                  #TABLE-OF-CONTENT

                  1. #Header-1
                  2. #Header-2
     ///////////////////////////////////&ast;/

    /&ast;===============
      #HEADER-1
    ===============&ast;/

    /&ast;...............
      ##HEADER-2
    ...............&ast;/

    /&ast;  ###HEADER-3
    ================&ast;/

    /&ast;  ####HEADER-4
    ................&ast;/


    /&ast;=== #####HEADER-5 ===&ast;/


    /&ast;... ######HEADER-6 ...&ast;/


### SCSS SECTIONING

    /////////////////
    //    #TITLE
    /////////////////


    ////////////////////////////////
    //      #TABLE-OF-CONTENT
    //
    //        1. #Header-1
    //        2. #Header-2
    ////////////////////////////////

    //===============
    //    #HEADER-1
    //===============

    //...............
    //    ##HEADER-2
    //...............

    // ###HEADER-3
    //================

    // ####HEADER-4
    //................

    //=== #####HEADER-5 ===//

    //... ######HEADER-6 ...//


## CSS Property Order

1. Layout
   `position(clear, display, float, TRouBLe, z-index)`
2. Box-Positioning
  `(border, margin, padding, height, width)`
3. Visual
  `(background, box-shadow, color)`
4. Font & Text
  `(font-size, font-family, line-height, text-align, text-transform, etc`
5. Miscellaneous
  `(cursor, overflow, etc)`

## Html Attribute Order

HTML attributes should come in this particular order for easier reading of code. Also double space between classes.

    class
    id, name
    data-*
    src, for, type, href, value
    title, alt
    role, aria-*

Classes make for great reusable components, so they come first. Ids are more specific and should be used sparingly (e.g., for in-page bookmarks), so they come second.
