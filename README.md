# WebDev-Snippets
A place to store useful web dev snippets I use. They aren't in any specific order.



#### Material Design Card (Box Shadow)
```box-shadow: rgba(0, 0, 0, 0.19) 0px 2.5px 5px 0px, rgba(0, 0, 0, 0.23) -2px 1px 6px 0px;```

#### Flex Box Boostrap-esque Grid/Columns

###### HTML
```
<div class="grid">
    <div class="col"></div>
    <div class="col"></div>
    <div class="col"></div>
</div>
```

###### CSS
```
.grid
{
  display: flex;
}

/*Equal Width Columns*/
.col
{
  flex: 1;
}

/*Differing widths, where the number is the amount of the times bigger than the
other columns in the grid*/
.col-2
{
  flex: 2;
}
.col-3
{
  flex: 3; 
}


/*Reset the columns into a single column for a smaller screen size. 
(400px abritrary breakpoint)*/
@media (max-width: 400px)
{
  .grid
  {
    display: block;
  }
}
```

#### CSS Gradients

```
/* fallback for old browsers */
background: FIRST_COLOUR;  

/* Chrome 10-25, Safari 5.1-6 */
background: -webkit-linear-gradient(to right/left, FIRST_COLOUR, SECOND_COLOUR);

/* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
background: linear-gradient(to right/left, FIRST_COLOUR, SECOND_COLOUR); 
```

#### Make a DIV fill the entire page

```
html,
body {
    height: 100%;
    margin: 0;
}

.fullpage-div {
    min-height: 100%;
}
```

#### ^ Achieve the same but on a React App that is using CSS Modules
Add The following to the public/index.html file
```
<style>
    html,
    body {
      height: 100%;
      margin: 0;
      padding: 0;
    }

    #root {
      display: flex;
      min-height: 100%;
      max-width: 100%;
    }
  </style>
```
and then set
```
.App
{
    width: 100%;
}
```
where App is the className applied to the container that holds all other components at the highest level.

#### Get all elements matching a class containing a set pattern

eg: Get all classes that have a class on them such as link-0, link-1, link-2 etc by checking for link- 

```
let classes = document.querySelectorAll('[class*= "link-"]');
```


#### Center a position:fixed; element

```
.element
{
    top: 50%;
    left: 50%;
    
    margin-left: -HALF_WIDTH;
    margin-top: -HALF_HEIGHT;
}
```

#### Ensure text in a flexbox wraps in IE
Explicitly set the width of both the parent flex box and the element holding the text that needs to wrap

```
.box
{
    display: flex;
    width: 100%;
}

.box > p
{
    width: 100%;
}
```

#### Position an element fixed but relative to its parent
Ensure the parent element is positioned as anything but ```static``` and then:

```
.parent
{
    position: relative;
}
.child
{
    position: absolute;
}
```

