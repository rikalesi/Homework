## Folder Structure

The folder [src](src) has the following folder structure:

```bash
src
├── assets
│      ├──css
│      │   └── style.css
│      └── images
│          ├── image-1.png
│          └── image-2.png
└── index.html
```

---

### About the display property

- We use the `display` property to set whether an element behaves as an inline or a block element

  - **Inline elements** only occupy as much width as needed and do not automatically start a new line.

    - Images and `<a>` elements are examples of inline elements.

  - **Block elements** always start on a new line and occupy as much width as there is available.

    - Paragraph and unordered lists are examples of block elements.

  - We can also use `display` to hide an element.

---

## style.css

```css
body {
  background-color: #f8fcfd;
}
h1,
h2,
h3 {
  text-align: center;
}
h3 {
  font-size: 20px;
  line-height: 2px;
}
h4 {
  font-size: 18px;
}
a {
  font-size: 16px;
  color: #181510;
}
section {
  margin: 0 auto;
  width: 80%;
  background-color: #f6e9c9;
}
.first-element {
  background-color: lightblue;
}
.second-element {
  background-color: goldenrod;
}
/* We use `display: block` to indicate a block element, which will occupy the whole width available */
.display-block {
  display: block;
}
/* We use `display: inline` to indicate an inline element, which will only occupy the necessary width */
.display-inline {
  display: inline;
}
/* We use `display: none` to completely remove an image so that it does not appear on the page and no longer occupies space in the layout */
.display-none {
  display: none;
}
```

## index.html

```html
<!DOCTYPE html>
<html lang="en-GB">
  <head>
    <meta charset="UTF-8" />
    <title>HTML Display</title>
    <link rel="stylesheet" href="./assets/css/style.css" />
  </head>

  <body>
    <header>
      <!-- Headers -->
      <h1>CSS Display Property</h1>
    </header>

    <section>
      <h2>Inline Elements</h2>
      <h3>do not start on a new line</h3>
      <h3>and only take up as much width as necessary.</h3>
      <!--Anchor elements <a> are inline elements-->
      <h4>Anchor elements</h4>
      <a
        class="first-element"
        href="https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements"
        >MDN Web Docs on Inline Elements</a
      >
      <a
        class="second-element"
        href="https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements"
        >MDN Web Docs on Block-Level Elements</a
      >
      <!--Images <img> are inline elements-->
      <h4>Image elements</h4>
      <img
        class="first-element"
        src="./assets/images/image-1.png"
        alt="box with text reading 200w 200h"
      />
      <img
        class="second-element"
        src="./assets/images/image-2.png"
        alt="box with text reading 200w 200h"
      />
    </section>

    <section>
      <h2>Block Elements</h2>
      <h3>always start on a new line and take up the full width available.</h3>
      <!--Paragraph <p> elements are block elements-->
      <h4>Paragraph elements</h4>
      <p class="first-element">This is a paragraph.</p>
      <p class="second-element">
        This is a paragraph with <strong>BOLDED TEXT</strong>.
      </p>
      <!--Unordered lists are block elements-->
      <h4>Unordered list</h4>
      <ul>
        <li class="first-element">This is list item one</li>
        <li class="second-element">This is list item two</li>
      </ul>
    </section>

    <section>
      <h2>display:inline</h2>
      <h3>changes a block element's property to inline.</h3>
      <h4>Paragraph element with display:inline</h4>
      <p class="first-element display-inline">This is a paragraph.</p>
      <p class="second-element display-inline">
        This is a paragraph with <strong>BOLDED TEXT</strong>.
      </p>
    </section>

    <section>
      <h2>display:block</h2>
      <h3>changes an inline element's property to block.</h3>
      <h4>Image elements with display:block</h4>
      <img
        class="first-element display-block"
        src="./assets/images/image-1.png"
        alt="box with height and width text"
      />
      <img
        class="second-element display-block"
        src="./assets/images/image-2.png"
        alt="box with height and width text"
      />
    </section>

    <section>
      <h2>display:none</h2>
      <h3>hides an element.</h3>
      <h4>Unordered list with display:none</h4>
      <ul class="display-none">
        <li>This is list item one</li>
        <li>This is list item two</li>
      </ul>
      <br />
    </section>
  </body>
</html>
```
