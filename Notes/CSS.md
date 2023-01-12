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
| :---|---: |
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
    |:--|--:|
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
        }
        ```
    - Using contain
        ```css
        body{
            background-size: contain;
        }
        ```
- Preventing background image from repeating
    ```css 
    body{
        background-repeat: no-repeat;
    }
    ```
- Adjusting transparency of a background color
    ```css
    .paragraph{
        background: rgba(3, 109, 3, 0.5);
    }
    ```