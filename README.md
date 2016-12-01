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

### 7 - Jquery how add !important to css

Fix: 

```
$("#tabs").css("cssText", "height: 650px !important;");
```

Stackoverflow: http://stackoverflow.com/questions/1986182/how-to-include-important-in-jquery

### 8 - Center img verticaly and float 

Fix:

```
/* help center float content */
.img_container_help{
    height: 100%;
    text-align: right;
    margin-left: auto;
    float: right;
    clear: right;
}
```

### 9 - Center with display table

Link: http://vanseodesign.com/css/vertical-centering/

```
<div id="parent">
    <div id="child">Content here</div>
</div>

css
#parent {display: table;}

#child {
    display: table-cell;
    vertical-align: middle;
}

and other method:

html
<div id="parent">
    <div id="child">Content here</div>
</div>
css

#parent {position: relative;}

#child {
    position: absolute;
    top: 50%;
    left: 50%;
    height: 30%;
    width: 50%;
    margin: -15% 0 0 -25%;
}
```

### 10 - Jquery drag page
https://codepen.io/JTParrett/pen/uzGvy

### 11 - Jquery mobile tap and other events
http://www.w3schools.com/jquerymobile/jquerymobile_events_touch.asp

### 12 - Test if is mobile Device

Credits: http://stackoverflow.com/questions/3514784/what-is-the-best-way-to-detect-a-mobile-device-in-jquery

```
    if( /Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent) ) {
     // some code..
    }
```
 ### 13 - Polyfill to mobile swipe
 
 font: http://stackoverflow.com/questions/2264072/detect-a-finger-swipe-through-javascript-on-the-iphone-and-android
 
 ```
 /* test swipe event in android and other mobile devices */
$(getStringQueryToSwipe()).on('touchstart', function(evt){
    xDown = evt.originalEvent.touches[0].pageX;                                    
    yDown = evt.originalEvent.touches[0].pageY;
})  

//document.addEventListener('touchmove', function(){console.log('touch move')}, false);

document.addEventListener('touchmove', function(evt){
    //console.dir('inside touchmove')
    if ( ! xDown || ! yDown ) {
        return;
    }

    console.dir('inside touchmove return')

    var xUp = evt.touches[0].clientX;                                    
    var yUp = evt.touches[0].clientY;

    var xDiff = xDown - xUp;
    var yDiff = yDown - yUp;

    if ( Math.abs( xDiff ) > Math.abs( yDiff ) ) {/*most significant*/
        if ( xDiff > 0 ) {
            /* left swipe */
            console.log('swipe left')
        } else {
            /* right swipe */
            console.log('swipe right')
        }                       
    } else {
        if ( yDiff > 0 ) {
            /* up swipe */ 
        } else { 
            /* down swipe */
        }                                                                 
    }
    /* reset values */
    xDown = null;
    yDown = null; 
}, false);                                   
/* end test */
 ```
