# ABOUT
This is one of my first projects with HTML and CSS. I am learning a lot of material, but some things are still hazy. I want to go back and refactor my code. The instructor, Jonas implements BEM, the CSS naming convention and the 7-1 method for organizing his files.

I want to use BEMIT and ITCSS if all possible. There is a lot of overlap between BEMIT and BEM and ITCSS and the 7-1 method. But I just think I prefer the former over the latter.

I also want to develop a system for ordering my CSS properties, sectioning the different parts of my CSS, and proper spacing of my CSS/SCSS. I am stealing a lot, if not all of my organizational method from other people. I am relying a lot on Harry Roberts' style guide because he put a lot of time thinking about the matter.

# Table of Contents  
[Headers](##headers)  
[Emphasis](##emphasis)  

This will be how I will organize the Table of Content. There will be 1 for the HTML and 1 for the CSS. I will use the "|" symbol and repeat it 75times. I will list the sections with their respective # and in lowercase. Indent "Table of Content" 15x.

<!-- ||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
                                  #TABLE OF CONTENT

                                  I.#navigation
                                    A.
                                  II.#header
                                    A.
                                  III.#section-about
                                    A.
                                  IV.#section-features
                                  V.#section-tours
                                  VI.#popup
|||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||| -->

# File Organization
7-1 method mixed with the ITCSS.

7-1 file organization is:
base/
components/
layout/
pages/
themes/
abstracts/
vendors/

ITCSS's file organization is:
    Settings – used with preprocessors and contain font, colors definitions, etc.

    Tools – globally used mixins and functions. It’s important not to output any CSS in the first 2 layers.

    Generic – reset and/or normalize styles, box-sizing definition, etc. This is the first layer which generates actual CSS.

    Elements – styling for bare HTML elements (like H1, A, etc.). These come with default styling from the browser so we
    can redefine them here.

    Objects – class-based selectors which define undecorated design patterns, for example media object known from OOCSS

    Components – specific UI components. This is where majority of our work takes place and our UI components are often composed of Objects and Components

    Utilities – utilities and helper classes with ability to override anything which goes before in the triangle, eg. hide helper class


SIMILARITIES BETWEEN THE 2:
base/   ----- Elements/Generic
components/   ------ Components
layout/    ------ Objects
pages/
themes/
abstracts/  -----Settings
            -----Tools
vendors/   ------Generic


MY FILE SYSTEM
I. Abstracts (Combination of Settings + Tools)
II. Generic (Vendors, 3rd party)
III. Base (Resets, box-sizing, typography, animations, base Styling)
IV. Object (This is basically the "layout" that the 7-1 method describes describes. This is the non-cosmetic layer. I can also call it the "Structure" folder)
V.Components (Specific UI Implementation, use the Atomic design principle here to further organize your components into atom, molecules, organisms, template, and pages. Most likely, you will only use the first three categories in this section). The "template" section can be thought of as the Object category. Meanwhile, the "pages" section can be thought of as the "Object" + "Components"
VI. Utilities
VII.Alteration (States, Themes)
VIII. main.scss (Place to import all of you partial scss files)

Simplified File System
I. Abstracts
II. Base
III. Objects
IV. components
V. Utilities
VI. main.scss (Import file)

#Html Attribute Order

HTML attributes should come in this particular order for easier reading of code. Also double space between classes.

    class
    id, name
    data-*
    src, for, type, href, value
    title, alt
    role, aria-*

Classes make for great reusable components, so they come first. Ids are more specific and should be used sparingly (e.g., for in-page bookmarks), so they come second.

#White Space
    One (1) empty line between closely related rulesets.
    Two (2) empty lines between loosely related rulesets.
    Three (3) empty lines between entirely new sections.

#CSS Property Order
Declaration order

Related property declarations should be grouped together following the order:

    Positioning (Position, TRouBLe top/right/bottom/left, z-index)
    Box model (Display, float, width/ height, padding, margin)
    Typographic (Text-align, font, line-height, color)
    Visual (background, border, )
    Misc (Clip-Path, Opacity, Animations, etc)

Positioning comes first because it can remove an element from the normal flow of the document and override box model related styles. The box model comes next as it dictates a component's dimensions and placement.

Everything else takes place inside the component or without impacting the previous two sections, and thus they come last.

# Sectioning
I will use the md version to title & section off my material in my code. # = Title/Header 1, ## = Header 2, ### = Header 3, so on and so forth.

My title will be styled like this. I will use Harry Robert's system. A space between the asterisks and 20 forward slashes. The title will be centered in the middle. Below is an example of what I am thinking about doing. Notice that all of the letters are capitalized.

HTML sectioning

<--////////////////////
          #TITLE
////////////////////-->

  <--////////////////////
  // ## Header 2 -->



SCSS Sectioning
// //////////////////// //
//         #TITLE       //       
// //////////////////// //                    


    ///////////////////////
    // ## Header 2

      ///////////////////////
      // ### Header 3

        ///////////////////////
        // #### Header 4


CSS Sectioning
/* //////////////////// *\
          #CARDS
\* //////////////////// */

  /*//////////////////// 
  // ## HEADER 2 */
