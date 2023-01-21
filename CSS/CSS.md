# CSS - Cascading Style Sheets
## 1. Ways of adding CSS to an Html page
- Internal - by using a style element in the head section
    ```html
    <style>
    body{
        background-color: red;
    }
    </style>
    ```
- Inline - by using the style attribute inside HTML elements
    ```html
    <h1 style="color:blue;">Writing First CSS Line</h1>
    ```
- External - by using a link element to link to an external CSS file
    ```html
    <link rel="stylesheet" href="style.css">
    ```
## 2. Difference between id and class
|id|class|
| :---|:--- |
|It is a unique identifier.|It is a property.|
|Multiple elements cannot have same id.|Multiple elements can have  class.|
|One element can have only one id.|One element can have multiple ses.|
|# is used to target an id.|. is used to target a class.|
## 3. Selectors in CSS - used to select Html elements
- Element Selector - used to select an element based on the tag name
    ```css
    h1{
        background-color: antiquewhite;
        color: aqua;
    }
    ```
- id Selector - used to select an element with a given id
    ```css
    #blog{
        background-color: aqua;
        color: azure;
    }
    ```
- class Selector - used to select an element with a given class
    ```css
    .album{
        background-color: rgb(219, 205, 9);
        color: rgb(255, 255, 255);
    }
    ```
- We can group selectors 
    ```css
    h1, h2, h3{
        background-color: antiquewhite;
        color: aqua;
    }
    ```
- We can use element.class as a selector
    ```css
    h2.blog{
        background-color: red;
        color: rgb(209, 233, 121);
    }
    ```
-  Asterisk(*) is used as a universal selector to select all the elements
    ```css
    *{
        margin: 4pt;
        padding: 10%;
    }
    ```
- Preference Order in CSS
    |Order|Type|
    |:--|:--|
    |1st|Inline CSS|
    |2nd|id Selector|
    |3rd|class Selector|
    |4th|Universal Selector|
## 4. Writing a comment in CSS
```css
/* This is a comment. */
```
## 5. Colors in CSS
### Types of colors in CSS
- Using Color Name
    ```css
    .heading{
        color: red;
    }
    ```
- Using Hex Code (#RRGGBB)
    ```css
    .heading{
        color: #7FFF00;
    }
    ```
- Using Decimal Code (R, G, B)
    ```css
    .heading{
        color: rgb(255,140,0);
    }
    ```
- Using Color Gradient
    - Linear Gradient
        ```css
        body{
            background: linear-gradient(to right bottom, green,rgb(255,140,0), rgba(255,140,0,0));
            /* We can add as many colors as we want, for direction we can also use angle in degree, eg. 90deg. */
        }
        ```
    - Radial Gradient
        ```css
        body{
            background: radial-gradient(circle, red 10%, green 20%, rgba(0,0,255,0.2) 40%);
            /* background-size will not work for radial gradient. Shape can either be cirle or ellipse.*/
        }
        ```
## 6. Background in CSS
- Adding color to the background
    ```css
    .paragraph{
        background: rgb(150, 175, 6);
    }
    ```
- Adding image to the background
    ```css
    .paragraph{
        background: url("Path");
    }
    ```
- Adjusting size of a background image
    - Using height and width
        ```css
        body{
            background-size: 400px 400px;
        }
        ```
    - Using cover
        ```css
        body{
            background-size: cover;
            /* The image keeps its aspect ratio and fills the given dimension */
        }
        ```
    - Using contain
        ```css
        body{
            background-size: contain;
            /*  The image keeps its aspect ratio, but is resized to fit within the given dimension */
        }
        ```
- Adjusting position of background image
    ```css
    body{
        /* Keyword Values */
        background-position: top;
        /* Percentage Values */
        background-position: 25% 75%;
        /* Length Values */
        background-position: 1cm 2cm;
        /* Multiple images */
        background-position: 0 0, center;
        /* Edge offsets values */
        background-position: bottom 10px right 20px;
    }
    ```
- Repeat property of background image
    ```css 
    body{
        /* Display image only once */
        background-repeat: no-repeat;
        /* Repeat image vertically */
        background-repeat: repeat-y;
        /* Repeat image horizontally */
        background-repeat: repeat-x;
    }
    ```
- Specify if the background image will scroll or be fixed
    ```css
    body{
        /* The background image will be fixed */
        background-attachment: fixed;
        /* The background image will scroll with the rest of the page */
        background-attachment: scroll;
    }
    ```
- Adjusting opacity / transparency of a background 
    ```css
    .paragraph{
        opacity: 0.5;
    }
    ```
- Adjusting transparency of a background color using RGBA
    ```css
    .paragraph{
        background: rgba(3, 109, 3, 0.5);
    }
    ```
## 7. Types of Units in CSS
- Absolute Units
    |Units|Description|
    |:--|:--|
    |cm|centimeters|
    |mm|millimeters|
    |in|inches (1in = 96px = 2.54cm)|
    |px|pixels (1px = 1/96th of 1in)|
    |pt|points (1pt = 1/72 of 1in)|
    |pc|picas (1pc = 12 pt)|
- Relative Units
    |Units|Description|
    |:--|:--|
    |em|Relative to the font-size of the element|	
    |ex|Relative to the x-height of the current font|	
    |ch|Relative to width of the "0"|	
    |rem|Relative to font-size of the root element|	
    |vw|Relative to 1% of the width of the viewport|	
    |vh|Relative to 1% of the height of the viewport|	
    |vmin|Relative to 1% of viewport's smaller dimension|	
    |vmax|Relative to 1% of viewport's larger dimension|	
    |%|Relative to the parent element|
## 8. Text Manipulation in CSS
- Text Color
    ```css
    .paragraph{
        color:aqua;
    }
    ```
- Text Background Color
    ```css
    .paragraph{
        background-color:aqua;
    }
    ```
- Text Alignment
    ```css
    .paragraph{
        /* text-align property is used to set the horizontal alignment of a text */
        text-align: left;
        text-align: right;
        text-align: center;
        text-align: justify;
        /* text-align-last property is used to specify how to align the last line of a text. */
        text-align-last: left;
        text-align-last: right;
        text-align-last: center;
        text-align-last: justify;
        /* direction and unicode-bidi properties are used to change the text direction of an element */
        unicode-bidi: bidi-override;
        direction: rtl;
        direction: ltr;
        /* vertical-align property is used to set the vertical alignment of an element */
        vertical-align: top;
        vertical-align: bottom;
        vertical-align: baseline;
        vertical-align: text-top;
        vertical-align: text-bottom;
        vertical-align: sub;
        vertical-align: super;
    }
    ```
- Text Decoration
    ```css
    .paragraph{
        /* text-decoration-line property is used to add a decoration line to text */
        text-decoration-line: none;
        text-decoration-line: overline;
        text-decoration-line: line-through;
        text-decoration-line: underline;
        text-decoration-line: overline underline;
        text-decoration-line: overline underline line-through;
        /* text-decoration-color property is used to set the color of the decoration line */
        text-decoration-color: green;
        /* text-decoration-style property is used to set the style of the decoration line */
        text-decoration-style: solid;
        text-decoration-style: double;
        text-decoration-style: dotted;
        text-decoration-style: dashed;
        text-decoration-style: wavy;
        /* text-decoration-thickness property is used to set the thickness of the decoration line */
        text-decoration-thickness: auto;
        text-decoration-thickness: 5px;
        text-decoration-thickness: 25%;
        /* text-decoration property can be used like this */
        text-decoration: underline red double 5px;
    }
    ```
- Text Transformation
    ```css
    .paragraph{
        /* text-transform property is used to specify uppercase and lowercase letters in a text */
        text-transform: uppercase;
        text-transform: lowercase;
        text-transform: capitalize;
    }
    ```
- Text Spacing
    ```css
    .paragraph{
        /* text-indent property is used to specify the indentation of the first line of a text */
        text-indent: 50px;
        text-indent: 50%;
        /* letter-spacing property is used to specify the space between the characters in a text */
        letter-spacing: 5px;
        letter-spacing: -5px;
        /* line-height property is used to specify the space between lines */
        line-height: 1.5;
        line-height: 10px;
        line-height: 10%;
        /* word-spacing property is used to specify the space between the words in a text */
        word-spacing: 20px;
        word-spacing: -20px;
        /* white-space property specifies how white-space inside an element is handled */
        white-space: normal;
        white-space: nowrap;
        white-space: pre;
        white-space: pre-wrap;
        white-space: pre-line;
    }
    ```
- Text Shadow
    ```css
    .paragraph{
        /* text-shadow property adds shadow to text */
        text-shadow: 2px 2px;
        /* add color to the shadow */
        text-shadow: 2px 2px red;
        /* add blur to the shadow */
        text-shadow: 2px 2px 5px red;
        /* add multiple shadows */
        text-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
    }
    ```
## 9. Font Manipulation in CSS
- Font Family
    ```css
    .paragraph{
        /* if the font name is more than one word, it must be in quotation marks */
        font-family: "Times New Roman", Times, serif;
        /* here Times and serif are backups in case "Times New Roman" is not found */
        /* some commonly used font fallbacks are -  serif, sans-serif, monospace, cursive, fantasy */
    }
    ```
- Font Style
    ```css
    .paragraph{
        /* font-style */
        font-style: normal;
        font-style: italic;
        font-style: oblique;
        /* font-weight property specifies the weight of a font */
        font-weight: normal;
        font-weight: bold;
        /* font-variant property specifies whether or not a text should be displayed in a small-caps font */
        font-variant: normal;
        font-variant: small-caps;
        /* font-size property sets the size of the text */
        font-size: 30px;
        font-size: 30%;
        font-size: 2.5em;
        /* font property is a shorthand property to use all these properties at once */
        font: italic small-caps bold 30px Georgia, serif;
    }
    ```
- Add custom font-family using Google Fonts
    1. Add a special stylesheet link to your HTML document
        ```html
        <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Tangerine">
        ```
    2.  Refer to the font in a CSS style
        ```css
        .paragraph{
            font-family: 'Tangerine', serif;
        }
        ```
- Add custom font-family from a ttf file
    ```css
    @font-face {
    font-family: 'Name of the Font Family';
    src: URL('fileName.ttf') format('truetype');
    }
    ``` 
- Add custom font-family from a otf file
    ```css
    @font-face {
    font-family: 'Name of the Font Family';
    src: URL('fileName.otf') format('opentype');
    }
    ```
## 10. CSS Box Model
![Alt text](https://upload.wikimedia.org/wikipedia/commons/e/ed/Box-model.svg) 
- Height and Width
    ```css
    div{
        /* in pixels */
        height: 10px;
        width: 10px;
        /* in centimetres */
        height: 10cm;
        width: 10cm;
        /* in percentage */
        height: 10%;
        width: 10%;
        /* The height and width properties do not include padding, borders, or margins. */
    }
    ```
- Margin
    ```css
    div{
        /* margin-direction property */
        margin-top: 100px;
        margin-bottom: 100px;
        margin-right: 150px;
        margin-left: 80px;
        /* margin property with four values */
        margin: top right bottom left;
        /* margin property with three values */
        margin: top right bottom;
        /* margin property with two values */
        margin: top-bottom right-left;
        /* margin property with one value */
        margin: all-four-margins;
        /* margin property auto is used to horizontally center the element */
        margin: auto;
        /* margin property inherit is used to inherit margin from parent element */
        margin: inherit;
    }
    /* Top and bottom margins of elements are sometimes collapsed into a single margin that is equal to the largest of the two margins. This is called Margin Collapse. */
    ```
- Padding
    ```css
    div{
        /* padding-direction property */
        padding-top: 50px;
        padding-right: 30px;
        padding-bottom: 50px;
        padding-left: 80px;
        /* padding property with four values */
        padding: top right bottom left;
        /* padding property with three values */
        padding: top right-left bottom;
        /* padding property with two values */
        padding: top-bottom right-left;
        /* padding property with one value */
        padding: all-four-paddings;
    }
    ```
- Border
    - Border Style
        ```css
        div{
            /* border-style property specifies what kind of border to display */
            border-style: dotted;
            border-style: dashed;
            border-style: solid;
            border-style: double;
            border-style: groove;
            border-style: ridge;
            border-style: inset;
            border-style: outset;
            border-style: none;
            border-style: hidden;
            /* border-style property with four values */
            border-style: top right bottom left;
            /* border-style property with three values */
            border-style: top right-left bottom;
            /* border-style property with two values */
            border-style: top-bottom right-left;
            /* border-style property with one value */
            border-style: all-four-borders;
        }
        ```
    - Border Width
        ```css
        div{
            /* border-width property specifies the width of the four borders */
            /* border-width property with four values */
            border-width: top right bottom left;
            /* border-width property with three values */
            border-width: top right-left bottom;
            /* border-width property with two values */
            border-width: top-bottom right-left;
            /* border-width property with one value */
            border-width: all-four-borders;
        }
        ```
    - Border Color
        ```css
        div{
            /* border-color property specifies the color of the four borders */
            /* border-color property with four values */
            border-color: top right bottom left;
            /* border-color property with three values */
            border-color: top right-left bottom;
            /* border-color property with two values */
            border-color: top-bottom right-left;
            /* border-color property with one value */
            border-color: all-four-borders;
        }
    - Border Shorthand
        ```css
        div{
            border: 5px solid red;
        }
        ```
    - Rounded Borders
        ```css
        div{
            border-radius: 10px;
        }
        ```
- Box Sizing
    ```css
    /* box-sizing property allows us to include the padding and border in an element's total width and height */
    div{
        /* the width and height properties includes content, padding and border */
        box-sizing: border-box;
        /* the width and height properties includes only the content */
        box-sizing: content-box;
    }
    ```
- Box Shadow
    ```css
    .paragraph{
        /* box-shadow property adds shadow to box */
        box-shadow: 2px 2px;
        /* add color to the shadow */
        box-shadow: 2px 2px red;
        /* add blur to the shadow */
        box-shadow: 2px 2px 5px red;
        /* add multiple shadows */
        box-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
        /* add shadow spread-radius */
        box-shadow: 2px 2px 5px 10px red;
        /* add shadow inside the box */
        box-shadow: inset 2px 2px 5px red;

    }
    ```
## 11. Float and Clear
- Float
    ```css
    .box{
        /* float property specifies how an element should float */
        float: none;
        float: left;
        float: right;
        float: inline-start;
        float: inline-end;
        float: inherit;
    }
    ```
- Clear
    ```css
    .box{
        /* clear property specifies what should happen with the element that is next to a floating element */
        clear: none;
        clear: left;
        clear: right;
        clear: both;
    }
    ```
## 12. CSS Flexbox
![Alt text](https://web-dev.imgix.net/image/VbAJIREinuYvovrBzzvEyZOpw5w1/uSH4TxRv8KNQDTK7Vn8h.svg) 
- Flex Container
    ```css
    .box{
        /* to create a flex box */
        display: flex;
        /* flex-direction property defines in which direction the container wants to stack the flex items */
        flex-direction: row;
        flex-direction: row-reverse;
        flex-direction: column;
        flex-direction: column-reverse;
        /* flex-wrap property specifies whether the flex items should wrap or not */
        flex-wrap: nowrap;
        flex-wrap: wrap;
        flex-wrap: wrap-reverse;
        /* flex-flow property is a shorthand property for setting both the flex-direction and flex-wrap properties */
        flex-flow: row wrap;
        /* justify-content property is used to align the flex items */
        justify-content: center;     
        justify-content: start;
        justify-content: end;        
        justify-content: flex-start;  
        justify-content: flex-end;    
        justify-content: left;       
        justify-content: right; 
        justify-content: space-between;
        justify-content: space-around;
        justify-content: space-evenly;
        justify-content: stretch;
        /* align-items property is used to align the flex items */
        align-items: center;
        align-items: start;
        align-items: end;
        align-items: flex-start; 
        align-items: flex-end;
        align-items: stretch;
        align-items: baseline;
        /* align-content property is used to align the flex lines */
        align-content: center;
        align-content: start;
        align-content: end;   
        align-content: flex-start; 
        align-content: flex-end;  
        align-content: stretch;
        align-content: space-evenly;
        align-content: space-between;
        align-content: space-around;
        align-content: baseline;
    }
    ```
- Flex Item
    ```css
    .box{
        /* order property specifies the order of the flex items */
        order: 2;
        order: -2;
        /* flex-grow property specifies how much a flex item will grow relative to the rest of the flex items */
        flex-grow: 2;
        flex-grow: 2.5;
        /* flex-shrink property specifies how much a flex item will shrink relative to the rest of the flex items */
        flex-shrink: 2;
        flex-shrink: 2.5;
        /* flex-basis property specifies the initial length of a flex item */
        flex-basis: 10em;
        flex-basis: 3px;
        flex-basis: 50%;
        /* flex property is a shorthand property for the flex-grow, flex-shrink, and flex-basis properties */
        flex: flex-grow flex-shrink flex-basis;
        /* align-self property specifies the alignment for the selected item inside the flexible container */
        align-self: center; 
        align-self: start; 
        align-self: end;
        align-self: flex-start; 
        align-self: flex-end; 
        align-self: self-start; 
        align-self: self-end; 
        align-self: baseline;
        align-self: stretch;
    }
    ```
## 13. CSS Grid
![Alt text](https://webkit.org/wp-content/uploads/grid-concepts.svg) 
- Grid Container
    ```css
    div{
        /* to create a grid */
        display: grid;
        display: inline-grid;
        /* row-gap property sets the gap between the rows */
        row-gap: 50px;
        /* column-gap property sets the gap between the columns */
        column-gap: 50px;
        /* gap property is a shorthand property for the row-gap and the column-gap properties */
        gap: row column;
        /* gap property with one value */
        gap: row-column;
        /* grid-template-areas property specifies named grid areas */
        grid-template-areas: 'box1 box1 . box2'
                             'box3 . box4 .'; 
        /* grid-template-columns specifies the size of the columns and number of columns in a grid layout */
        grid-template-columns: auto auto auto;
        grid-template-columns: 200px 300px 50px 500px;
        /* grid-template-rows specifies the size of the rows in a grid layout */
        grid-template-rows: auto auto auto;
        grid-template-rows: 200px 300px 50px 500px;
        /* justify-content property is used to align the whole grid inside the container */
        justify-content: center;     
        justify-content: start;
        justify-content: end;        
        justify-content: flex-start;  
        justify-content: flex-end;    
        justify-content: left;       
        justify-content: right; 
        justify-content: space-between;
        justify-content: space-around;
        justify-content: space-evenly;
        justify-content: stretch;
        /* align-content property is used to vertically align the whole grid inside the container */
        align-content: center;
        align-content: start;
        align-content: end;   
        align-content: flex-start; 
        align-content: flex-end;  
        align-content: stretch;
        align-content: space-evenly;
        align-content: space-between;
        align-content: space-around;
        align-content: baseline;
    }
    ```
- Grid Item
    ```css
    div{
        /* grid-column-start and grid-row-start defines the starting column and row of a grid item */
        grid-column-start: 2;
        grid-row-start: 2;
        /* grid-column-end and grid-row-end defines the ending column and row of a grid item */
        grid-column-end: 2;
        grid-row-end: 2;
        /* grid-area property is used as a shorthand property for the grid-row-start, grid-column-start, grid-row-end and the grid-column-end */
        grid-area: row-start / column-start / row-end / column-end;
        grid-area: row-start / column-start / span row / span column;
        /* grid-area property is also be used to assign names to grid items, named grid items can be referred to by the grid-template-areas property of the grid container. */
        grid-area: box;
        /* grid-column property defines number of columns an item will span */
        grid-column: 1 / 3;
        grid-column: 1 / span 3;
        /* grid-row property defines number of rows an item will span */
        grid-row: 1 / 3;
        grid-row: 1 / span 3;
    }
    ```
## 14. CSS Positions
```css
.paragraph{
    /* position property specifies the type of positioning method used for an element  */
    position: static;
    /* static positioned elements are not affected by the top, bottom, left, and right properties */
    position: relative;
    /* setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position */
    position: fixed;
    /* element with fixed position is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. */
    position: absolute;
    /* element with absolute position is positioned relative to the nearest positioned ancestor */
    position: sticky;
    /* element with sticky position is positioned based on the user's scroll position */
    /* top, bottom, left and right properties */
    top: 10px;
    bottom: 10px;
    left: 10px;
    right: 10px;
    /* z-index property specifies the stack order of an element, element with higher z-index will be on top  */
    z-index: 2;
}
``` 
## 15. CSS Media Queries
- max-width
    ```css
    /* if the browser window is 600px or smaller, the background color will be orange */
    @media only screen and (max-width: 600px) {
        body {
        background-color: orange;
        }
    }
    ```
- min-width
    ```css
    /* if the browser window is 600px or above, the background color will be red */
    @media only screen and (min-width: 600px) {
        body {
        background-color: red;
        }
    }
    ```
- landscape
    ```css
    /* web page will have a blue background if the orientation is in landscape mode */
    @media only screen and (orientation: landscape) {
    body {
        background-color: blue;
    }
    }
    ```
## 16. CSS Transforms
- transform Property
    - Translate
        ```css
        .box{
            /* translateX() */
            transform: translateX(10deg);
            /* translateY() */
            transform: translateY(10deg);
            /* translateZ() */
            transform: translateZ(10deg);
            /* translate() */
            transform: translate(10px , 10px);
            /* translate3d() */
            transform: translate3d(10, 20, 30);
        }
        ```
    - Rotate
        ```css
        .box{
            /* rotateX() */
            transform: rotateX(10deg);
            /* rotateY() */
            transform: rotateY(10deg);
            /* rotateZ() */
            transform: rotateZ(10deg);
            /* rotate() */
            transform: rotate(20deg);
            transform: rotate(-20deg);
            /* rotate3d() */
            transform: rotate3d(10, 20, 30);
        }
        ```
    - Scale
        ```css
        .box{
            /* scaleX() */
            transform: scaleX(10);
            /* scaleY() */
            transform: scaleY(10);
            /* scaleZ() */
            transform: scaleZ(10);
            /* scale() */
            transform: scale(10,10);
            /* scale3d() */
            transform: scale3d(10,10,10);
        }
        ```
    - Skew
        ```css
        .box{
            /* skewX() */
            transform: skewX(20deg);
            /* skewY() */
            transform: skewY(20deg);
            /* skew() */
            transform: skew(20deg, 10deg);
        }
        ```
    - Matrix
        ```css
        .box{
            /* matrix() */
            transform: matrix(scaleX(), skewY(), skewX(), scaleY(), translateX(), translateY());
            /* to use multiple functions together*/
            transform: translate(80px, 80px) scale(1.5, 1.5) rotate(45deg);
        }
        ```
- transform-origin Property
    ```css
    .box{
        /* transform-origin property allows you to change the position of transformed elements */
        transform-origin: 20% 40%;
        transform-origin: 20% 40% 20;
        /* values can be left, center, right, length, % for X - axis */
        /* values can be top, center, bottom, length, % for Y - axis */
        /* values can be length for Z - axis */
    }
    ```
- transform-style Property
    ```css
    .box{
        /* transform-style property specifies how nested elements are rendered in 3D space */
        transform-style: flat;
        transform-style: preserve-3d;
    }
    ```
- perspective Property
    ```css
    .box{
        /* perspective property defines how far the object is away from the user */
        perspective: none;
        perspective: 800px;
        perspective: 23rem;
        perspective: 5.5cm;
    }
    ```
- perspective-origin Property
    ```css
    .box{
        /* perspective-origin property defines at from which position the user is looking at the 3D-positioned element */
        perspective-origin: value-x value-y;
        /* value can be left, center, right, length, % for X axis, default value is 50% */
        /* value can be top, center, bottom, length, % for Y axis, default value is 50% */
    }
    ```
- backface-visibility Property
    ```css
    .box{
        /* backface-visibility property defines whether or not the back face of an element should be visible when facing the user */
        backface-visibility: visible;
        backface-visibility: hidden;
    }
    ```
## 17. CSS Transitions
- Using Hover
    ```css
    /* Transitions enables us to define the transition between two states of an element */
    .box:hover {
        background: yellow;
        width: 300px;
        height: 300px;
        transform: rotate(180deg);
    }
    ```
- transition-property Property
    ```css
    .box{
        /* it is the property on which transition will be applied */
        transition-property: opacity;
        transition-property: opacity, height;
    }
    ```
- transition-duration Property
    ```css
    .box{
        /* transition-duration property specifies how much time a transition effect takes to complete */
        transition-duration: 5s;
        transition-duration: 500ms;
    }
    ```
- transition-delay Property
    ```css
    .box{
        /* transition-delay property specifies a delay for the transition effect */
        transition-delay: 2s;
        transition-delay: 250ms;
    }
    ```
- transition-timing-function Property
    ```css
    .box{
        /* transition-timing-function property specifies the speed curve of the transition effect */
        transition-timing-function: linear;
        transition-timing-function: ease;
        transition-timing-function: ease-in;
        transition-timing-function: ease-out;
        transition-timing-function: ease-in-out;
        transition-timing-function: cubic-bezier(0.1, 0.7, 1, 0.1);
    }
    ```
- transition Property
    ```css
    .box{
        /* transition property is a shorthand property for transition-property, transition-duration, transition-timing-function, and transition-delay */
        /* property name, duration */
        transition: margin-right 4s;
        /* property name, duration, delay */
        transition: margin-right 4s 1s;
        /* property name, duration, easing function */
        transition: margin-right 4s ease-in-out;
        /* property name, duration, easing function | delay */
        transition: margin-right 4s ease-in-out 1s;
        /* apply to multiple properties */
        transition: margin-right 4s, color 1s;
    }
    ```
## 18. CSS Animations
```css
/* @keyframes */
@keyframes nameOfAnimation {
    from {
        background-color: red;
        }
    to {
        background-color: yellow;
        }
}
/* percentage value states with animation */
@keyframes nameOfAnimation {
  0%   {
    top: 0px;
    background: red;
    }
  25%  {
      top: 200px;
      background: white;
    }
  50%  {
      top: 100px;
      background: green;
    }
  75%  {
      top: 200px;
      background: orange;
    }
  100% {
      top: 0px;
      background: blue;
    }
}
.box{
    /* animation-name  */
    animation-name: nameOfAnimation;
    /* animation-duration  */
    animation-duration: 750ms;
    animation-duration: 3s;
    /* animation-delay  */
    animation-delay: 750ms;
    animation-delay: 3s;
    animation-delay: -3s;
    /* animation-iteration-count  */
    animation-iteration-count: infinite;
    animation-iteration-count: 5;
    /* animation-direction  */
    animation-direction: normal;
    animation-direction: reverse;
    animation-direction: alternate;
    animation-direction: alternate-reverse;
    /* animation-timing-function  */
    animation-timing-function: ease;
    animation-timing-function: ease-in;
    animation-timing-function: ease-out;
    animation-timing-function: ease-in-out;
    animation-timing-function: linear;
    animation-timing-function: step-start;
    animation-timing-function: step-end;
    animation-timing-function: cubic-bezier(0.1, 0.7, 1, 0.1);
    /* animation-fill-mode  */
    animation-fill-mode: none;
    animation-fill-mode: forwards;
    animation-fill-mode: backwards;
    animation-fill-mode: both;
    /* animation-play-state */
    animation-play-state: paused;
    animation-play-state: running;
    /* animation  */
    animation: nameOfAnimation duration timing-function delay iteration-count direction;
}
```