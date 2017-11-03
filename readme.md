# Simple Node.js App

## Installation:
* `npm i` 

## How to run:
* `npm run watch` Builds and watches jade files in `source/templates/` and the index.scss stylesheet in `source/stylesheets/`.
* `npm run build` Builds project files.
* `npm run clean` Deletes and recreates the built stylesheets.
* `npm run watch-css` Only watches `source/stylesheets/index.scss` for changes.

#### Commands referenced above:
```
"build-css": "node-sass source/stylesheets/index.scss --use autoprefixer --output-style compressed -o static/css",
"watch-css": "node-sass source/stylesheets/index.scss --use autoprefixer -o static/css -w",
"clean": "rm -rf static/css && mkdir -p static/css",
"build": "npm run clean && npm run build-css",
"watch": "npm run clean && npm run build-css && npm run watch-css & nodemon server -e js,jade",
"start": "node server"
```