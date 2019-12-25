# Cascade Style Sheets

Comments: `/* COMMENT HERE */`

Syntax
CSS has two building blocks: a **property** and a **value**
- Declaration	`prop:val`
- Declaration Block	`{prop:val}`

Three ways to use CSS:
- **inline style attribute** `style="color:blue;"`
- **style tags** `<style>h1 {color: blue;}</style>`
- **external style sheet** `<link rel="stylesheet" href="./styles.css"

Selectors
- CSS Rule	`selector {prop:val}`
- by type `p {color:red}`
- by class `.done {color:red}`
- by id `#warn {color:red}`
- universal `* {color:red}`
- advanced selectors ([by attribute](./attr.md), [pseudo-classes](./ps-class.md), [pseudo-elements](./ps-ele.md), [combinators](./comb.md))

[Variables](./variables.md)

[At-Rules](./at-rules.md)

[Units](https://www.w3schools.com/css/css_units.asp) (relative & absolute)

[Inheritance](./inheritance.md) (which selector wins) 

[Box Model](https://www.w3schools.com/css/css_boxmodel.asp)
- Diagram (https://www.tutorialrepublic.com/lib/images/css-box-model.jpg)
- `box-sizing` property defines how the user agent should calculate the total width and height of an element (values: [content-box](./content-box) vs [border-box](./border-box.md))
- `overflow` [property](https://www.w3schools.com/css/css_overflow.asp): clip content or use scroll bars (values: visible, hidden, scroll, auto)

Layout
- `position` [property](https://www.w3schools.com/css/css_positioning.asp) (values: static, relative, fixed, absolute, sticky)
- `float` and `clear`[properties](https://www.w3schools.com/css/css_float.asp)

Visuals
- [Fonts](https://www.w3schools.com/css/css_font.asp) ([google fonts](./fonts-google.md), [properties](./fonts-properties.md))
- Colors ([picker](https://www.w3schools.com/colors/colors_picker.asp), [methods](./color-methods.md), [theory](./color-theory.md), [hsl()](./hsl.md))

Graphics
by manipulating different selectors and properties, you can make interesting shapes (e.g. [crescent moon](./crescent-moon.md), [heart](./heart.md) )
- [Animations](./animate/index.md)

- [Icons](https://www.w3schools.com/css/css_icons.asp)
- Short Hands

Responsive Web Design
- [Flex](./flex/index.md)
- [Grid](./grid/index.md)

Frameworks
- [w3.css](https://www.w3schools.com/w3css/w3css_references.asp)
- Bootstrap
