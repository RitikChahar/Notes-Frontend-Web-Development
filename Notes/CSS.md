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