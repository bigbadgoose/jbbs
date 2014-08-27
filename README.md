# Jekyll Boilerplate with Bower and Bootstrap Sass


## Setup

0. These instructions assume Jekyll already
1. You will need [npm](https://npmjs.org/): `homebrew install npm`
2. You will also need [bower](http://bower.io/): `npm install -g bower`
3. Then run `bower install`
4. Finish off with `jekyll serve -w --trace`



## What is it?

This is a boilerplate for setting up Jekyll with Bower, Bootstrap, and Sass. Bonus: added Font Awesome

Uses Bower to install Bootstrap, jQuery, and Font Awesome, with Bootstrap and friends imported via custom imports and variables file.

The crux of the approach here is that all Bootstrap files are untouched - Bootstrap is effected by creating a custom import file, which itself imports a variables override file.

The file `bootstrap-variables-override.scss` is imported _after_ the default `_variables.scss` file, and is an identical copy with all lines commented out.
Developers should uncomment lines in the override file, and remove `!default` in those rules.

This will produce a clean interleave of your overrides on top of Bootsrap defaults while preserving the Bootstrap file and providing a canonical record of all overridden values for edification.

The only other change to the default Jekyll theme is addition of an `assets` folder



## What about Javascript?

The javascript setup is basic - using the html script tag to directly source the javascript files. Future versions may include grunt or other system to fancify this.



## Approach

- Kept simple
- Kept default
- Minimal starter
- Keeps as close as possible to canonical Jekyll theme example - minimal structural difference
