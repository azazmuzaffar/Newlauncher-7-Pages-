### Note: All the changes have been made for 768px to 992px resolution only.

<hr>

## 1) The logo/icons are not coming in order b/w 768px to 992px resolution.

![image](https://user-images.githubusercontent.com/64412852/182362281-b0ec0a1c-d10b-420c-8a7b-1bd1acf92308.png)

## Solution: 

### (style.css) (6784 line)

Please remove the <b> display: block; </b> and add <b> width: fit-content; </b> to the media query.

```css

@media only screen and (max-width: 991.98px) {
  .as-featured-area.container .brands-area {
    max-width: 724px;
    margin-bottom: 0px;
    margin-top: 36px;
    /* display: block; */
    width: fit-content;
  }
}

```

## 2) Remove the third one b/w 768px to 992px resolution.

![image](https://user-images.githubusercontent.com/64412852/182364505-207db9a9-7c42-47f7-a298-084657efdec3.png)

## Solution: 

### (about_us.blade.html) (~135 line)

Add/replace the highlighted class to the third/last element only, currently it's in loop/dynamic so can't do it on my own, but please figure this out.
Note: you just need to add the class, it will work work on it's own b/w 768px to 992px resolution.

![image](https://user-images.githubusercontent.com/64412852/182365417-d237d141-132d-421d-bd23-58d8a514c895.png)


## 3) Gray text is breaking to next line weirdly.

![image](https://user-images.githubusercontent.com/64412852/182370236-f6f1e682-2581-4be8-a3a4-e9c109afa16a.png)

<hr>

![image](https://user-images.githubusercontent.com/64412852/182395735-f8109d8b-b3ec-4e55-b4dc-1ed4d9770030.png)


## Solution: 

Please replace the three paragraphs accordingly on both contact and partner page.

### (contact_us.blade.html) (partner.blade.html)

```html
<p>We reply to all messages <span class="bl-visible-on-ipad-only"><br></span> within 12 hours.</p>
```

```html
<p>Daily appointment from <span class="bl-visible-on-ipad-only"><br></span> 11am to 7pm.</p>
```

```html
<p>Possibly, the fastest <span class="bl-visible-on-ipad-only"><br></span> way to reach us.</p>
```

### (about_us.blade.html)

```html
 <p class="fs-18">And by 2023, we will be adding 30 more developers, bringing <span class="bl-visible-on-ipad-only"><br></span> 99.9% of available launches to our portal.</p>
```

### Add the CSS code in (style.css) 

```css

/* Visible on Ipad only - Start */
.bl-visible-on-ipad-only{
  display: none;
}
@media only screen and (max-width: 991px){
  .bl-visible-on-ipad-only{
    display: block;
    display: unset;
  }
}
@media only screen and (max-width: 768px){
  .bl-visible-on-ipad-only{
    display: none;
  }
}
/* End - Visible on Ipad only */

```

## 4) Making text bigger on some place on about page...

### please find the following text on about page and give then the following class.

**********************************************

At NEWLAUNCHER, we bridge buyers to developers.<br>
To date, we have partnered with 78 developers.<br>
And by 2023, we will be adding 30 more developers, bringing 99.9% of available launches to our portal.<br>
We are humbled & driven to serve you.<br>
At NEWLAUNCHER, we strive for excellence.<br>
We innovated NEWLAUNCHER, keeping you in mind.<br>
To be the only platform of choice for new launches. 

**********************************************

### Class

```html
 class="fs-18"
```

### Add CSS in style.css

```css

/* Fonts Size 18px for ipad - Start */
@media only screen and (max-width: 991px) and (min-width: 768px) {
  .fs-18{
    font-size: 18px !important;
  }
}
/* End - Fonts Size 18px for ipad */

```

<hr>

# That's All, Thank you!

## 5) Why gap is coming on left and right side.
![image](https://user-images.githubusercontent.com/64412852/182407047-db6c6bd0-d442-40dc-84d2-ae1030557ef1.png)

### please change the width from 960px to 100% (style.css) (~6710)

```css
@media only screen and (max-width: 1200px) {
  .as-featured-area.container {
    /* max-width: 960px; */
    max-width: 100%;
  }
}
```

## 6) Contact us form fields are not aligned properly in these screen size...
![Screenshot_2](https://user-images.githubusercontent.com/64412852/183235695-73faf2f9-b693-463e-a00c-eaded06444c1.png)

(style.css)

Change the max-width from 767.98px to 991px, as below...

![image](https://user-images.githubusercontent.com/64412852/183235900-03efb8d1-e5de-426d-8527-12602692ae40.png)
 






