# CSS

## Inbox

- [Px v REM v EM](https://carlmultimedia.com/px-vs-rem-vs-em/)

--

## Log

--

## Notes

### components of css

```css
h1{
    color: blue;
    text-align: right;
}
```

- entire thing is a rule
- h1, selector
- {}, declaration block
- color: blue, individual declaration
- color, property
- blue, value

A CSS rule is a block of declarations which apply declaration properties and values to a selector.

### classes

- used for selecting multiple elements
- allows multiple of the same name per document
- .className

### id

- used for selecting distinct elements
- only one unique id with the same value per document
- #idName

### units

- ideally relative units will keep a site more responsive
- EM # TODO
- REM # TODO

### style

- use double quotes
- when a rule has multiple selectors put each selector on a new line with a comma

```css
h1,
h2,
h3 {
    color: blue;
    text-align: right;
}
```

### combinator

- describes the relationships between selectors
- allows for the combination of multiple selectors
- basic selectors
  - general sibling selector ( ~ )
  - adjacent sibling selector ( + )
    - selects the next sibling
  - child selector ( > )
  - descendant selector ( space )
    - selects the next child element
  - column selector (||)

### specificity

--

## End
