### PNI SCSS Style-Guide

## Formatting
* Use hyphens when naming mixins, extends, classes, functions & variables: `span-columns` not `span_columns` or `spanColumns`.
* Use one space between property and value: `width: 20px` not `width:20px`.
* Avoid using shorthand properties for only one value: `background-color: #ff0000;`, not `background: #ff0000;`
* Use `//` for comment blocks not `/* */`.
* Use one space between selector and `{`.
* Use double colons for pseudo-elements
* Mark todos and action items with `TODO`.  `// TODO: action item`

## Order
* Place `@extends` and `@includes` at the top of your declaration list.
* Place media queries directly after the declaration list.
* Place pseudo-classes and pseudo-elements second.
* Place nested elements third.

## Selectors
* Avoid the use of ID's for style.
* Use ID and class names that are as short as possible but as long as necessary.
* Avoid nesting more than 3 selectors deep.
* Avoid nesting within a media query.

## File
* Partials are named `_partial.scss`

## GIT
* The format for the commit is `[type-of-work] / [JIRA ticket number]` the type of work could be: `feature`, `hotfix` or `release`. ie. `feature/SPLS-01`

### Example

```css
$some-colour: #fff

.some-element {
    @include (flexbox);
    @include justify-items(center);

    // TODO: some action item

    height: 20px;
    width: 0;
    background-color: $some-colour;

    @media ($tablet) {
        height: 10px;
    }

    &::before {
        content: '';
    }

    .some-nested-element {
        .another-nested-element {
            // STOP!
        }
    }
}

```
