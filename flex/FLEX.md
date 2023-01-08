# Flexbox Layouts

Website templates using css flexbox.

## Description

* The `layout1.html` template renders `header, body, sidebar, and footer` elements. In this variation we have used flex's default direction `row` for making flexible layout and `header` & `footer` are set with `min-height` value that's why we had to subtract `header` and `footer` heights manually.

Here is the CSS snippet for making this layout:

```
header {
  min-height: 20vh;
  /* other header styles go here */
}

main {
  display: flex;
  /* Subtract header and footer height manually */
  min-height: calc(100vh - 40vh);
  /* other main content styles go here */
}

footer {
  min-height: 20vh;
  /* other footer styles go here */
}
```

* The `layout2.html` template renders `header, body, and footer` elements. But we include the `body` element as a flexible layout. I'd recommend using this variation as this is much simpler.

Here is the CSS snippet for making this layout:

```
body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

header {
  flex: 0 0 auto;
  /* other header styles go here */
}

main {
  flex: 1 0 auto;
  /* other main content styles go here */
}

footer {
  flex: 0 0 auto;
  /* other footer styles go here */
}
```

* The `layout3.html` template renders `header, body, and footer` elements too. We're going to improve the `layout2.html` a bit by replacing the `body` element with a `div` element.

Here is the CSS snippet for making this layout:

```
.app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

header {
  flex: 0 0 auto;
  /* other header styles go here */
}

main {
  flex: 1 0 auto;
  /* other main content styles go here */
}

footer {
  flex: 0 0 auto;
  /* other footer styles go here */
}
```

## Don't

* Don't use fixed `height` for locking element's height, use `min-height` instead
* Don't use fixed `width` for locking element's width, use `max-width` instead
