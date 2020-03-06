# Instructions

The source files for **light** and **dark** mode CSS themes are located in this directory. Any modification of either theme requires regeneration of CSS files. The Bulma website can always be referenced for proper [instructions](https://bulma.io/documentation/customize/with-node-sass/).

Ensure that `npm` is installed.

Run the following command to generate CSS files.

```shell
npm run css-build
```

The resulting CSS files are written to the `../css` directory.

In some cases, an error similar to the following may occur while running the CSS build command.

```shell
Error: Node Sass does not yet support your current environment: OS X 64-bit with Unsupported runtime (79)
```

When this happens, run the following command to rebuild `node-sass`, and then try rebuilding the CSS.

```shell
npm rebuild node-sass
```
