# Today I learned...
### The value and magic of CSS FlexBox

## Table of Contents
- [Introduction](#introduction)

## Introduction

Hello fellow coders!  I'm so excited to be making my first contribution to today-i-learned.  Ben was the best instructor any wanna be programmer could want and I'm honored to be able to be a part of this awesome repository!

Ok! So FlexBox!

Flexbox or "Flexible Box" is a relatively new set of CSS properties we can utilize to distribute space among elements and align content exactly how we want.  It's never been easier to set up grids and organize content, I assure you once you get the swing of Flexbox you will never bother with float or any grid system again.

A brief intro from the [MDN Page on Using CSS Flexible Boxes](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes)

> The CSS3 Flexible Box, or flexbox, is a layout mode intended to accommodate different screen sizes and different display devices. For many applications, the flexible box model is easier than the block model since it does not use floats, nor do the flex container's margins collapse with the margins of its contents.
>
> Many designers find the flexboxes easier to use than boxes. Without a lot of work, div's frequently rose to the top of a page when designers did not want them to---so for example, sticking a footer to the bottom of a page was difficult. The widths and heights of flexboxes vary to adapt to the display space, holding the lower down elements in place. Flexbox logic also asks whether you want div's to accrue to the right or on the bottom. The display order of flexbox elements is independent of their order in the source code.
>
> Popular layouts can thus be achieved more simply and with cleaner code. This independence intentionally affects only the visual rendering, leaving speech order and navigation based on a linear reading of the HTML source.

## The Basics

FlexBox is super simple to pick up, but takes some time to master.  If you already have a solid foundation with CSS all thats really new is:

### Two New Values:
![alt text](https://i.imgur.com/QPMSjo9.png "Example Legend")
### Display: flex;
  #### CSS
  ```css
  .parent {
    display: flex;
  }
  ```
  ![alt text](https://i.imgur.com/y3mfDG3.png "display: flex;")
### Display: inline-flex;
  #### CSS
  ```css
  .parent {
    display: inline-flex;
  }
  ```
  ![alt text](https://i.imgur.com/NtlTQyC.png "display: inline-flex;")

  These display properties created flex containers which create a "flex formatting context" for its content.  Similar to making a block formatting context but the flex layout is the replacement with its built-in ability to adjust automatically.

## Manipulating Contents of Flexbox Container

Once we have a parent container with a display of flex there is a myriad of options we have for aligning, ordering, and structuring our content within.  They fall into three broad categories with their own sub categories.  I will include far more detailed sources for each of the sub categories. For the time being this repo will just include the basics to get you started using flexbox, you will be TODO Add link to reources / reword sentence

1. Order & Orientation
    * flex-direction
    * flex-wrap
    * flex-flow
    * order
2. Alignment
    * justify-content
    * align-items
    * align-self
    * align-content
3. Flexibility
    * flex-grow
    * flex-shrink
    * flex-basis

## Order & Orientation

### Flex-Direction

Flex-direction as the name suggests defines the alignment of the children of a flex container with four options.

#### Row

Will align children elements if the parent container in a row.

```css
.parent {
  display: flex;
  flex-direction: row;
}
```
![alt text](https://i.imgur.com/RJD0vq0.png "flex-direction: row;")

#### Row-Reverse

Functions the same as row with the exception of ordering the child elements in reverse.

```css
.parent {
  display: flex;
  flex-direction: row-reverse;
}
```
![alt text](https://i.imgur.com/EQQzS4d.png "flex-direction: row-reverse;")

#### Column

Will align children elements if the parent container in a column.

```css
.parent {
  display: flex;
  flex-direction: column;
}
```
![alt text](https://i.imgur.com/8mUkA4R.png "flex-direction: column;")

#### Column-Reverse

Functions the same as column with the exception of ordering the child elements in reverse.

```css
.parent {
  display: flex;
  flex-direction: column-reverse;
}
```
![alt text](https://i.imgur.com/MwDhG1m.png "flex-direction: column-reverse;")

## Alignment

### Justify Content

This propertly allows for the alignment of children with the primary axis of the flex container.  So if we have a parent container with row we will be justifying content along the X-Axis while if it were a column we'd be justifyig it along the Y-Axis.

For the purpose of the following examples the flex-direction will be a row, but bear in mind the structuing applies the same for columns.

#### Flex-Start

Will justify the content among the beggining of the flex axis, so being a row we will "float the contents" to the start or left of the axis.

```css
.parent {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
}
```
![alt text](https://i.imgur.com/MwDhG1m.png "justify-content: flex-start;")

#### Flex-End

I'm sure your noticing some patterns by now.  Much like flex-start, flex-end will float the children elements to the end of the axis.  Since the flex-direction is row that that puts our little red buddies all the way to the right.

```css
.parent {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
}
```
![alt text](https://i.imgur.com/lJX7RpO.png "justify-content: flex-end;")

#### Center

Justify-Content: center; much like the rest of flexbox attribute values works exactly as it sounds.  It will center the contents of the container within the center of it's flex-direction's axis.

```css
.parent {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
```
![alt text](https://i.imgur.com/4039Flq.png "justify-content: center;")

#### Space Between

Space between will adjust the content evenly between each child elements. Bear in mind if the parent container has padding it won't be set to the edge like in the example below.

```css
.parent {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
```
![alt text](https://i.imgur.com/c6XdOql.png "justify-content: space-between;")

#### Space Around

Space around will adjust the content of the children elements automatically based on the space around them (not just between). Again the padding of the container and margin of the children will effect the final result of space-around.

```css
.parent {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}
```
![alt text](https://i.imgur.com/Gzc2uEn.png "justify-content: space-around;")
