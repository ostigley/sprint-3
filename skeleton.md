#What happens to the layout when you resize the screen to less than 550 px. 
The most noticeable effects are: 
* The skeleton column system collapses such that each column, or set of columns has it's own line.  There is not more than one div of columns on the same line. 
*The width of the containers decreases, and white space is used to show content, as space becomes limited. 

#How do you think that works? 
This is achieved using a media query for above 550px, which sets the width to the relevant % of the page width (12 base):
```
    @media (min-width: 550px)
    .ten.columns {
        width: 82.6666666667%;
    }
```
Below this 550px screen size, the following column width is used, changing the WIDTH of the column to the entire width of the parent div.
```
    .column, .columns {
        width: 100%;
        float: left;
        box-sizing: border-box;
    }
```
