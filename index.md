---
title       : Introduction of Slidify
subtitle    : 
author      : Wush Wu
job         : Taiwan R User Group
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
github:
  user: wush978
  repo: MLDMMonday_SlidifyTutorial
license: by-nc-sa
logo: Taiwan-R-logo.png
--- .segue .nobackground .dark




## Slidify

### Stunning Presentations from Markdown

--- &twocol

## Slidify

*** =left

- 由Ramnath Vaidyanathan所開發
- 採用Markdown語法
- 具有驚人的彈性，可以透過HTML、Java Script和CSS來做調整

*** =right

<img src="assets/img/slidify_logo.png" class="fit100" />

---

## 安裝

透過`devtools`從github安裝`Slidify`


```r
library(devtools)
install_github("slidify", "ramnathv")
```


### `devtools`的安裝

- 如果是Windows作業系統，請先安裝[`Rtools`](http://cran.r-project.org/bin/windows/Rtools/)
- 可參考社群教學影片：[安裝Rtools(Windows) ](http://www.youtube.com/watch?v=enPPMHr5SrM&list=PLM7HGQkDNOHtqUTowalvnOwZCx4mWDmte&feature=share&index=4)

--- 

## 開始人生第一個Slidify投影片


```r
library(slidify)
author("資料夾名稱")
```


- 會建立一個資料夾以及預設的`index.Rmd`
- 會建立一個git repository

TODO: 影片 or Demo

---

## 第一眼：

    ---
    title    : Title 
    substitle: Subtitle
    author   : Author
    job      : Job
    widgets  : []
    mode     : selfcontained
    ---
    
    ## Slide 1
    
    Use an empty line followed by three dashes to separate slides!
    
    --- .class #id 
    
    ## Slide 2

--- #cover bg:url(assets/img/Cover.png)

## 封面

---

## 投影片

    ---
    
    ## Slide 1
    
    Use an empty line followed by three dashes to separate slides!
    
    --- .class #id 
    
    ## Slide 2

- `---`表示分頁
- `##`表示投影片標題
- 採用Markdown語法，細節請參考[Markdown語法說明](http://markdown.tw/)，可在[Dillinger](http://dillinger.io)試玩。

---

## 與R 的整合

    ---
    
    \```{r}
    a <- 1
    a + 1
    f(a)
    \```
    
    ---


```
## [1] 2
```

```
## Error: 沒有這個函數 "f"
```


- 採用類似[knitr](http://yihui.name/knitr/)的方法
    - 可參考[20121203 MLDM Monday [markdown + knitr]](http://www.youtube.com/watch?v=OHKZLeKlUsM&feature=share)

--- &twocol

## 投影片的客製化

<img src="assets/img/customization.png" />

*** =left

### Layout

- 利用如`--- &twocol`來指定要用的layout
- 可以把layout放置於`assets/layout`底下，如：`assets/layouts/twocol.html`
- 產生投影片的套件是[whisker](http://cran.r-project.org/web/packages/whisker/index.html)

*** =right

<img src="assets/img/twocol.png" />

--- &twocol

## 自行定義twocolwithfoot

*** =left

<img src="assets/img/twocolwithfoot.png" />

*** =right

<img src="assets/img/source.png" />

--- &twocolwithfoot

## Header

*** =left

## Left

*** =right

## Right

*** =foot

## Foot

*** =pnotes

## Notes

---

## 發佈

請見Demo
