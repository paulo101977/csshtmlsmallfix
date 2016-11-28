# CSS HTML Small fix tutorial

## 1 - how Fix div size in small screens/mobile

The fix is in stackoverflow link:

http://stackoverflow.com/questions/18588835/allow-a-div-to-cover-the-whole-page-instead-of-the-area-within-the-container

**Step:**

change the position absolute of the div for "fixed"

**Example:**

```
.custom-div-full-screen-mobile-small-size
{
    position:fixed;
    padding:0;
    margin:0;

    top:0;
    left:0;

    width: 100%;
    height: 100%;
    background:rgba(255,255,255,0.5);
}
```

### 2 - How Fix div vertical align (too work in bootstrap)

**Step:**

The fix is in stackoverflow link:
http://stackoverflow.com/questions/20547819/vertical-align-with-bootstrap-3

put the class in both div to align:

```
.inline{
    display: flex;
    align-items: center;
}
```
### 3 - Horizontal align div (too work in bootstrap)

**Step:**

The fix is in stackoverflow link:
http://stackoverflow.com/questions/7745232/align-images-to-right-in-a-div

put the class in both div to align:

```
.item{
    width : 100%;
    float:right;
    clear:right;
}
```

### 4 - Perfect align div vertical (too work in bootstrap)

**Step:**

The fix is link:
https://scotch.io/tutorials/a-visual-guide-to-css3-flexbox-properties

put the class in both div to align:

```
.start, .telephone{
    display: flex;
    -webkit-flex-direction: column; /* Safari */
    flex-direction:         column;
    flex-wrap: nowrap;
    text-align: left;
    justify-content: center;
}
```

### 5 - Prevent two scroll propagate

**Step:**

The fix is link:
http://stackoverflow.com/questions/5802467/prevent-scrolling-of-parent-element


### 6 - Scroll horizontal and vertical with wheel

this use the jquery.mousewheel.min.js:

https://css-tricks.com/snippets/jquery/horz-scroll-with-mouse-wheel/
