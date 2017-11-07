# Material Drop Shadow Elevation

This is like [@material/elevation][1], but uses [`drop-shadow`][2] CSS filter
instead of a `box-shadow` property. This allows to use it on weird shaped things
like [CSS triangles][3].

```
npm install material-ds-elevation
```

Usage:

```scss
@import "material-ds-elevation/functions";
.my-element {
  // Instead of:
  //   @include mdc-elevation(2);
  // Use:
  filter: drop-shadow-elevation(2);

  &::before {
    @include make-me-a-triangle(bottom); // not included :P
  }
}
```

## TODO

- Add transitions


[1]: https://github.com/material-components/material-components-web/tree/master/packages/mdc-elevation
[2]: https://developer.mozilla.org/en-US/docs/Web/CSS/filter-function/drop-shadow
[3]: https://css-tricks.com/snippets/css/css-triangle/
