---
# title: "Yuchen Zhang"


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

# 

<div class="container">

  <div class="mySlides">
    <img src="gallery/self.jpg" style="width:100%" class="demo cursor" onclick="currentSlide(1)" alt="Me in my friends' views">
  </div>

  <div class="mySlides">
    <img src="gallery/ideal-life.JPG"  style="width:100%" class="demo cursor" onclick="currentSlide(2)" alt="My ideal life (HAHA)">
  </div> 
    
  <a class="prev" onclick="plusSlides(-1)">❮</a>
  <a class="next" onclick="plusSlides(1)">❯</a>

  <div class="caption-container">
    <p id="caption"></p>
  </div>


</div>

<!-- **My Monologue:**   -->
I am a data analyst/scientist. I see things behind data and build products to let you see them too.

Check out the links about me: [Blogs](https://petitmi.com/bread) | [Medium](https://medium.com/@petitmi001) | [Linkedin](https://www.linkedin.com/in/yuchen-nyx-zhang/) | [Youtube](https://www.youtube.com/channel/UC6YTScw2p9u6AHp-tgXDIrA)

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