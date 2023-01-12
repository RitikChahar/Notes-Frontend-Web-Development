# CSS - Cascading Style Sheets
## Ways of adding CSS to an Html page
### 1. Internal - by using a style element in the head section
```html
<style>
body{
    background-color: red;
}
</style>
```
### 2. Inline - by using the style attribute inside HTML elements
```html
<h1 style="color:blue;">Writing First CSS Line</h1>
```
### 3. External - by using a link element to link to an external CSS file
```html
<link rel="stylesheet" href="style.css">
```
## Difference between id and class
|id|class|
| :---|---: |
|It is a unique identifier.|It is a property.|
|Multiple elements cannot have same id.|Multiple elements can have same class.|
|One element can have only one id.|One element can have multiple classes.|
|# is used to target an id.|. is used to target a class.|
## Selectors in CSS - used to select Html elements
### 1. Element Selector - used to select an element based on the tag name
```css
h1{
    background-color: antiquewhite;
    color: aqua;
}
```
### 2. id Selector - used to select an element with a given id
```css
#blog{
    background-color: aqua;
    color: azure;
}
```
### 3. class Selector - used to select an element with a given class
```css
.album{
    background-color: rgb(219, 205, 9);
    color: rgb(255, 255, 255);
}
```
### 4. We can group selectors 
```css
h1, h2, h3{
    background-color: antiquewhite;
    color: aqua;
}
```
### 5. We can use element.class as a selector
```css
h2.blog{
    background-color: red;
    color: rgb(209, 233, 121);
}
```
### 6. * can be used as a universal selector to select all the elements
```css
*{
    margin: 4pt;
    padding: 10%;
}
```
### Preference Order in CSS
|Order|Type|
|:--|--:|
|1st|Inline CSS|
|2nd|id Selector|
|3rd|class Selector|
|4th|Universal Selector|
## Writing a comment in CSS
```css
/* This is a comment. */
```