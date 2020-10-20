## Import font-su to IcoMoon (in order to update)
1. Import `selection.json` to the IcoMoon app using the `Import Icons` button.

## Export from IcoMoon
1. 

## Update font-su repo
1. checkout `master` to your local `font-su` repo.
1. Export font from icomoon. See [Exporting from IcoMoon](#export-from-icomoon)
1. Open downloaded zip files.
1. Move `styles.scss` and `variables.scss` to the `/scss` folder.
1. Open `styles.scss` and update `$icomoon-font-path: "fonts" !default;` to `$icomoon-font-path: "../fonts" !default;`
1. Move `style.css` to the `/css` folder.
1. Open `styles.css` and update font urls from `fonts/` to `../fonts/` (ex: update `fonts/font-su.eot?eiodpz` to `../fonts/font-su.eot?eiodpz`)
1. Go to [CSS Minifier](https://cssminifier.com/). Copy/paste the code from `style.css`, click "Minify", copy minified code to clipboard, and replace the code in `css/style.min.css`

## Documentation (Github Pages)
1. Checkout `gh-pages` to your local `font-su` repo.
1. Export font from icomoon. See [Exporting from IcoMoon](#export-from-icomoon)
1. Open downloaded zip file.
1. Rename `demo.html` to `index.html`.
1. Move the newly renamed `index.html` file to the `gh-pages` branch folder.
1. Move `demo-files/demo.css` and `demo-files/demo.js` to the `demo-files` folder in the `gh-pages` branch folder.