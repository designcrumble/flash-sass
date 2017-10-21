Flash-SASS
=============

a sass file structure to speed up your project setup

This boiler plate helps your team to kickstart projects. Index.html is basically your design system for the front end devs. They can jump and pick elements directly from it to have a fast and efficient code flow.

<!-- This build methodology is currently being used on  -->

SASS Directories
----------

1.  Base

	The base directory contains styles that help start a project. The base directory could contain the following type of SASS files:
  * Typography
	* Reset

2.  Layout

	The layout directory contains styles that are large containers of a page. This directory could include SASS files like:
	* Responsive Grid
	* Page specific layouts

3.  Components

	The modules directory will probably contain the bulk of your SASS files. A page may consist of multiple modules and should be styled individually. These modules may include files like:
	* Header
	* Footer
	* Navigation
	* Content Block

4.  Helpers

	The views directory contains any specific styles that a page may need to change from the generic layout or modules. For example the header in your website maybe green throughout a website or application but on a specific page you want it to change to a blue background that's where the views files would come in.

  * Authored dependancies (Mixins, variables, Extends)

5.  Pages

  Page specific styles

6.  Themes

  The views directory contains any specific styles that a page may need to change from the generic layout or modules. For example the header in your website maybe green throughout a website or application but on a specific page you want it to change to a blue background that's where the views files would come in.

7.  Vendors

  Include any external libraries here.

  * Vendor dependancies (Compass, Foundation)

## Rules

  - There should only be a maximum of 2 CSS files per page ( this prevents HTTP requests )
  - One line for each selector or rule
  - List related items together
  - Only nest 3 levels deep
  - Break files out into small modules (avoid having a SCSS file that is larger than 100 lines)
  - Avoid using IDs throughout the site. Use IDs for parent elements. Example: Header, Footer, Main. Using Classes avoids having to use !important 
  - Be generous with commenting
  - If a ```:hover``` pseudo class is styled, ```:focus``` should also be styled for accessibility.
  ## CSS

### Formatting

* Use soft tabs (2 spaces) for indentation
* Prefer dashes over camelCasing in class names.
  - Underscores and PascalCasing are okay if you are using BEM (see [OOCSS and BEM](#oocss-and-bem) below).
* Do not use ID selectors
* When using multiple selectors in a rule declaration, give each selector its own line.
* Put a space before the opening brace `{` in rule declarations
* In properties, put a space after, but not before, the `:` character.
* Put closing braces `}` of rule declarations on a new line
* Put blank lines between rule declarations

**Bad**

```css
.avatar{
    border-radius:50%;
    border:2px solid white; }
.no, .nope, .not_good {
    // ...
}
#lol-no {
  // ...
}
```

**Good**

```css
.avatar {
  border-radius: 50%;
  border: 2px solid white;
}

.one,
.selector,
.per-line {
  // ...
}
```

## Commenting
  - Using "// " for your comments in SASS and they will not output in the compiled CSS


## Variables
  - Any values commonly throughout the SASS build should be set as a variable (fonts, colors, percentages, z-index)
  - All colors should be variables


## Order of imports
  - Vendor dependancies (compass)
  - Authored dependancies (Mixins, variables)
  - Base styles ( reset, fonts, typography )
  - Layout styles
  - Modules styles
  - Views styles

## Release History

* 0.1.0: Initial release.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
6. Change commit name and email (`git commit --amend --author="name <email@address.com>"`)
