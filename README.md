# Gavekort 
<!DOCTYPE html>
<html lang="da">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>∞ Gavekort</title>
  <style>
    body {
      margin: 0;
      background: white;
      font-family: sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      flex-direction: column;
    }

    #intro {
      font-size: 3em;
      cursor: pointer;
      opacity: 1;
      transition: opacity 0.5s ease;
    }

    .image-container {
      display: none;
    }

    .image-container img {
      max-width: 90vw;
      max-height: 90vh;
      display: none;
    }

    .image-container img.active {
      display: block;
    }
  </style>
</head>
<body>
  <div id="intro">∞ Gavekort</div>

  <div class="image-container" id="slideshow">
    <img src="Billede 1.jpeg" alt="kram">
    <img src="Billede 2.jpeg" alt="støtte">
    <img src="Billede 3.jpeg" alt="hjælp">
    <img src="Billede 4.jpeg" alt="faster">
  </div>

  <script>
    const intro = document.getElementById("intro");
    const slideshow = document.getElementById("slideshow");
    const images = slideshow.getElementsByTagName("img");
    let index = 0;

    intro.addEventListener("click", () => {
      intro.style.display = "none";
      slideshow.style.display = "block";
      images[0].classList.add("active");

      setInterval(() => {
        images[index].classList.remove("active");
        index = (index + 1) % images.length;
        images[index].classList.add("active");
      }, 2500); // Skift hvert 2.5 sekund
    });
  </script>
</body>
</html>
![Billede 1](https://github.com/user-attachments/assets/40b158db-a841-4c4b-ad47-e259ec705732)
![Billede 2](https://github.com/user-attachments/assets/8dcccaa1-1210-4050-9029-db4e5e2ed815)
![Billede 3](https://github.com/user-attachments/assets/f7e0bc89-20e7-4db3-a1b5-f695e6fecf24)
![Billede 4](https://github.com/user-attachments/assets/4d14ef8c-347a-4103-9968-e6b1853bb1f9)
