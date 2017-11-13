# Exercise 5 – Using SASS and BEM

## Variables

SASS is pretty much CSS with superpowers. One of the benefits is that SASS includes variables you can use for colors, 
layout or whatever you see fit and they look like this: 
```
$primary-color: #4F1F1F; 
$font-stack:    Helvetica, sans-serif;
```
And can be used like this: 
```
color: $primary-color;
font-family: Helvetica, sans-serif;
```
In this project the variables are found inside `css/scss/00-settings/_global-variables.scss`

### Task: Edit a variable
Create a new varable called `color-tamarillo` and give it the value of `#8C1414`. Change the 
`$color-hero-bg` to use the new varable and make sure the hero changes background color.

## Partials and import
In SASS partials are a way to modularize your CSS and make it easier to maintain. A partial is a file named with a 
leading underscore that can be included in other files by using the `@import` directive and will not be processed 
as its own css file. In our project all scss files are partials and is included inside the `style.scss` file which then
is processed to style.css.

### Task: create a new file
Create a new file inside `css/scss/04-components/navigation` that is called `_global-footer.scss`. Remember the 
underscore to indicate that the new file is a partial. The file is already getting included in the `style.scss`-file.

## Nesting and BEM
In SASS you can also nest your CSS. This will give CSS the same visual hierarchy as HTML.

```
.hero {
...
  &__image-container {
    ...
  }

  &__content-container {
    ...
  }

  &__content {
    ...
  }
}
```

The SASS will then be processed to look like this in a normal CSS file:

```
.hero{
    ...
}

.hero__image-container{
    ...
}

.hero__content-container{
    ...
}

.hero__content{
    ...
}

```

The & character makes the magic happen.

The double underscores comes from the BEM methodology. BEM stands for Block Element Modifier and is a  that 
helps creating reusable components and promotes code sharing. 

Examples: 
```
.block {}
.block__element {}
.block--modifier {}

.person {}
.person__hand {}
.person--female {}
.person--female__hand {}
.person__hand--left {}
```


### Task: Fill the footer with content
1. Add a copyright to the left and a list of links to the right of the footer which can be found in 
`02-organisms/00-global/footer.mustache`. Remember to mark your content with classes following BEM. 
If you want to know more about BEM you can take a look at 
[MindBEMding – getting your head ’round BEM syntax](https://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/)
or by looking inside `02-organisms/00-global/header.mustache`. 

2. Give the footer some styling in the `_global-footer.scss` that you created earlier. Remember nesting and use
variables for colors, fonts etc. 

3. Create a BEM-modifier class to the footer for example `global-footer--christmas` and add some style. 
Add the modifier class to the footer directly or by using a mustache `styleModifier` explained in 
[Exercise 4b](https://github.com/nerdschoolbergen/patternlab/tree/master/exercise4#exercise-4b---using-stylemodifier). 
If you use a `styleModifier` you need to include the footer pattern in a template. 

## Mixins
Mixins can be used to make a group of CSS declarations to be reused. Vendor prefixes, pseudo-icons, CSS-shapes and 
placeholders are good examples of mixins. You can find the mixins in this project inside 
`/css/scss/01-tools/_mixins.scss`. To create a mixin you use the `@mixin`-directive and to use a mixin `@include` 
is what you need.

## Operators
SASS includes operators (+, -, *, /, and %) that can be used to for example calculate width to create a fluent layout: 
```
width: 600px / 960px * 100%;
```
 