# sassiness

A small package that holds beautiful modular SASS Mixins

*put logo here*

***

##Install

Install using npm `npm i sassiness`

Place `@include "~sassiness/sassiness.sass"` at the top of your `App.sass` (or `App.scss`)

***

##Example Usage 

Below is an example of how to use the mixins. Each other mixin works the same way; by placing the variables inside the ($).

###center-box

```scss
/* this is imported */
@mixin center-box($width, $margin_vertical)
    width: $width
    margin: $margin_vertical (100 - $width) / 2
```

```scss
/* in your App.sass file ('$' are your variables) */
.div 
    @include center-box($width, $margin_vertical)
```

```css
/* compiled css code */
.div 
	width: 80%;
	margin: 25px 10%;
```

***

#Current Mixins Available

Below is a list of possible @include mixins. If you wish to see what they are all doing behind the scenes, look in the node_modules/sassiness/sassiness.sass file.

###background-image
```scss
@include background-image($url, $size, $position, $repeat, $color) 
```

###hover-transition
```scss
@include hover-transition($sec) 
```

###border-radius
```scss
@include border-radius($size) 
```

###box-shadow
```scss
@include box-shadow($color, $radius, $spread)  
```

###list-reset
```scss
// sets padding + margins to 0 and list-style: none
@include list-reset;  
```

### clearfix
```scss
// Clearfix hack for parent with floating children
@include clearfix
```

### placeholder
```scss
// $fontsize is optional
@include placeholder($color, $fontsize)
```

***
