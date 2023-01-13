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

## 9. Font Manipulation in CSS
