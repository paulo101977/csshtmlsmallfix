# CSS HTML Small fix tutorial

## 1 - how Fix div size in small screens/mobile

The fix is in stackoverflow link:

http://stackoverflow.com/questions/18588835/allow-a-div-to-cover-the-whole-page-instead-of-the-area-within-the-container

Step:

change the position absolute of the div for "fixed"

Example:

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
