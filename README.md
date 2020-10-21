## Import font-su to IcoMoon (in order to update)
1. Import `selection.json` to the IcoMoon app using the `Import Icons` button.

## Export from IcoMoon
1.

## Update font-su repo
1. Clone this repo and checkout the `master` branch.
1. Export font from icomoon. See [Exporting from IcoMoon](#export-from-icomoon) for export details.
1. Open downloaded zip files.
1. Move `styles.scss` and `variables.scss` to the `/scss` folder.
1. Open `styles.scss` and update `$icomoon-font-path: "fonts" !default;` to `$icomoon-font-path: "../fonts" !default;`
1. Move `style.css` to the `/css` folder.
1. Open `styles.css` and update font urls from `fonts/` to `../fonts/` (ex: update `fonts/font-su.eot` to `../fonts/font-su.eot`)
1. Go to [CSS Minifier](https://cssminifier.com/). Copy/paste the code from `style.css`, click "Minify", copy minified code to clipboard, and replace the code in `css/style.min.css`
1. Update package.json with latest version (should version set in IcoMoon that is stored in `selection.json`)

## Update `font-su` documentation
Visit the [Github Pages README.md](https://github.com/Starchup/font-su/edit/gh-pages/README.md) for this repo.
