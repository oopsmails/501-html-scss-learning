# Microsoft Homepage Clone

A Pen created on CodePen.io. Original URL: [https://codepen.io/bradtraversy/pen/ZEGGNRb](https://codepen.io/bradtraversy/pen/ZEGGNRb).


https://www.youtube.com/watch?v=uKgn-To1C4Q&list=RDCMUC29ju8bIPH5as8OGnQzwJyA&index=8

## Knowledge Summary

### Arrange Nav Bar

08:34 *display: flex*
## Notes

- 08:34 *display: flex*

- 16:02 hover, lightening button color 

```
.btn:hover {
  opacity: 0.9;
}
```

- 16:22 Showcase: arrange around

```
.showcase {
  width: 100%;
  height: 400px;
  background: url('https://i.ibb.co/zGSDGCL/slide1.png') no-repeat center center/cover; <------------------ background image!!!
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  justify-content: flex-end; <---------------- push down!!!
  padding-bottom: 50px;
  margin-bottom: 20px;
}

```


- 22:36 Home cards: grid

```
/* Home cards */
.home-cards {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 20px;
  margin-bottom: 40px;
}
```

it's kind of going off the page here is because of the images **images are always**
24:11
**going to go out of their container unless we set the width** to be restricted
24:17
to be a hundred percent of the container

- 27:05 chevron: push out/right when hover

```
.home-cards a:hover i {
  margin-left: 10px;
}
```

- 29:06 Xbox:

......................


- 39:40 Space between items in "Follow" section

Using *, asterisk

we need some spacing in between all this so what I'm gonna do
39:42
is take the follow class and say everything within it so we'll use an asterisk asterisk care and just give it
39:48
a margin right of let's do 10 pixels save and now it's going to space this
39:55
stuff out for us

```
.follow * {
  margin-right: 10px;
}
```


- 45:27 Align in the middle

```
.links-inner {
  max-width: 1100px;
  margin: 0 auto; <---------------- align in the middle
  padding: 0 20px;
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-gap: 10px;
  align-items: flex-start;
  justify-content: center;
}
```

- 49:46 *flex-wrap: wrap;*

when this gets
49:48
smaller I actually want it to wrap I want these to go on top of each other so
49:54
we can use a property called flex wrap and set that to wrap and save and now
50:01
they'll just kind of go on top of each other and they don't go out of the screen it doesn't look great but I mean
50:08
it's it's you can see see all the links and it doesn't go off the screen


```
.footer ul {
  display: flex;
  flex-wrap: wrap;
}
```

- 51:09 Footer not align properly

Need to make it same as *.footer ul*

```
.footer div {
  margin-bottom: 20px;
  display: flex; <--------------------- 
  align-items: center; <----------------------
}
```

- 58:22 Hamberger button:

```
  <div class="menu-btn">
    <i class="fas fa-bars fa-2x"></i>
  </div>
```

- 01:03:05 take out space left

transform: translateX(-500px);

```
  .main-nav ul.main-menu {
    display: block;
    position: absolute;
    top:0;
    left: 0;
    background: #f2f2f2;
    width: 50%;
    height: 100%;
    border-right: #ccc 1px solid;
    opacity: 0.9;
    padding: 30px;
    transform: translateX(-500px); <---------------- 
    transition: transform 0.5s ease-in-out;
  }


  .main-nav ul.main-menu.show {
    transform: translateX(-20px);
  }
```

- 01:06:21  pseudo selector:

1:06:17
we can use a pseudo selector of last child which is just going to take the


```
  .main-nav ul.main-menu li:last-child {
    border-bottom: 0;
  }
```

- 16:22 Showcase:
- 16:22 Showcase:














