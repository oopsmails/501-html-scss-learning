
# Creative Agency Website

- Ref: Thanks!

> Simple HTML/CSS website from the [YouTube tutorial project]
 
(https://www.youtube.com/watch?v=lvYnfMOUOJY&t=274s)
![Creative Agency](/images/screenshot.png 'Creative Agency')
[LIVE PREVIEW](https://raw.githack.com/bradtraversy/creative-agency-website/master/index.html)

https://github.com/bradtraversy/creative-agency-website


## Notes: index.html

### 09:03 of 1:26:50: Start of style.ss

```
@import url('https://fonts.googleapis.com/css?family=Poppins:200,300,400,500,600,700,800,900&display=swap');

:root {
  --primary-color: #f60f20;
  --secondary-color: #1b206e;
}

/* BASE STYLES */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html,
body {
  font-family: 'Poppins', sans-serif;
  color: #111;
}
```

### 10:24: logo

```
.logo {
  position: absolute; <--------------------------------- absolute here
  top: 30px;
  left: 100px;
  font-size: 2rem;
  font-weight: 700;
  z-index: 20; <--------------------------------- still showing after toggling main menu
}
```

### 12:57: section

two direct children/elements, img and div


### 13:13: home image

right side, strech from top to bottom

```
.home-img {
  position: absolute;
  bottom: 0;
  right: 0; <--------------------------------- push it to right side when using position: absolute
  height: 110%;
}
```


### 14:40: section flex

```
section {
  display: flex; <--------------------------------- flex box
  flex-direction: column; <--------------------------------- added at 44:20, for service page and add section.home for home page
  height: 100vh; <--------------------------------- viewport height
  align-items: center; <--------------------------------- text in center
  padding: 100px;
  margin-top: 60px;
}

section.home {
  flex-direction: row; <--------------------------------- to separate and specify in each page
  margin-top: 0; <--------------------------------- at 45:00, to separate and specify in each page
}
```

### 15:35: home content z-index higher than image

```
.home-content {
  position: relative; <--------------------------------- ??
  z-index: 10;
  max-width: 600px; <--------------------------------- width
}
```

### 19:06: talk about rem and em


### 19:24: button generic

```
.btn {
  cursor: pointer;
  display: inline-block;
  background: var(--primary-color);
  color: #fff;
  text-decoration: none;
  padding: 10px 30px;
  margin: 20px 0;
  border: 0;
}

.btn:hover {
  transform: scale(0.98);
}
```



### 22:04: toggle

```
.toggle {
  position: fixed; <--------------------------------- fixed to make it stay there! similar to nav-bar
  top: 0;
  right: 0;
  width: 60px;
  height: 60px;
  background: var(--primary-color) url(../images/menu.png); <--------------------------------- background, url, img
  background-size: 30px;
  background-position: center;
  background-repeat: no-repeat;
  z-index: 20;
  cursor: pointer;
}

.toggle.active {
  background: var(--primary-color) url(../images/close.png);
  background-size: 25px;
  background-position: center;
  background-repeat: no-repeat;
}
```



### 25:50: toggle active

### 26:52: navigation, show on entire screen

```
.navigation {
  position: fixed; <--------------------------------- fixed again here
  top: 0;
  left: 100%; <--------------------------------- push back
  width: 100%;
  height: 100%;
  background-color: #fff;
  z-index: 15;
  display: flex;
  justify-content: center;
  align-items: center;
}

.navigation.active {
  left: 0; <--------------------------------- push away
}

.navigation ul {
  position: relative; <--------------------------------- according to use justify-content and align-items
}

.navigation ul li {
  position: relative; <--------------------------------- according to use justify-content and align-items
  list-style: none;
  text-align: center;
}

.navigation ul li a {
  font-size: 2.2rem;
  color: #111;
  text-decoration: none;
  font-weight: 300;
}

.navigation ul li a:hover {
  color: var(--primary-color);
}

```

### 31:50: move social-bar and email imgs to left

```
.navigation .social-bar {
  position: absolute; <--------------------------------- absolute to make it stay lefe: 0
  top: 0;
  left: 0;
  width: 60px;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.navigation .social-bar a {
  display: inline-block; <--------------------------------- Compared to display: inline , the major difference is that display: inline-block allows to set a width and height on the element.
  transform: scale(0.5);
}

.navigation .email-icon {
  position: absolute; <--------------------------------- absolute to make it stay bottom: 20px
  bottom: 20px;
  transform: scale(0.5);
}

```
### 34:03: javascript

```
const toggle = document.querySelector('.toggle') <--------------------------------- querySelector
const navigation = document.querySelector('.navigation')

toggle.addEventListener('click', () => {
  toggle.classList.toggle('active')
  navigation.classList.toggle('active') <--------------------------------- .toggle
})
```
### 38:12: media query

```
@media (max-width: 1068px)
```

## Notes: services.html, using grid

### 41:03: start html

### 47:08: .services

```
.services {
  margin-top: 40px;
  display: grid; <--------------------------------- grid
  grid-template-columns: repeat(3, 1fr); <--------------------------------- layout: grid-template-columns
  gap: 40px;
  text-align: center;
}

.services .service {
  padding: 30px;
}

.services .service:hover {
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1); <--------------------------------- make it like card !!!
}
```


### 52:08: media grid changing responsively

```
grid-template-columns: repeat(2, 1fr);

grid-template-columns: 1fr;
```

## Notes: work.html, using flex box

### 53:36: Start of work.html

### 56:43: flex

```
.portfolio {
  display: flex; <--------------------------------- make all items in a row
  flex-wrap: wrap; <--------------------------------- wrap if overflow
  justify-content: center;
  margin-top: 20px;
}

.portfolio .item {
  position: relative; <--------------------------------- !!! 57:49, why this is relative, because we want do hover "Launch" button, that will be position: absolute within THIS item !!!
  width: 300px;
  height: 300px;
  margin: 5px;
}

.portfolio .item img {
  width: 100%; <--------------------------------- make img occupy 300px defined above
  height: 100%;
}
```


### 59:01: hover action "Launch" button

```
.portfolio .item .action {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0; <--------------------------------- default NOT there !!!
  transition: 0.5s; <--------------------------------- add transition, fade-in as default
}

.portfolio .item:hover .action { <--------------------------------- hover
  opacity: 1; <--------------------------------- show button
}

.portfolio .item .action a {
  display: inline-block; <--------------------------------- inline-block
  color: #fff;
  text-decoration: none;
  border: 1px solid #fff;
  padding: 5px 15px;
}

```



## Notes: contact.html, using flex box

### 01:04:00: start of contact.html

### 01:11:06: flex

```
.contact {
  position: relative;
  width: 100%;
  margin-top: 50px;
  display: flex;
  justify-content: space-between;  <--------------------------------- space-between
  align-items: flex-start;
}
```

### 01:12:44: calc

```
.contact-form {
  position: relative;
  background: #f9f9f9;
  width: calc(100% - 400px); <--------------------------------- calc(100% - 400px), use 100% but take away 400px
  padding: 60px 40px 20px;
}

```

### 01:13:15: 100% across

```
.contact-form form {
  width: 100%; <--------------------------------- 100% across
}

.contact-form .row {
  width: 100%; <--------------------------------- 100% across
  display: flex; <--------------------------------- input side by side ...
}

.contact-form .input50 {
  width: 50%;
  margin: 0 10px;
}

.contact-form .input100 {
  width: 100%;
  margin: 0 10px;
}

.contact-form .row input,
.contact-form .row textarea {
  position: relative;
  border: 1px solid rgba(0, 0, 0, 0.2); <--------------------------------- input border
  color: #111;
  background: transparent;
  width: 100%;
  padding: 10px;
  outline: none;
  font-size: 16px;
  font-weight: 300;
  margin: 10px 0;
  resize: none;
}
```

### 01:17:55: targeting input

```
.contact-form .row input[type='submit'] { <--------------------------------- targeting input
  background-color: var(--secondary-color);
  color: #fff;
  margin: 0;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-weight: 300;
  border: 0;
  cursor: pointer;
}

```

### 01:19:45: flex, info-box

```
.contact-info .info-box {
  display: flex; <--------------------------------- flex
  align-items: flex-start;
  margin-bottom: 40px;
}
```

### 01:20:40: resize icons

```
.contact-info .info-box .contact-icon {
  width: 20px;
  margin-right: 40px;
}
```
### 01:24:31: flex-direction

```
.contact-form .row {
    flex-direction: column;
}


.contact-form .input50,
.contact-form .input100 {
    width: 100%;
    margin: 0;
}
```

