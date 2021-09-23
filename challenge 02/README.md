# General Button Styling Tips

### Hover Area for Link Buttons

In the HTML for this challenge, there are two rows of identical buttons, except the first row of buttons has the button class directly on the `<a>` elements, whereas the second row of buttons has a `<p>` element surrounding each button and the button class is on the `<p>` element. They look the same. But there is an important difference. 

![](https://raw.githubusercontent.com/hoc-labs/images/main/rdb-styling-buttons-img5.png)


Hover over the button in each of the rows. Can you see the difference? For the buttons in the second row, where the button class is on the `<p>` element, the hover does not appear until you hover over the text within the `<a>` element.

This is because the `<a>` element has built-in support for changing the cursor to a pointer when the user hovers over it, whereas the `<p>` does not.

**When using an `<a>` as a button, you must add the padding to the `<a>` element, not its parent.**

### Link Button Padding

Another issue with adding padding to any button, `<a>` or a `<button>` element, is that you should always use padding and not hard-code a fixed width and height.

* **remove the second row of buttons for this step since we no longer need them.**

* **remove the padding property from the .button style and replace it with a width and a height.**

```css
.button {
    width: 175px;
    height: 50px;
}
```

![](https://raw.githubusercontent.com/hoc-labs/images/main/rdb-styling-buttons-img6.png)

Notice any issues? 

* The first issue is it's hard to know what width and height to use.
* The bigger issue is the button requires a lot of additional styling to center the text.

It's certainly possible to style it, but let's take a look at what happens when we accept the default height, add padding for width, and text-align:center.

```css
.button {
  display: inline-block;
  background: #FFE600;
  color: black;
  width:175px;
  /* add */
  padding: 15px 0;
  text-align:center;
  /* remove
  height:75px; 
  */
}
```

and view the page.

![](https://raw.githubusercontent.com/hoc-labs/images/main/rdb-styling-buttons-img7.png)

The problem is the padding on the left/right are not equal when we use a fixed width.

**Always using padding to get a uniform padding around the button text**.

It is also usually best practice to add more padding to the width than the height, in about a 1.5-2.0:1 ratio.

**Add a padding of 16px on the top/bottom and 24-32px on the left/right and view the page again. How does that look?











