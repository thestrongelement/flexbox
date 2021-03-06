# flexbox

If you're using flexbox for the first time don't get too bogged down in all the properties, just start simply.

## demo
See it at http://www.thestrongelement.com/flexbox/

## getting started

Take something very basic. 

This will equalize the width of the `<span>` and `<strong>` elements.
```html
<style>
  p { display: flex; }
  span, strong { flex: 1; }
</style>
<p>
  <span>the</span>
  <strong>strong</strong>
  <span>element</span>
</p>
```

If you need them stacked:
```css
p { ...; flex-flow: column; }
```
*Note:* By default, you won't see much happen above. You'll still need to make the flex container 100% of the browser height using old tricks like `p { ...; position: absolute; height: 100%; }`

Reverse the order:
```css
p { ...; flex-flow: column-reverse; }
```

If we want "**strong**" to take up 2x more space:
```css
strong { flex: 2; }
```
*Hint: You can use decimals, e.g. 1.5. And you can animate it!*

That's a good start. 

## should you use it?
Yes, yes, yes.

http://caniuse.com/#search=flexbox

###should you use prefixes?
Yes.

###IE?
Usually, you can use floats or let elements stack for IE 8 and 9 and still achieve good results. Float rules have no effect on flex items.

Developers have been coding clever layouts for a long time so you can resort to Javascript and polyfills if you must support aging IEs.

##helpful resources
Extensive overview of all flex properties
https://css-tricks.com/snippets/css/a-guide-to-flexbox/

Great tool (at the bottom) for exploring options 
https://scotch.io/tutorials/a-visual-guide-to-css3-flexbox-properties

Shows various form options
http://philipwalton.github.io/solved-by-flexbox/demos/input-add-ons/