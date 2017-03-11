# Chartboost Coding Challenge: Dinosaur Database
## Demo
[http://yarunluon.github.io/chartboost/dinosaurs/](http://yarunluon.github.io/chartboost/dinosaurs/)

## Task
Create a simple web app for searching the Chartboost Dinosaur Database for dinosaurs filtered by geographical time period.

## Accuracy
I tried my best for accuracy, but trade-offs between time and responsiveness were made.

#### Fonts
I used the fonts from Chartboost.com.
```css
font-family: proxima-nova, 'Proxima Nova', Helvetica, Arial, sans-serif;
```

#### Nav bar
I didn't use the same width as the mockup (245px) instead relying on Bootstrap's grid system to set the navigation width.

#### Select Box
Styling select boxes is difficult. One option was to recreate the behavior using either `<div>` or a combination of `<ul>`, `<ol>` elements. Instead, to save time, I decided to use Bootstrap's default styling of `<select>`. Another option was to use Bootstrap's dropdown menus, but this requires rewiring the dropdown behavior to match the `<select>` behavior.

## Durability
#### Backbone/Marionette
Backbone/Marionette was used as the MVC framework to keep the presentation layer separate from the data layer.

#### Sass
Styles were written using sass to make the css more DRY.

#### Small files
Many small files let multiple people work on the code base at the same time without causing merge conflicts.

#### Design note
Instructions specifically state:
> The minimum requirement is a single, static `index.html` that we can drag into a browser window (Chrome).

With this requirement, templates are stored in `index.html` and `period` json are hardcoded into the models to prevent XSS violations. Otherwise, templates would be in separate html files for better maintainability and json would be loaded from disk to better mimic a server call.

## Performance
I used best practices whenever possible. I am happy to hear any that I missed!

#### Next steps
To further improve performance, we could minify and concatenate the css and js files.

## Comprehension
Uses MVC design pattern for quicker comprehension. Source code is marked up with JSDoc annotation.

## Delight
* Website is responsive.
* If given more time, animations would be added to ease the transitions between periods.
* Additional error message was added to account for non-404 errors.

## Installation
Dragging `index.html` into Chrome is sufficient. Additionally, file can be hosted from a simple Node server.

#### Install Connect Server and gulp-sass
Installs a light weight server to serve static pages. Requires [Node](https://nodejs.org/en/).
```sh
$ npm install
```

#### Start server
```sh
# http://localhost:8080
$ node server.js
```

#### Generate documentation
```sh
$ gulp jsdoc
```
