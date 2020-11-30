# floating-labels
Floating Labels for Bootstrap

![Sample text input](https://i.imgur.com/zGK4SkX.png) 

## How to use

First Include the stylesheet in your html. If you prefers, use this CDN: https://cdn.jsdelivr.net/gh/exacti/floating-labels@latest/floating-labels.min.css
```html
<link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/gh/exacti/floating-labels@latest/floating-labels.min.css" media="screen">
```
Just put the input or textarea element inside a parent (div or span) with `.form-label-group` class and add a label tag after this element.
The input and label must have the same id linked with for in label to work properly. 

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

```html
<div class="form-label-group">
    <input type="text" id="tt3" class="form-control form-control-lg" placeholder="Floating Label lg" />
    <label for="tt3">Floating Label lg</label>
</div>
```

### For intl-tel-input
Make the label after input with JavaScript code, like this sample made with jQuery:
```JavaScript
$('.intl-tel-input ~ label').insertAfter('.intl-tel-input input.form-control');
```

## Dependencies

Works perfect with Bootstrap 4 but Bootstrap isn't required. Requires a browser compatible with [:placeholder-shown](https://caniuse.com/#feat=css-placeholder-shown) CSS pseudo-element.
