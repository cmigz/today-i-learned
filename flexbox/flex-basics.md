# Today I learned...
### How Awesome CSS Flexbox is
##### By: Christian Mignacca
##### [@cmigz](https://github.com/cmigz)

## Table of Contents
- [Introduction](#introduction)
- [The Basics](#the-basics)
- [Manipulating Flex Contents](#manipulating-contents-of-flexbox-container)
  - [Order and Orientation](#order--orientation)
    - [Flex-Direction](#flex-direction)
      - [Row](#row)
      - [Row-Reverse](#row-reverse)
      - [Column](#column)
      - [Column-Reverse](#column-reverse)
  - [Alignment](#alignment)
    - [Justify-Content](#justify-content)
      - [Flex-Start](#flex-start)
      - [Flex-End](#flex-end)
      - [Center](#center)
      - [Space-Between](#space-between)
      - [Space-Around](#space-around)
- [Sources and External Resources](#sources-and-external-resources)

## Introduction

Hello fellow coders!  I'm so excited to be making my first contribution to today-i-learned.  Ben was the best instructor any wanna be programmer could ask for and I'm honored to be able to be a part of this awesome repository!

Ok! So FlexBox!

Flexbox or "Flexible Box" is a relatively new set of CSS properties we can utilize to distribute space among elements and align content exactly how we want.  It's never been easier to set up grids and organize content. I assure you once you get the swing of Flexbox you will never bother with `float` or any other grid system again.

A brief intro from the [MDN Page on Using CSS Flexible Boxes](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes)

> The CSS3 Flexible Box, or flexbox, is a layout mode intended to accommodate different screen sizes and different display devices. For many applications, the flexible box model is easier than the block model since it does not use floats, nor do the flex container's margins collapse with the margins of its contents.
>
> Many designers find the flexboxes easier to use than boxes. Without a lot of work, div's frequently rose to the top of a page when designers did not want them to---so for example, sticking a footer to the bottom of a page was difficult. The widths and heights of flexboxes vary to adapt to the display space, holding the lower down elements in place. Flexbox logic also asks whether you want div's to accrue to the right or on the bottom. The display order of flexbox elements is independent of their order in the source code.
>
> Popular layouts can thus be achieved more simply and with cleaner code. This independence intentionally affects only the visual rendering, leaving speech order and navigation based on a linear reading of the HTML source.

## The Basics

FlexBox is super simple to pick up but takes some time to master.  If you already have a solid foundation with CSS all that's really new is:

### Two New Values:
![alt text](https://i.imgur.com/QPMSjo9.png "Example Legend")
### Display: flex;
  #### CSS
  ```css
  .parent {
    display: flex;
  }
  ```
  ![](https://i.imgur.com/ByxCOyr.gif)
### Display: inline-flex;
  #### CSS
  ```css
  .parent {
    display: inline-flex;
  }
  ```
  ![](https://i.imgur.com/4VXBCwr.gif)

  These display properties create flex containers which make a "flex formatting context" for its content.  Similar to making a block formatting context but the flex layout is the replacement with flexbox's built-in ability to adjust automatically.

## Manipulating Contents of Flexbox Container

Once we have a parent container with a display of flex there is a myriad of options we have for aligning, ordering, and structuring our content within.  They fall into three broad categories with their own subcategories. For the time being this repo will just include the basics to get you started using flexbox, you can dig into the [Sources and External Resources](#sources-and-external-resources) for additional and more detailed teachings.

1. Order & Orientation
    * **flex-direction:** row || row-reverse || column || column-reverse;
      * _Default:_ row
      * Defines which axis the container's children will be aligned along.
    * **flex-wrap:** wrap || no-wrap || wrap-reverse;
      * _Default:_ nowrap
      * Decides whether the container is a single or multi-line and the direction of its cross-axis thereby defining the direction new lines are placed.
    * **flex-flow:** row nowrap || column-reverse || column wrap || row-reverse wrap-reverse;
      * _Default:_ row nowrap
      * Since flex-direction and flex-wrap are often used in tandem we have the flex-flow property to use as a shortcut for setting the two in one property.
    * **order:** -1 || 0 || 1;
      * _Default:_ 0
      * The order property allows us to define the sequence in which children within a container will appear.  The property takes a single integer value which organizes the content starting with the lowest defined order and continues up from there.
2. Alignment
    * **justify-content:** flex-start || flex-end || center || space-between || space-around;
      * _Default:_ flex-start
      * This property will define the alignment of children items along the primary axis of the parent.
    * **align-items:** flex-start || flex-end || center || baseline || stretch;
      * _Default:_ stretch
      * Similar to justify-content with the exception it defines the alignment of items on the secondary axis.
    * **align-self:** flex-start || flex-end || center || baseline || stretch;
      * _Default:_ auto
      * As align items will organize all children elements align-self can be used to apply to only certain children.
    * **align-content:** flex-start || flex-end || center || space-between || space-around || stretch;
      * _Default:_ stretch
      * Similar to the workings of justify-content, align-content will organize a containers lines within where there is a surplus of space in the cross axis.
3. Flexibility
    * **flex-grow:** 0 || 1;
      * _Default:_ 0
      * Defines a "flex grow factor" given the integer passed to property and is used to scale children elements with more control.
    * **flex-shrink:** 0 || 1;
      * _Default:_ 1
      * Defines a "flex shrink factor" given the integer passed to property and is used to scale children elements with more control.
    * **flex-basis:** 30% || 50% || content;
      * _Default:_ auto
      * Another means of specifically targeting specific child elements this property uses the same values of width and height in addition to content.

There is a myriad of different options we have when utilizing Flexbox's properties, but there are two that take up a majority of what you will likely be using with flexbox.  For the time being, we will go into examples and more detail on Flex-Direction and Justify-Content. At the end of this repository, you will find all my sources for learning flexbox and links to the content so you can learn more about the pieces this guide doesn't get into great detail of.

## Order & Orientation

### Flex-Direction

Flex-direction, as the name suggests, defines the alignment of the children of a flex container with four options.

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

This property allows for the alignment of children along the primary axis of the flex container.  So if we have a parent container with row we will be justifying content along the X-Axis while if it were a column we'd be justifying it along the Y-Axis.

For the purpose of the following examples, the flex-direction will be a row but bear in mind the structuring applies the same for columns.

#### Flex-Start

Will justify the content among the beginning of the flex axis, so being a row we will "float the contents" to the start or left of the axis.

```css
.parent {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
}
```
![alt text](https://i.imgur.com/SbcPZye.png "justify-content: flex-start;")

#### Flex-End

I'm sure you're noticing some patterns by now.  Much like flex-start, flex-end will float the children elements to the end of the axis.  Since the flex-direction is the row that puts our little red buddies all the way to the right.

```css
.parent {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
}
```
![alt text](https://i.imgur.com/lJX7RpO.png "justify-content: flex-end;")

#### Center

Justify-Content: center; much like the rest of flexbox attribute values works exactly as it sounds.  It will center the contents of the container within the center of its flex-direction's axis.

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

Space around will adjust the content of the children elements automatically based on the space around them (not just between). Again the padding of the container and margin of the children will affect the final result of space-around.

```css
.parent {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}
```
![alt text](https://i.imgur.com/Gzc2uEn.png "justify-content: space-around;")

## Sources and External Resources

A lot of this walkthrough has come from three sources I used to pick up and practice the basics of flex-box.  You will find much more in-depth information from these links and the chance to practice and play with all the different properties.  Please get in touch if you find any additional resources you think would make a good addition to this repository!

- [CodeSchool: "Craking the Case with Flexbox"](https://www.codeschool.com/courses/cracking-the-case-with-flexbox)
  - Comes with the silly songs that go along with all of code school's content.  All joking aside this is the most in-depth and best source I found for really getting into the details with flexbox but more importantly the chance to practice use the properties and see them in real time.
- [Flexbox Froggy](http://flexboxfroggy.com/)
  - A great little game/practice site.  It has 24 levels that teach/test use of each of flexbox's properties.  Really good for solidifying what you've learned.
- [Flexbox Cheat Sheet](https://yoksel.github.io/flex-cheatsheet/)
  - My go-to source when I forget what it is specifically I'm trying to accomplish.  It's really useful in that it has a section for each property and interactive example where you can select a property value and see how it affects the container and it's children.
