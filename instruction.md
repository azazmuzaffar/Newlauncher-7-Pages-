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
