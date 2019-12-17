[UP](./index.md)

# Animation Shorthand Property
sets an animated transition between styles. It is a shorthand for:
- animation-name (initial value: none),
- animation-duration (initial value:0s),
- animation-timing-function (initial value:ease),
- animation-delay (initial value:0s),
- animation-iteration-count (initial value:1),
- animation-direction (initial value:normal),
- animation-fill-mode (initial value:none),
- animation-play-state (initial value:running)  

The order of values within each animation definition is important: 
- the first value that can be parsed as a <time> is assigned to the animation-duration
- and the second one is assigned to animation-delay.