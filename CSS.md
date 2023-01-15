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
            border-direction: 5px solid red;
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