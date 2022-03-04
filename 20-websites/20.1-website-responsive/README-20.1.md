# Responsive Website

## Ref: Lokuri Website

> https://github.com/bradtraversy/loruki-website

> https://www.youtube.com/watch?v=p0bGHP-PXD4

> Fake cloud hosting website used in this [YouTube tutorial](https://www.youtube.com/watch?v=p0bGHP-PXD4)

> Fake cloud hosting website [Live Preview](https://zen-carson-c10c9f.netlify.app)


## Notes:

- 06:26 of 2:02:21

Add Fonts from Google

- 07:14

Basic

```
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

body {
  font-family: 'Lato', sans-serif;
  color: #333;
  line-height: 1.6;
}

.container { <---------------- TBD
  max-width: 1100px;
  margin: 0 auto;
  overflow: auto;
  padding: 0 40px;
}

```

- 08:00

Build nav bar

- 12:05

```
.flex {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
}
```

- 13:48

justify-content: space-between;

- 14:35

```
.navbar ul {
  display: flex; <------------ this makes ul from verical to horizontal !!!
}
```

- 15:18

hover

```
.navbar a:hover {
  border-bottom: 2px #fff solid;
}
```

- 21:20

Variables

```
:root {
  --primary-color: #047aed;
....
}
```

- 22:22

```
.showcase {
  height: 400px;
  background-color: var(--primary-color);
  color: #fff;
  position: relative; <--------------- make this relative so that we could use *position: absolute* inside this !!!
}

```

- 23:15 of 2:02:21

```
- defined in utilities.css

.grid {
  display: grid; <---------------- similar to flex, not automatically, need use with "grid-template-columns"
  grid-template-columns: repeat(2, 1fr); <------------- this is same as grid-template-columns: 1fr, 1fr; repeat(2, 1fr) means repeat twice, 1fr ... can use px or percentage directly but not good practice, use fr always
  gap: 20px; <-------------- gap between
  justify-content: center;
  align-items: center;
  height: 100%;
}

- overriden in style.css
.showcase .grid {
  overflow: visible; <----------------- for card overflow 30:13
  grid-template-columns: 55% auto;
  gap: 30px;
}

```

- 31:40

```
.showcase-form input[type='text'],
.showcase-form input[type='email'] {
  border: 0;
  border-bottom: 1px solid #b4becb;
  width: 100%;
  padding: 3px;
  font-size: 16px;
}

```

- 33:08

```
.showcase-form input:focus {
  outline: none; <-------------- get rid of the outline box when having focus
}
```

- 35:20

```
.btn:hover {
  transform: scale(0.98);
}

```

- 36:45 

```
.showcase::before, <---------------------- 
.showcase::after {
  content: '';
  position: absolute;
  height: 100px;
  bottom: -70px;
  right: 0;
  left: 0;
  background: #fff;
  transform: skewY(-3deg); <---------------------- 
  -webkit-transform: skewY(-3deg);
  -moz-transform: skewY(-3deg);
  -ms-transform: skewY(-3deg);
}

```

- 45:45

Separate out utilities.css, *link* it in *index.html*, before the *link* of *style.css*

- 51:40

Manipulate text, wrap, center ...

```
.stats-heading {
  max-width: 500px; <--------------- wrapping by max-width
  margin: auto; <--------------- center it by margin ??? interesting .....
}
```

- 54:18

organize grid, columns and rows ....

```
/* Cli */
.cli .grid {
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
}

.cli .grid > *:first-child { <--------------- first-child
  grid-column: 1 / span 2;
  grid-row: 1 / span 2;
}

/* Cloud */
.cloud .grid {
  grid-template-columns: 4fr 3fr;
}

```

- 01:08:05

flex, not for media, but just more responsive even for web

```
.languages .flex {
  flex-wrap: wrap; <------------------- flex here
}

.languages .card {
  text-align: center;
  margin: 18px 10px 40px;
  transition: transform 0.2s ease-in; <--------------- see 01:09:35, to make animation moving up smoother
}

```

- 01:09:10

cards hover, animation, move up a little bit

```
.languages .card:hover {
  transform: translateY(-15px); <--------------- to make animation smoother, with transition on .languages .card
}
```

- 01:13:09

organize in utilities.css, grouping ...


- 01:14:39

Media queries start

```
/* Tablets and under */
@media (max-width: 768px)


/* Mobile */
@media (max-width: 500px)
```

- 01:17:25

make grid one column, together here!

```
.grid,
  .showcase .grid,
  .stats .grid,
  .cli .grid,
  .cloud .grid,
  .features-main .grid,
  .docs-main .grid {
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
  }

```

- 01:19:44

justify-self vs justify-content

justify-self: put on an item inside flex box containter or grid containter, to justify just that item

justify-content: put on either a flex box containter or grid containter and justify all elements inside

```
  .showcase-form {
    justify-self: center; <--------------- 
    margin: auto;
    animation: slideInFromBottom 1s ease-in;
  }
```

- 01:21:50

feather.html


- 01:24:44

img is too big, 

```
.features-head img,
.docs-head img {
  width: 200px;
  justify-self: flex-end;
}

```

- 01:29:42

Go to *<i>* tag ..., selector

icon tag ...

`<i class="fas fa-band-aid"></i>`

```
.features-main .card > i { <----------------- Go to html tag
  margin-right: 20px;
}
```

- 01:32:05

*first-child* and *nth-child(2)*

```
.features-main .grid > *:first-child {
  grid-column: 1 / span 3;
}

.features-main .grid > *:nth-child(2) {
  grid-column: 1 / span 2;
}
```

- 01:32:05 Docs page

- 01:38:51

*<pre><code>* <------------------- code tag usage

```
<h3>Install</h3>
<p>Mac (Homebrew)</p>
<pre><code>$ brew install loruki-cli</code></pre>
<p>NPM</p>
<pre><code>$ npm install loruki-cli</code></pre>
<p>Yarn</p>
<pre><code>$ yarn install loruki-cli</code></pre>

```


- 01:41:07

```
.docs-main .grid {
  grid-template-columns: 1fr 2fr;
  align-items: flex-start; <------------------ align to top
}
```


- 01:52:06

Animations: using *@keyframes*

```
@keyframes slideInFromLeft {
  0% {
    transform: translateX(-100%);
  }

  100% {
    transform: translateX(0);
  }
}
```


- 01:54:21

Apply animation

```
.showcase-text {
  animation: slideInFromLeft 1s ease-in;
}

animation: slideInFromRight 1s ease-in;

animation: slideInFromBottom 1s ease-in;
```

- 01:56:53

Deploy to netlify, to explor!


