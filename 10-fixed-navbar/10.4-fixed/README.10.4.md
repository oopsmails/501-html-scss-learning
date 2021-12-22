
# Create a responsive navigation nav with no JS!

- Ref: 
https://www.youtube.com/watch?v=8QKOaTYvYUA&list=RDCMUCJZv4d5rbIKd4QHMPkcABCw&start_radio=1


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

