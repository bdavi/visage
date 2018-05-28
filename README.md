# visage

*visage* is a small set of CSS utility classes meant for convenience and composability.

It's not meant to replace a full CSS framework or custom CSS. Rather, it provides some ready-to-use basics that are helpful on almost any project.

## Build
*visage* uses Sass and must be compiled into CSS before use in the browser.

There are a number of ways to compile Sass and, depending on the project, your build may already support Sass. If not, the included build script will render *visage* as vanilla CSS using the stand alone `sass` executable  (available [here](https://sass-lang.com/install)).

Build the CSS by running this from the project root:
```
$ bin/build

=> Success
=> The expanded CSS is available here: ./build/visage.css
=> For a minified/production version see: ./dist/visage.min.css
```

When running the build script, you may receive a warning similar to this:
```
-bash: bin/build: Permission denied
```

If so, ensure the build script is executable by running this:
```
$ chmod +x bin/build
```

## Usage
- [Margin and Padding](#margin-and-padding)

### Margin and Padding
Combine a prefix, direction and amount to create a class which specifies margins and padding.


**Prefixes**

Value | Description
----- | -----------
`m` | Margin
`p` | Padding


**Directions**

Value | Description
----- | -----------
*none* | All Directions
`l` | Left
`r` | Right
`t` | Top
`b` | Bottom
`x` | Left & Right
`y` | Top & Bottom


**Amounts**

Value | Description
----- | -----------
`0` to `5` | 0 to 25px in increments of 5px
`-1` to `-5` | -5px to -25px in increments of -5px (Margin Only)
`-auto` | Yields `{ margin: 0 auto; }`. Only `m` prefix.


**Example usage:**
```
<!– { margin-left: -15px; margin-right: -15px; } –>
<div class="mx-3">Hello World</div>

<!– { padding-top: 5px; padding-right: 20px } –>
<div class="pt1 pr4">Hello World</div>
```
