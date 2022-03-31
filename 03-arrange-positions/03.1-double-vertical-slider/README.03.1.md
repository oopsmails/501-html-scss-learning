
# Build 5 Projects With HTML, CSS & JavaScript

- Ref: 

https://www.youtube.com/watch?v=JkeyKeK3V24&list=RDCMUC29ju8bIPH5as8OGnQzwJyA&start_radio=1

https://github.com/bradtraversy/50projects50days

Timestamps:
0:00 - Intro
2:23 - Project 1 - Blurry Loading
15:31 - Project 2 - Vertical Slider <--------------------------------- here, see position moving around
41:23 - Project 3 - Random Choice Picker
1:01:44 - Project 4 - Live User Filter
1:28:50 - Project 5 - Content Placeholder


## Tracking

- 13:48, Making checkbox to toggle nav

pseudo class, hover
tidle, ~, looking for the **preceeding** sibling *nav* to the *nav-toggle*, doesn't have to **immidiatly after**.

In here, the location of *<checkbox>*, is right before the *<nav>*, it is clearer.

```
.nav-toggle:checked~nav {
    display: block;
}

```

- 18:07, the *for* of *label* is looking for an **id**, not a **class**. Normally, use **id** in html and use **class* in CSS.

- 19:13, it is easier to keep *<span>X</span>*, to keep track moving around.

- 20211222: paused at 19:45
- 20211223: paused at 23:53, transition ...

```
transform: scale(size, smoosh);

- nav
transform: scale(1, 0);
transition: transform 250ms ease-in-out;

```
- 27:08

we can make the links fade in as the scaling finishes though so instead of squishing like this the link sort of appear into the navigation so remember the four properties that I can do there's **scale translate rotate and opacity** so we're allowed to do our opacity.

```
.nav {
    ...
    opacity: 0;
}

.nav-toggle:checked ~ nav a {
    opacity: 1;
}

- transition: on-what, duration, mode, delay-to-begin
transition: opacity 250ms ease-in-out 250ms;

```

- 31:20 - styling it for large screens

fr, fraction unit

- 35:55: *all: unset* not working for Edge

- 39:00 - adding the pseudo elements

```


```

