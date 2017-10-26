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

  These display propertetiers created flex containers which create a "flex formatting context" for it's content.  Similar to making a block formatting context but the flex layout is the replacement with it's built in ability to adjust automatically. 
