# typeset

LESS mixin for typesetting

## .typeset

Set the font-basis for a closure.

### Usage

```css
  .typeset(18px);
```

## .typeset.scale

Provide a font size basis and scale factor in a natural language form.

### Usage

```css
  .typeset.scale(1.5);
```

## .typeset.scale.size;

Scale the base font provided exponentially with relative integers from negative infinity to infinity.

### Usage
```css
  .typeset(18px);
  .typeset.scale(1.5);
  .typeset.scale.size(+1); //-> font-size: 24px
```

### Keyword support
- xx-small (-2), 
- x-small (-1), 
- medium (0), 
- large (1), 
- x-large (2), 
- and xx-large (3).

### Keyword usage
```css
  .typeset(18px);
  .typeset.scale(1.5);
  .typeset.scale.size(large); //-> font-size: 24px
```

## .typeset.grid
Set the resolution of the baseline grid. By default, the grid resolution is same the font basis. Increasing resolution, sub-divides the basis to create more grid lines to snap content to.

### Usage
```css
  .typeset(18px);
  .typeset.grid(sqrt(18)); // square root of basis is default
```

## .typeset.grid.line-height
Set line-height as a basis for alignment with the baseline grid. 

### Parameters
- Font-size
- line-height basis

### Usage
```css
  .typeset(18px);
  .typeset.grid;
  .typeset.grid.line-height(18px, 1.2);
```

### Usage with font scaling 
Passing a ruleset to scale provides a 'font-size' variable.
```css
  .typeset.scale.size(xx-large, {
    font-size: @font-size;
    .typeset.grid.line-height(@font-size, 1.2);
  });
```

## DRY example
The examples above are atomic and, although functional, are unneccessarily repetitious. This [GIST](#) shows a more realistic usage of these mixins where a lexical approach greatly reduces repetition.
