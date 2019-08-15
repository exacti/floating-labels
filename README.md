# floating-labels
Floating Labels for Bootstrap

![Sample without text input](https://i.imgur.com/JWEUrDi.png) ![Sample with text input](https://i.imgur.com/sro4kQC.png)

## How to use

First Include the stylesheet in your html.
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

## Dependencies

Works perfect with Bootstrap 4 but Bootstrap isn't required. Requires a browser compatible with [:placeholder-shown](https://caniuse.com/#feat=css-placeholder-shown) CSS pseudo-element.
