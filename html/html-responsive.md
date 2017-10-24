# Responsive Web Design

* [Responsive Web Design](http://www.w3schools.com/css/css_rwd_intro.asp)

## Images

##### Scale down

    img {
        max-width: 100%;
        height: auto;
    }

##### Scale up and down

    img {
        width: 100%;
        height: auto;
    }

##### Background

    div {
        width: 100%;
        height: 400px;
        background-image: url('img.jpg');
        background-repeat: no-repeat;
        background-size: contain;
        border: 1px solid red;
    }



---

Full size background image:

```
html {
    background: url(img_flower.jpg) no-repeat center fixed; 
    background-size: cover;
}
```

Or create a div with e.g. fixed-bc class. This stays fixed when scrolling:

```
.fixed-bg {
    background-image: url("img.gif");
    min-height: 500px;
    background-attachment: fixed;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
}



