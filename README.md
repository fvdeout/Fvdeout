<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Party Entertainment</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    html, body {
      height: 100%;
      overflow: hidden;
      font-family: 'Segoe UI', sans-serif;
    }
    .slider {
      display: flex;
      width: 500%;
      height: 100vh;
      transition: transform 0.6s ease-in-out;
    }
    .slide {
      width: 100vw;
      height: 100vh;
      flex-shrink: 0;
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      background-size: cover;
      background-position: center;
    }
    .slide h1 {
      color: white;
      font-size: 4rem;
      text-shadow: 2px 2px 10px rgba(0,0,0,0.6);
    }
    .nav-btn {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background: rgba(0,0,0,0.5);
      color: white;
      font-size: 2rem;
      border: none;
      padding: 1rem;
      cursor: pointer;
      z-index: 10;
    }
    .prev { left: 10px; }
    .next { right: 10px; }
    .slide1 { background-image: url('https://via.placeholder.com/1920x1080/FF69B4/000000?text=Slide+1'); }
    .slide2 { background-image: url('https://via.placeholder.com/1920x1080/00BFFF/000000?text=Slide+2'); }
    .slide3 { background-image: url('https://via.placeholder.com/1920x1080/FFD700/000000?text=Slide+3'); }
    .slide4 { background-image: url('https://via.placeholder.com/1920x1080/ADFF2F/000000?text=Slide+4'); }
    .slide5 { background-image: url('https://via.placeholder.com/1920x1080/FF4500/000000?text=Slide+5'); }
  </style>
</head>
<body>
  <div class="slider" id="slider">
    <div class="slide slide1"><h1>Welcome</h1></div>
    <div class="slide slide2"><h1>Our Services</h1></div>
    <div class="slide slide3"><h1>Gallery</h1></div>
    <div class="slide slide4"><h1>Packages</h1></div>
    <div class="slide slide5"><h1>Contact</h1></div>
  </div>
  <button class="nav-btn prev" onclick="prevSlide()">❮</button>
  <button class="nav-btn next" onclick="nextSlide()">❯</button>

  <script>
    let index = 0;
    function showSlide() {
      const slider = document.getElementById('slider');
      slider.style.transform = `translateX(-${index * 100}vw)`;
    }
    function prevSlide() {
      index = (index - 1 + 5) % 5;
      showSlide();
    }
    function nextSlide() {
      index = (index + 1) % 5;
      showSlide();
    }
  </script>
</body>
</html>
