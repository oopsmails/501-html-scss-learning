# Amazing shoes
The code that goes with [this video](https://www.youtube.com/watch?v=X1dz0xRbSJc&)



## Knowledge Summary

### There are whole bunch of *Syntax* to learn in this tutorial!

- 00:20:20 why we have *@supports*
- 00:22:28 why we have *.spacing>\*+\**
- 00:27:35 *&>\**


### Using @function to handle image path, by myself.

```
@function calcImgPath($img) {
  @return "../../11-basic-examples/11.2-modern-landing-page/img/" + $img;
}

background-image:url(calcImgPath('shoe-3.png'));
```

- *@return var(--img-location) + $img;*
  
This is NOT working because var() can only be transpiled at runtime!

- *background-image:url(var(--img-location) + "shoe-2.png");*

This is NOT working because *It is not possible to create a composite url() value out of two or more strings. On top of the legacy url() value, which isn't even a proper CSS function*

Ref:  
https://stackoverflow.com/questions/42932294/css-attr-concatenation-with-url-path

### Using var with different scopes

```
background: radial-gradient(var(--clr-inner, limegreen), var(--clr-outer, purple));

```


## Notes

01:15:25

00:00 - Introduction
01:41 - Start HTML
07:57 - Start CSS
17:57 - Styling the hero
24:54 - Styling the featured section
48:23 - Styling the our products section
54:51 - Using the custom properties we set up
1:02:06 - Using floats and shape-outside
1:14:26 - Outro

### Learning Notes

- 00:11:16 About *display: inline-block;*

Anchors or links are default as *inline*, 
Not to overlaping with text, etc.

- 00:15:44 About *clamp*

font-size: clamp(3rem, calc(5vw + 1rem), 4.5rem);

- 00:19:00 play around *background-size: 10%;*

```
@function calcImgPath($img) {
  @return "../../11-basic-examples/11.2-modern-landing-page/img/" + $img;
}

:root {
  --img-location: "../../11-basic-examples/11.2-modern-landing-page/img/";
}


.hero {
  text-align: center;
  padding: 15em 0;
  // background-image: url(../../11-basic-examples/11.2-modern-landing-page/img/shoe-3.png); // ok
  background-image:url(var(--img-location) + "shoe-2.png"); // Not working! 
  background-image:url(calcImgPath('shoe-3.png'));
  background-size: 10%; // 19:00
}
```

- 00:19:30 Play around *radial-gradient(#444, #111);*


- 00:20:20 why we have *@supports*

```
@supports (background-blend-mode: multiply) {
    ...
}
```

- 00:22:28 why we have *.spacing>\*+\**

So, it is adding style (in this case, margin-top) to those elements who has a siblinng BEFORE it ...

In our case here, this is adding *margin-top* to *<a href ...>* and *<p*, which having sibling before them, but NOT adding to *h1*.

```
-- usage: 

    <div class="container spacing">
      <h1 class="primary-title">Amazing shoes at an amazing price</h1>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa quam perspiciatis facilis beatae laudantium
        quidem enim sit sequi!</p>
      <a href="#" class="btn">See what we have</a>
    </div>


.spacing>*+* {
  margin-top: var(--spacer, 2rem)
}
```


- 00:27:05 *display: flex*

- 00:27:35 *&>\**

> `>*` means all direct children
> `&` means retake this so it's going to pump out


```
.split {
  display: flex;
  gap: 1em;
  flex-wrap: wrap;
  justify-content: center;

  &>* {
    flex-basis: 30%;
    min-width: 15em;
  }
}


-- & is like below

.split {
  display: flex;
  gap: 1em;
  flex-wrap: wrap;
  justify-content: center;
}

.split > * {
    flex-basis: 30%;
    min-width: 15em;
}
```


- 00:33:35 using *&* again

```
.featured {
  background: #eee;

  &__item {
    display: block;
    position: relative; <------------ will use position absolute later ...

-- will compiled into

.featured__item {
  display: block;

```

- 00:33:35 using *&:hover*

```
 &:hover,
    &:focus {

```


- 00:37:15 using Pseudo Element

Pseudo element anytime you have a pseudo element you need to give it content to make it exist

>00:39:03, making blue circles background and moving around it.

```
    &::after {
      content: '';
      position: absolute; <---------------- this is why using *position: relative;* on *&__item*
      top: 10%; <----------------- 00:39:03, making blue circles background and moving around it.
      left: 10%;
      padding: 75% 75% 0 0;
      border-radius: 50%;
      background: #2193b0;
      z-index: -1;
    }
```

- 00:49:18 using *radial-gradient*

try *background: radial-gradient(red, yellow);*

```
background: radial-gradient(var(--clr-inner, limegreen), var(--clr-outer, purple));

```

- 00:51:25, *border-radius: 1em;*

Using *border-radius* to decorate *backgroud* ... like to css buttons.

- 00:54:33, re-using *spacing*

- 00:57:24, variables with *component* scope

```
.hero {
  --clr-accent: #faa700;
}

.shoe-red {
  --clr-inner: #faa700;
  --clr-outer: #e48d00;
  --clr-accent: #a1173c;
}

.shoe-white {
  --clr-inner: #fce4b3;
  --clr-outer: #eac886;
  --clr-accent: #2f4858;
}

.shoe-blue {
  --clr-inner: #6dd5ed;
  --clr-outer: #2193b0;
  --clr-accent: #008951;
}
```



- 01:02:01, using *float: right;* + *width: 65%;*



- 01:04:18, make text go into image "outline", using *shape-outside*

```
outline: 2px solid red;
shape-outside: circle(30%);
```

01:05:01, firefox dev tool, to see and play around the *circle()*

1:05:48  
the thing is you don't have to do a circle you can actually do a url and you want to guess what you're all  

1:05:54  
**going to use the image itself and because it's a png it knows it's transparent**


shape-outside: url(calcImgPath('shoe-1.png'));


- 01:07:36, debugging empty spaces ...


- 01:10:32, separating logic, left and right, *&.shoe-left*

Nesting *.product__image* inside *&.shoe-left*

```
    &.shoe-left {
      .product__image {
        float: left;
        shape-outside: url(calcImgPath('shoe-2.png'));
        margin: 0 0 0 -5em;
        shape-margin: 2em;
      }
    }
```

## Temp:

background-image:url(calcImgPath('shoe-3.png'));







