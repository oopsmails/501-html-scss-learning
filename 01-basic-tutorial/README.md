# HTML and SCSS Learning

- Ref:

https://www.youtube.com/watch?v=D-h8L5hgW-w&list=RDCMUCVyRiMvfUNMA1UPlDPzG5Ow&start_radio=1


- Figma

https://www.figma.com/  

oopsmails@gmail


## Setup

### VS Code

### Plugins

- Live Sass Compiler (Live Server plugin will also be installed along with this)
- Click on the bottom right coner tool bar to enalbe/disable watching

### Run

right click *index.html*, "Open with live server"

### Code Sources

- Codepen demo:
- 
https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbm9keUtHTHdiZkY0OUpLQzBUdXpieF9tTXI0UXxBQ3Jtc0trM2RpbU9KVTRMRExQTWwxczlYUVZsWWVaQ0t1UWMxZmg5U1NKQnRubzlzNG8yUXRDV0Y3ZHRiMjRJZnhWc3QycTJrNDQtNTNJaFdWLWNsVTRGUlV3dUFyLWdoSG1VMlp3cHhneXR5dDJmTDJsRU1Daw&q=https%3A%2F%2Fcodepen.io%2Fdesigncourse%2Fpen%2FJjbPdqd

- Project files:

https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbXNlakhmTXJFY0ZUUlRMWG53SjBvcng0aUlDZ3xBQ3Jtc0ttdUNKZmFrVC1NNkFCVFBtMmtCUmVRZlZobFJfWEVRYjlha2xtVzVtVmxrc0xDVWJNMUU2UVZLV0RmUXl5ZUVibWxoYXNYZGFsc29rS1hZZVZaVjh4ZGZoWUVzS2cwdEtnZWkyRnctNU1Rc1MzTVNnNA&q=https%3A%2F%2Fcoursetro.s3.amazonaws.com%2Fstuff%2F2021frontend.zip

## Knowledge

### Mixins

- Normally, don't use Mixins without arguments.




## References:

- HTML and CSS Tutorial for 2021 - COMPLETE Crash Course!

https://www.youtube.com/watch?v=D-h8L5hgW-w

- 00:58:00: google map
- 00:59:03: starting CSS
- 01:28:16: 

- 01:36:45: &before, :after and :before pseudo-element selectors in Sass  
see https://stackoverflow.com/questions/11084757/sass-scss-nesting-and-multiple-classes  
```
&:before {
            content: '';
            left: -2em;
            position: absolute;
            width: 20px;
            height: 20px;
            background-image: url('../images/bullet.svg');
            background-size: contain;
            margin-right: .5em;
        
```
- 01:38:23: position, absolute and relative

- 01:44:38: another way of selector, could also use class

```
input[type="submit"] {
```

- 01:47:45: z-index, 999, on top of everything ...
- 01:49:15: display: block; why, if we want to put padding or margin, etc., on a href element
- 01:49:45: &:hover ...

- 01:54:54: responsive css design, mobile and web, through *media queries*

- 01:56:29
```
@media only screen and (min-width: 768px) {



```

- 02:03:01: grid ...

```
display: grid;
    grid-template-columns: repeat(auto-fit, minmax(19rem, 1fr));



.navbar .container {
        display: grid;
        grid-template-columns: 180px auto;
        justify-content: unset;
    }

```

- 02:04:36

```
@media only screen and (min-width: 1080px) {


map, example for putting image at right

position: absolute;
right: 0;

```

- 02:13:25: more understanding on *&:before* and *&:after*

```
@media only screen and (min-width: 1450px) {



```


