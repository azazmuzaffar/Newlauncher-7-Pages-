### Note: All the changes have been made for 768px to 992px resolution only.

<hr>

## 1) The logo/icons are not coming in order b/w 768px to 992px resolution.

![image](https://user-images.githubusercontent.com/64412852/182362281-b0ec0a1c-d10b-420c-8a7b-1bd1acf92308.png)

## Solution: 

(style.css) (6784 line)

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

## 1) Remove the third one b/w 768px to 992px resolution.

![image](https://user-images.githubusercontent.com/64412852/182364505-207db9a9-7c42-47f7-a298-084657efdec3.png)

## Solution: 

Add/replace the highlighted class to the third/last element only, currently it's in loop/dynamic so can't do it on my own, but please figure this out.
Note: you just need to add the class, it will work work on it's own b/w 768px to 992px resolution.

![image](https://user-images.githubusercontent.com/64412852/182365417-d237d141-132d-421d-bd23-58d8a514c895.png)



