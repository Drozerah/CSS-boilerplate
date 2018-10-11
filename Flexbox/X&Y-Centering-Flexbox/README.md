# CSS Horizontal and Vertical Centering - Flexbox

This CSS code helps in centering a flex item vertically and horizontally. 

Note : this code allow to fix an issue in the case that the flex-item is bigger than the flex-container. Indeed, when the flex-item overflows the flex-container the top becomes inaccessible for the viewport... To correctly solve that problem we can apply the Flexbox [auto margins](https://stackoverflow.com/questions/32551291/in-css-flexbox-why-are-there-no-justify-items-and-justify-self-properties/33856609#33856609) onto the flex-item like so :

````
.flex-container {
    height: height: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
}
.flex-item {
    margin: auto;
}
````
In addition we must give first to both the html & body tags a height : 

````
html, body{
    height: 100%;
}
````
otherwise there will be no vertical centering because of height reference lack...
