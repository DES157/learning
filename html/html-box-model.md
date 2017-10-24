# Box Model

content
padding
border
margin

## TL;DR

Check the selectors, but you should always do something like this:

    *, *:before, *:after {
        -moz-box-sizing:border-box;
        -webkit-box-sizing:border-box;
        box-sizing:border-box
        }

## Details

### Box Sizing

`border-box` - make width/height include content, border, and padding. So, for example, you can set `width: 100%` and still add padding and border.


!FINISH THIS SOMETIME
