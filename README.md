# typeset

LESS mixin for typesetting

## .typeset

TBD

## .typeset.scale

Provide a font size basis and scale factor in a natural language form.

```css
  .typeset.scale(18px by 1.25);
```

## .typeset.scale.size;

Scale the base font provided exponentially with relative integers from negative infinity to infinity.

```css
  .typeset.scale.size(+1);
```

Scale the base font provided exponentially with the keywords: 
- xx-small (-2), 
- x-small (-1), 
- medium (0), 
- large (1), 
- x-large (2), 
- and xx-large (3).

```css
  .typeset.scale(18px by 1.25);
  .typeset.scale.size(medium); //-> font-size: 18px
```
