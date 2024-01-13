---
# title: "Nyx"
description: "回归个体 Back To Individual"

---


<style>
body {
  font-family: Arial;
  margin: 0;
}

* {
  box-sizing: border-box;
}

img {
  vertical-align: middle;
  object-fit: contain;
  height: 300px; /* Your preferred width */
  width: auto;

}

/* Position the image container (needed to position the left and right arrows) */
.container {
  position: relative;
}

/* Hide the images by default */
.mySlides {
  display: none;
}

/* Add a pointer when hovering over the thumbnail images */
.cursor {
  cursor: pointer;
}

/* Next & previous buttons */
.prev,
.next {
  background-color: rgba(192,192,192, 0.8);
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  margin-top: -50px;
  color: white;
  font-weight: bold;
  font-size: 20px;
  border-radius: 0 3px 3px 0;
  user-select: none;
  -webkit-user-select: none;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

/* Container for image text */
.caption-container {
  text-align: center;
  background-color: #222;
  /* padding: 2px 10px; */
  color: white;
}
</style>

<!-- ######################### -->

<body>

# Nyx

<div class="container">
  <!-- <div class="mySlides">
    <img src="gallery/gongxi.jpg"  style="width:100%" class="demo cursor" onclick="currentSlide(1)" alt="Me playing rock">
  </div> 

  <div class="mySlides">
    <img src="gallery/me_duck.jpg"  style="width:100%" class="demo cursor" onclick="currentSlide(1)" alt="Me And A Canadian Duck">
  </div> -->

  <div class="mySlides">
    <img src="gallery/self.jpg" style="width:100%" class="demo cursor" onclick="currentSlide(2)" alt="Two Me In A Time. Souce: Magifrenchie, and Peacinu">
  </div>

    
  <a class="prev" onclick="plusSlides(-1)">❮</a>
  <a class="next" onclick="plusSlides(1)">❯</a>

  <div class="caption-container">
    <p id="caption"></p>
  </div>


</div>

<!-- **My Monologue:**   -->
I work on data, as a data analyst or a data scientist as you call me. I have a bachelor's in statistics and a master's in data science, with 5 years of industry experience. I am knowledgeable about [how data flow works](https://petitmi.com/bread/20230920-data-product/) and have led multiple end-to-end projects in both data analytics and machine learning.

In my spare time, I enjoy boxing, music, and discussing movies and books with beloved friends.

I feel it's an unstoppable trend that people are becoming data rows crossed in servers of internet platforms, which makes my work increasingly important. But I believe it's never the definition of human existence, and the most precious part of humanity is sophisticated feelings and thoughts, both good and lost.

> Some of my portfolio and thoughts: [Bread](https://petitmi.com/bread).

<!-- <table class="translation">
    <tr>
        <td>
**嘿，伙计** 你好。在这儿，以数据科学和商业为主职业感悟在[Bread](https://petitmi.com/bread)中。其他的在[Juicy](https://petitmi.com/juicy)里，包括情感夜话、都市传说、爱的教育和其他所有。内容是由[中文](https:petitmi.com/categories/%E4%B8%AD%E6%96%87/)和[英文](https:petitmi.com/categories/english/)书写的，可以通过*Seeds-Categories*筛选。

**关于我的一些事实：**
- 我的[名字](/juicy/20230831-name-preceeds-essence/):张雨晨，Nyx。
- 喜欢包含布鲁斯、爵士、电子、太空流行之类元素的音乐，三拍子律动的音乐有时会不明所以地触动我。
- 欢迎用电子邮箱与我聊天: petitmi001#gmail.com


以上内容在下次编辑前有效。
        </td>
        <td> 

**G’day, dute.** There you go, data science and business oriented career epiphanies are in [Bread](https://petitmi.com/bread). Others are in [Juicy](https://petitmi.com/juicy), including emotional night talk, urban legends, love education and all the rest. The content is written in [Chinese](https:petitmi.com/categories/%E4%B8%AD%E6%96%87/) and [English](https:petitmi.com/categories/english/) and can be filtered by *Seeds-Categories*! .


**Some of my other facts:**
- My [names](/juicy/20230831-name-preceeds-essence/), Yuchen Zhang, Nyx and so on.
- Love music with elements like blues, jazz, electronic, space pop, etc. Music with three-beat rhythms sometimes touches me in an unexplained way. 
- Feel free to chat with me by e-mail: petitmi001#gmail.com

Expired before next edit.
        </td>
    </tr>
</table> -->

<script>
let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("demo");
  let captionText = document.getElementById("caption");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
  captionText.innerHTML = dots[slideIndex-1].alt;
}
</script>
</body>




---