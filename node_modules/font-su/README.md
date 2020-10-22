# Font SU
Starchup's custom icon font family for garments and things.

- :tv: **[Click here to see a full explainer video](https://youtu.be/drEyugXElqA)** on how to update the font family with a new icon.
- :books: **[Click here to see full documentation](https://starchup.github.io/font-su/)** of the font-su icons in action.

## Create / Update Icon (svg)
> **Note:** This requires some editor tool like Adobe Illustrator/Photoshop or Affinity Desiger.

1. If you're editing, open an existing `svg` in your editor tool.
1. If you're creatinga new icon, open the `_template.svg` from the [`svgs`](https://github.com/Starchup/font-su/tree/master/svgs) folder in your editor tool.
1. Create the new icon (or import a purchased svg) or make your edits (see notes)
1. To export (these are specific to Affinity Designer), do the following:
    1. Click `File > Export`
    1. Select `SVG`
    1. Preset: SVG (digital - high quality)
    1. Raster DPI: 300
    1. Export text as curves for font independence: unchecked
    1. Area: Whole document
    1. Don't export layers hidden by Export persona: unchecked
    1. Click "Export"
    1. Export to the `svgs` folder in your local `font-su` repo (see notes)

**Notes:**
1. When editing / creating new icon.. make sure, if you used "stroke" or the purchased icon came with "stroke", to select `Layer > Expand Stroke`. Strokes will not be picked up when exporting font files from IcoMoon. Also, make sure to combine all layers/elements into some simple layer (In Affinity Designer, click "Add" icon in top right while all layers are selected)
1. When exporting a new icon, be sure to choose a name for the icon that will also be used for the css selector for the icon. The name should also be generic as we can choose the label/alt names within our codebase. For the font, the more generic the better. Also, make sure to check for class names that already exist. For example, if you're exporting a `shirt` there are likely more `shirt` icons, so you might have to make yours `shirt-2`.

## Import `font-su` project to IcoMoon
> IcoMoon only stores projects in an individual browser's cache and supplies a [`selection.json`](https://github.com/Starchup/font-su/blob/master/selection.json) file to upload as a project in order to edit. Projects aren't tied to "accounts" they're tied to a browser, so we'll need to upload the most recent `selection.json` each time we want to edit to ensure we're editing the most recent version of our font.

1. Import `selection.json` to the IcoMoon app using the `Import Icons` button.
1. Follow the steps below to [Import new / updated icon to IcoMoon](https://github.com/Starchup/font-su/blob/master/README.md#import-new--updated-icon-to-icomoon)

## Import new / updated icon to IcoMoon
1. After you [Create / Update Icon (svg)](https://github.com/Starchup/font-su/blob/master/README.md#create--update-icon-svg), drag and drop it the `font-su` project under the appropriate section (or create a new section) - _note this isn't extremely important, just a way to keep separation of icon origin within IcoMoon._

## Export from IcoMoon
1.

## Update font-su repo
Any time we update `font-su`, we should update both the font family repo AND the documentation.

1. Clone this repo and checkout the `master` branch.
1. Export font from icomoon. See [Exporting from IcoMoon](#export-from-icomoon) for export details.
1. Open downloaded zip files.
1. Follow the instructions below to update the font family and documentation

#### Update font family
1. Move `styles.scss` and `variables.scss` to the `/scss` folder.
1. Open `styles.scss` and update `$icomoon-font-path: "fonts" !default;` to `$icomoon-font-path: "../fonts" !default;`
1. Move `style.css` to the `/css` folder.
1. Open `styles.css` and update font urls from `fonts/` to `../fonts/` (ex: update `fonts/font-su.eot` to `../fonts/font-su.eot`)
1. Go to [CSS Minifier](https://cssminifier.com/). Copy/paste the code from `style.css`, click "Minify", copy minified code to clipboard, and replace the code in `css/style.min.css`
1. Update package.json with latest version.
1. Push changes to `master`

#### Update documentation
1. Visit [README.md in `gh-pages` branch](https://github.com/Starchup/font-su/tree/gh-pages) to update documentation.