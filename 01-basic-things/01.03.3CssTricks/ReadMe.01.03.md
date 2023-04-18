# Easier layouts with these 3 Grid tips

https://www.youtube.com/watch?v=z2kuC7w9emE

https://codepen.io/kevinpowell/pen/wvypKOg

## SCSS not compile

compare 501-html-scss-learning\css\01\01.03\index.01.03.scss with 501-html-scss-learning\css\01\01.03\index.01.03.orig.scss

## Important

> minmax(min(300px, 100%), 1fr));

```
grid-template-columns: repeat(auto-fit, minmax(min(300px, 100%), 1fr));
```

> grid-auto-flow + grid-auto-columns

```
@media (min-width: 50em) {
    .grid-auto-flow {
        grid-auto-flow: column;
        grid-auto-columns: 1fr;
    }
}
```

> width: min(100% - 2rem, var(--max-width));

```
.container {
    --max-width: 75rem;
    width: min(100% - 2rem, var(--max-width));
    margin-inline: auto;
}
```
