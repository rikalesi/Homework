## Folder Structure

```bash
src
├── assets
│      ├──css
│      │   └── style.css
│      └── images
│          ├── image-1.png
│          ├── image-2.png
│          ├── image-3.png
│          └── image-4.png
└── index.html
```

# style.css

```css
h1,
h2,
h3 {
  text-align: center;
}
header {
  width: 100%;
  border: 10px solid darkblue;
  background-color: lightblue;
}
section {
  height: 400px;
  width: 80%;
  margin: 30px auto;
  border: 10px solid black;
}
/* When an element's position is `relative`, it stays in the normal flow but can be offset by a value provided in the CSS
 */
#relative-box {
  position: relative;
  left: 200px;
}
/*When an element's position is `absolute`, it is no longer in the normal flow but instead is positioned relative to its ancestor element and is determined by values provided for top, bottom, left, and right */
#absolute-section {
  position: relative;
}
#absolute-box {
  position: absolute;
  top: 50px;
  right: 100px;
}
/* An element in the `fixed` position is also not in the normal flow. However, unlike `absolute`, the position is determined in relation to the viewport */
#fixed-box {
  position: fixed;
  bottom: 0;
  right: 0;
}
```

# index.html

```html
<!DOCTYPE html>
<html lang="en-GB">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="./assets/css/style.css" />
    <title>CSS Positioning</title>
  </head>

  <body>
    <header>
      <h1>CSS Positioning</h1>
    </header>

    <section>
      <h2>Static Position</h2>
      <img src="./assets/images/image-1.png" alt="box with number 1" />
      <h3>Element is in normal flow. This is the default value.</h3>
    </section>

    <section>
      <h2>Relative Position</h2>
      <img
        id="relative-box"
        src="./assets/images/image-2.png"
        alt="box with number 2"
      />
      <h3>Element is in normal flow but is offset based on provided value.</h3>
      <h3>
        The values top, right, left and bottom can be used to offset element.
      </h3>
    </section>

    <section id="absolute-section">
      <h2>Absolute Position</h2>
      <img
        id="absolute-box"
        src="./assets/images/image-3.png"
        alt="box with number 3"
      />
      <h3>The element is removed from the normal flow.</h3>
      <h3>
        Its final position is relative to the positioned parent or ancestor
      </h3>
      <h3>and is determined by the values of top, right, bottom, and left.</h3>
    </section>

    <section>
      <h2>Fixed Position</h2>
      <img
        id="fixed-box"
        src="./assets/images/image-4.png"
        alt="box with number 4"
      />
      <h3>The element is removed from the normal document flow.</h3>
      <h3>
        The final position is relative to the viewport and determined by the
        values of top, right, bottom, and left.
      </h3>
    </section>
  </body>
</html>
```
