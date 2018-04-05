# WebDev-Snippets
A place to store useful web dev snippets I use. They aren't in any specific order.



#### Material Design Card (Box Shadow)
```box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);```

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


