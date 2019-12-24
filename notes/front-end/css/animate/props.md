[UP](./index.md)

# animation properties
animation properties control how the animation should behave

## [animation](./shorthand.md)
[example](./eg/animation.md)  
shorthand for multiple animation properties  

## animation-delay
[example](./eg/delay.md)  
sets when an animation starts

## animation-direction
[example](./eg/direction.md)  
sets whether an animation should play forwards, backwards, or alternating back and forth.

- **normal** - The animation is played as normal (forwards). This is default
- **reverse** - The animation is played in reverse direction (backwards)
- **alternate** - The animation is played forwards first, then backwards
- **alternate-reverse** - The animation is played backwards first, then forwards

## animation-duration
[example](./eg/duration.md)  
sets the length of time for the animation.

## animation-fill-mode
[example](./eg/fill.md)  
sets how a CSS animation applies styles to its target before and after its execution.  

- **none** - Default value. Animation will not apply any styles to the element before or after it is executing
- **forwards** - The element will retain the style values that is set by the last keyframe (depends on animation-direction and animation-iteration-count)
- **backwards** - The element will get the style values that is set by the first keyframe (depends on animation-direction), and retain this during the animation-delay period
- **both** - The animation will follow the rules for both forwards and backwards, extending the animation properties in both directions

## animation-iteration-count
allows you to control how many times you would like to loop through the animation  
values: **[number]**, **infinite**

## animation-name
sets the name of the animation, which is later used by @keyframes to tell CSS which rules go with which animations.

## animation-play-state
[example](./eg/state.md)  
sets whether an animation is **running** or **paused**.

## [animation-timing-function](./timing.md)
[example](./eg/timing.md)  
sets how an animation progresses through the duration of each cycle.