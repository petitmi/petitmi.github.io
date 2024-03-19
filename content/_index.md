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
    <img src="gallery/self.jpg" style="width:100%" class="demo cursor" onclick="currentSlide(2)" alt="Me in my friends' views">
  </div>

  <div class="mySlides">
    <img src="gallery/ideal-life.jpg"  style="width:100%" class="demo cursor" onclick="currentSlide(1)" alt="My ideal life (HAHA)">
  </div> -->
    
  <a class="prev" onclick="plusSlides(-1)">❮</a>
  <a class="next" onclick="plusSlides(1)">❯</a>

  <div class="caption-container">
    <p id="caption"></p>
  </div>


</div>

<!-- **My Monologue:**   -->
I am a data analyst. I see things inside data and build products to let you see them too.

Check out stuffs about me!
[Blogs](https://petitmi.com/bread) | [Medium](https://medium.com/@petitmi001) | [Linkedin](https://www.linkedin.com/in/yuchen-nyx-zhang/) | [Youtube]https://www.youtube.com/channel/UC6YTScw2p9u6AHp-tgXDIrA

Fun facts about me:
- I live in Canada and love it more every day. I hope to travel to Montreal, the Yukon and beyond.
- I'm from Xi'an, the historic city of China, also as known as the Carb food city. And I like Sichuan/Choqing/Chaoshan Hotpot, [Xi'an Liangpi](https://www.chinaxiantour.com/xian-travel-guides/xian-local-food/liangpi.html). 
- I wrote songs, and becaused of one of the songs, I was banned by a UGC website similar to Youtube. I love songs with electron, Jazz, or catchy sound effects factors, either floating or provoking.
- I feel never statisfied with my self introduction. So it changes often.
- I take all my pictures for laughs, so I have a tough time finding LinkedIn profile avatars or the gallery above.

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