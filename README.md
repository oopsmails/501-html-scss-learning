# html-css-learning

## VS Code Settings

- Note: even with vscode-live-sass-compiler, when first time pull the repo, may need to change scss files to trigger the compilation, to generate the css files needed.

vscode-live-sass-compiler relative path

- Need to click _Watch Sass_ on the Status Bar at the bottom, make it "Watching ...."

- **Parallax**

Notice how my _liveSassCompile.settings.formats_ is formatted: I've written the save paths as _/Parallax/css/_ and _/Parallax/dist/css_. This goes to the project root and saves the css files inside the folders called css and dist which are inside the Parallax directory. (image link)

In conclusion each time you want to change the save path all you have to do is modify the settings.json file inside the .vscode folder rather than modifying the user settings which is tedious in my opinion.

```
- Sample:

{
"liveSassCompile.settings.formats": [
    {
        "format": "expanded",
        "extensionName": ".css",
        "savePath": "/Parallax/css"
    },
    {
        "extensionName": ".min.css",
        "format": "compressed",
        "savePath": "/Parallax/dist/css"
    }
],

"liveSassCompile.settings.excludeList": [
    "**/node_modules/**",
    ".vscode/**"
],
"liveSassCompile.settings.generateMap": true,
"liveSassCompile.settings.autoprefix": [
    "> 1%",
    "last 2 versions"
]
}
```

- Using 20211225

```
"liveSassCompile.settings.includeItems": [
        // "~/dev/html-scss-learning/css/*.scss",
        "/Parallax/css/*.scss",
        "/Parallax/css/*/*.scss",
        "~/dev/*.scss",
    ]
```

## 20.3, _.main-nav_ example

```
.main-nav
```
