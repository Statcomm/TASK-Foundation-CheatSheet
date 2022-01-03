# CSS

## CSS Basics

**Comments**
Comments in css are in the following format only

```css
/* This is a comment */
```

### Basics

In CSS, there are 3 types of **SELECTORS**

1. Tags
2. Classes
3. Ids

**Tags**

```css
_______________ {
  /* This will change the styling for every h1 tag in the linked html file */
}
```

**Classes**

```css
_______________ {
  /* This will change the styling for every tag 
    in the linked html file that implemented 
    the class container. 
    The HTML might look like the following
    
    <div class="container"> ... </div>
    */
}
```

**Ids**

```css
_______________ {
  /* This will change the styling for every tag 
    in the linked html file that implemented 
    the id box1. 
    The HTML might look like the following
    
    <div id="box1"> ... </div>
    */
}
```

to create a class in css you use the following command.
In CSS, we use the Kebab case (separate each word with a dash `-`)

```css
.class-name {
  /* properties: value; */
}
```

### colors

```css
/*To change the background color*/
___: ___;

/*To change the font color*/
___: ___;

/*To change the border color*/
___: ___;
```

### Box Model

```css
/*To add padding  */
___: ___;

/*To add margin */
___: ___;

/*To add border */
___: ___;
```

### Font

```css
/*To change the font size */
___: ___;

/*To change the font family  */
___: ___;

/*To change the font width */
___: ___;
```

### Sizes

**Units**
There are multiple units in CSS to size things
`____`: a CSS unit that represents number of pixels
`____`: a CSS unit that represents the percentage relatively to the container
`____`: a CSS unit which is relative to the font size of the parent element
`____`: a CSS unit which is relative to the font size of the html element
`____`: a CSS unit that represents the view height. We use it usually for background size and set it to 100 to get the size of the whole screen vertically.

```css
/*To change width */
___: ___;

/*To change height  */
___: ___;
```

### Position

```css
/*
To make everything inside a container relative to it. we use: position: ___
*/
position: ________;

/*To make any item in the container doesn't care about the container content, and it doesn't mind being on top of the over elements we use position: ____
This is perfect to put things stacking on top of each other
Making the position ____ allows you to use the following properties
- top:
- bottom: 
- left: 
- right: 
- z-index: 
*/
position: _________;

/*When position is (absolute), you can put things stacking on each other, but you can specify which element should be on visible on the top of another element, we use ___ and add a higher number to it */
______: 1000;
```

### Display

```css
/*To make an element take a whole block (a whole row) we use */
display: ___;

/*To make an element takes only the size that it needs, without taking a whole row  */
display: ___;

/*To enable a container to be horizontal we use  */
display: ___;

/*To hide an element  */
display: _____;
```

### Flex

```css
/*First thing you need to do to use any flex feature is to do */
display: flex;

/*To change the main axis to row or column you use  */
______: row;
______: column;

/*To make things center in the (MAIN AXIS) you use  */
______: center;

/*To make things center in the (CROSS AXIS) you use  */
______: center;
```

**common flex usages**
Making a container centers everything inside it, vertically and horizontally.

1. Give the container a size of 100vh, so it can center vertically on the whole screen
2. Use flex
3. (Optionally) change the direction, depending how you want to show the elements to column or row
4. use `align-items: center` and `justify-content:center`

example:

```css
.centered-container {
  display: flex;
  height: 100vh;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
```
