# Media Queries

How do you make your portfolio look nice on both desktop and mobile? One way is
to use CSS media queries.

```css
/* A rule that will be used on all devices */
h1 {
  font-size: 2em;
  color: white;
  background-color: black;
}

/* change the h1 to use less ink on a printer */
@media print {
  h1 {
    color: black;
    background-color: white;
  }
}

/* make the font bigger when shown on a screen at least 480px wide */
@media screen and (min-width: 480px) {
  h1 {
    font-size: 3em;
    font-weight: normal;
  }
}
```
