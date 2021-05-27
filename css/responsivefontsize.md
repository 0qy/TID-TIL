# Maths formula for responsive font size!

```text
body {
  font-size: calc([minimum size] + ([maximum size] - [minimum size]) * ((100vw - [minimum viewport width]) / ([maximum viewport width] - [minimum viewport width])));
}
```

Example:

```text
body {
  font-size: calc(14px + (26 - 14) * ((100vw - 300px) / (1600 - 300)));
}
```

[source](https://css-tricks.com/books/fundamental-css-tactics/scale-typography-screen-size/) [credit](https://madebymike.com.au/writing/fluid-type-calc-examples/)

