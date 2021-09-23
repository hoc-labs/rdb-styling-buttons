# Buttons

### Form vs Link Buttons
There are two scenarios where you use buttons:
* **Part of a form**. There is a special-purpose HTML element, `<button>`, that is used for submitting the form. The `<button>` element should only be used within a form. We'll cover it when we work with forms.
* **A link that looks like a button**. In this case we need to style an `<a>` element to look like a button. An `<a>` element has built-in support for displaying a pointer cursor when you hover over the element, giving the user feedback that the element can be clicked.

### Styling Link Buttons

Below is what the starter HTML/CSS looks like. It has two `<a>` elements at the bottom that just have a simple CSS style to set the text color to yellow.

![](https://raw.githubusercontent.com/hoc-labs/images/main/rdb-styling-buttons-img1.png)

We want the buttons to look like the screen capture below, with the links at the bottom styled so that they look like buttons.

![](https://raw.githubusercontent.com/hoc-labs/images/main/rdb-styling-buttons-img2.png)


There are some issues that we need to address when using an `<a>` element as a button.

## Setting display:inline-block

Create a CSS style, named `button`, that will be used to style the `<a>` elements that will be buttons.

```css
.button {
  background-color:#FFE600;
  color:black;
  padding:50px;
}
```
```markup
<p class="links">
    <a class="button" href="#">contact me</a> 
    <a class="button" href="#">learn more about me</a>
</p>
```
This is what the content looks like after the new style has been applied. The padding is overlapping the content above. Why is that?

![](https://raw.githubusercontent.com/hoc-labs/images/main/rdb-styling-buttons-img3.png)

### Inline elements do not support padding/margins.

It is because the `<a>` element is an inline element (display:inline) and inline elements do not support adding padding or margins. If you add padding or margins it does not add space to the element. It just pushes out over the top of the surrounding elements.

### Inline-block elements do support padding/margins.

`display:inline-block` keeps the content inline, but allows the padding/margins to be applied.

Therefore, we need to change the display property of the `<a>` element that is being styled as a button to inline-block.

**Add `display:inline-block` to the `.button` style and view the page again.**

Now, with .button having display:inline-block set, but still keeping the large padding, this is what it looks like. The padding is adding padding within the border of the `<a>` element.

![](https://raw.githubusercontent.com/hoc-labs/images/main/rdb-styling-buttons-img4.png)

**Set the padding back to a reasonable amount, such as 10px.**

The button are now starting to look more like buttons. In the next challenge we'll improve on the styling.

![](https://raw.githubusercontent.com/hoc-labs/images/main/rdb-styling-buttons-img3.1.png)

















