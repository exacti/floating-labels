# floating-labels
Floating Labels for Bootstrap

![Sample text input](https://i.imgur.com/JxO24vv.png) 

## How to use

First Include the stylesheet in your html. If you prefers, use this CDN: https://cdn.jsdelivr.net/gh/exacti/floating-labels@latest/floating-labels.min.css

```html
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/exacti/floating-labels@latest/floating-labels.min.css" media="screen">
```
Just put the input or textarea element inside a parent (div or span) with `.form-label-group` class and add a label tag after this element.

The input and label must have the same id linked with for in label to work properly. Input must have the `placeholder` defined.

For in border style (like outlined material design), add the `.in-border` class. For fully outline style with transparency, use the `outline` class. If you use `outline` class, the label tag must be inside a span tag. The diference beteween in-border and outline is the background. In-border have a white background and outline is transparent with only border.

#### Code samples

```html
<div class="form-label-group">
    <textarea id="tt" class="form-control" placeholder="Floating Label area" rows="4"></textarea>
    <label for="tt">Floating Label area</label>
</div>
```

```html
<div class="form-label-group">
    <input type="text" id="tt2" class="form-control" placeholder="Floating Label" />
    <label for="tt2">Floating Label</label>
</div>
```

Like outlined material design

In-border:
```html
<div class="form-label-group in-border">
    <input type="text" id="tt3" class="form-control form-control-lg" placeholder="Floating Label lg" />
    <label for="tt3">Floating Label lg</label>
</div>
```

Outline:
```html
<div class="form-label-group outline">
    <input type="text" id="tt2" class="form-control" placeholder="Floating Label" />
    <span><label for="tt2">Floating Label</label></span>
</div>
```

### For intl-tel-input

You can put the flag's container on the right using `iti-right` class.

Make the label after input with JavaScript code, like this sample made with jQuery:
```JavaScript
$('.intl-tel-input ~ label').insertAfter('.intl-tel-input input.form-control');
```

Or this most advanced code (ideal for 2 or more elements):
```JavaScript
$('.intl-tel-input, .iti').find('input.form-control').each(function(index, element) {
	let label = $(element).parent().find('~ label');
	$(element).after(label);
});
```

## Dependencies

Works perfect with Bootstrap 4 but Bootstrap isn't required. Requires a browser compatible with [:placeholder-shown](https://caniuse.com/#feat=css-placeholder-shown) CSS pseudo-element.
