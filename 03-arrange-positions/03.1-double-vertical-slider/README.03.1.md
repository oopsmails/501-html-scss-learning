
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

- 21:33, 

```

.slider-container {
  position: relative; <-------------- set as "relative"!!! because will set everything inside it as "absolute"
  overflow: hidden;
  width: 100vw; <------------------- take whole width
  height: 100vh;
}

.left-slide {
  height: 100%;
  width: 35%;
  position: absolute; <-------------------- using "absolute"
  top: 0;
  left: 0;
  transition: transform 0.5s ease-in-out;
}

```

- 22:41, moving around for immidiate div

```
.left-slide > div {
  height: 100%;
  width: 100%;
  display: flex;  <-------------------- 
  flex-direction: column;  <-------------------- 
  align-items: center;  <-------------------- 
  justify-content: center;  <-------------------- 
  color: #fff;
}
```

- 27:23, separate button up and down 

```
.slider-container .action-buttons button {
  position: absolute;
  left: 35%;
  top: 50%;
  z-index: 100;
}

.slider-container .action-buttons .down-button {
  transform: translateX(-100%); <------------------- Using "translateX" to move horizontally!!!
  border-top-left-radius: 5px;
  border-bottom-left-radius: 5px;
}

.slider-container .action-buttons .up-button {
  transform: translateY(-100%); <------------------- Using "translateY" to move vertically!!!
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
}

```






