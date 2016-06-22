# Emoji Mosaic

Turn an image into a mosaic made of emojis.

[Live site](http://ericandrewlewis.github.io/emoji-mosaic/)

## Figure out the average color value of each Emoji?

What is the source for the Emoji character? Using the actual system character seems exceedingly hard — I don't think I got [node-canvas](https://github.com/Automattic/node-canvas) installed correctly, and even so I don't believe it would render the Apple Emoji system font.

Maybe extract emoji characters from another library? [Gemoji did it](https://github.com/github/gemoji/tree/master/images/emoji/unicode) [The Apple ttf library might be unlicensed](http://stackoverflow.com/questions/22337295/license-of-apple-color-emoji-ttf/22949517#22949517)?

Get a package to [read pngs](https://github.com/niegowski/node-pngjs) and make a lookup table?

Use a prebaked lookup table [like in emojicam](https://github.com/AlexWiles/emojicam/blob/master/emojicam/emoji-colors-jpg.js)?

## How to layout the emoji?

Display emojis as a system font in-browser. www.caniemoji.com for compatability. Using prebaked lookup table, create another mapping from the prebaked lookup table to a table of emoji characters as stored in the system font. This will dynamically display raw text as opposed to png data.
