# visage

*visage* is a small set of css utility classes meant for convenience and composability.

It's not meant to replace a full css framework or custom css. Rather, it provides some ready-to-use basics that are helpful on almost any project.

### Build
*visage* uses Sass and must be compiled into css before use in the browser.

There are a number of ways to compile Sass and, depending on the project, your build may already support Sass. If not, the included build script will render *visage* as vanilla css using the stand alone `sass` executable  (available [here](https://sass-lang.com/install)).

Build the css by running this from the project root:
```
$ bin/build

=> Success
=> The expanded css is available here: ./build/visage.css
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
