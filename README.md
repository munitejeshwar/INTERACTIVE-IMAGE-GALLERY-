## INTERACTIVE IMAGE GALLERY
## NAME:K MUNI TEJESHWAR
## REG NO: 212223040102
## DATE: 22/03/25
## PROGRAM:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h2>Image Gallery</h2>

    <div class="gallery-container">
        <button id="prevBtn">❮</button>
        <div class="gallery">
            <div class="image">
                <img src="King & Hitman ♥️✨.jpeg" alt="RO-KO">
                <div class="caption">CAR</div>
            </div>
            <div class="image">
                <img src="AA1AEJaM.jpeg" alt="ROHIT">
                <div class="caption">CAR</div>
            </div>
            <div class="image">
                <img src="rohit-sharma-cricket-mumbai-indians-mi-indian-premier-3840x2160-4993.png" alt="MUMBAI INDIANS">
                <div class="caption">DARK SKY</div>
            </div>
        </div>
        <button id="nextBtn">❯</button>
    </div>

    <footer>
        Created by K MUNI TEJESHWAR | Reg No: 212223040102
    </footer>

    <script src="script.js"></script>
</body>
</html>


```
## style.css:
```
body {
    font-family: Arial, sans-serif;
    text-align: center;
    background: #f4f4f4;
    margin: 0;
    padding: 0;
}

.gallery-container {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 20px auto;
    max-width: 600px;
    overflow: hidden;
}

.gallery {
    display: flex;
    transition: transform 0.5s ease-in-out;
}

.image {
    position: relative;
    margin: 5px;
    text-align: center;
}

.image img {
    width: 200px;
    height: 150px;
    border-radius: 10px;
    transition: 0.3s;
    display: block;
    margin: auto;
}

.image:hover img {
    transform: scale(1.1);
}

.caption {
    position: absolute;
    bottom: 10px;
    width: 100%;
    background: rgba(0, 0, 0, 0.7);
    color: white;
    padding: 5px;
    font-size: 14px;
    opacity: 0;
    transition: 0.3s;
}

.image:hover .caption {
    opacity: 1;
}

button {
    background-color: #333;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    font-size: 20px;
    border-radius: 5px;
}

button:hover {
    background-color: #555;
}

footer {
    background: #222;
    color: white;
    padding: 10px;
    position: fixed;
    width: 100%;
    bottom: 0;
}

```
## script.js:
```
const gallery = document.querySelector(".gallery");
const prevBtn = document.getElementById("prevBtn");
const nextBtn = document.getElementById("nextBtn");

let scrollAmount = 0;
const scrollStep = 210; // Adjusted for image width + margin

nextBtn.addEventListener("click", () => {
    if (scrollAmount < (3 - 1) * scrollStep) { // Adjusted for 3 images
        scrollAmount += scrollStep;
    }
    gallery.style.transform = `translateX(-${scrollAmount}px)`;
});

prevBtn.addEventListener("click", () => {
    if (scrollAmount > 0) {
        scrollAmount -= scrollStep;
    }
    gallery.style.transform = `translateX(-${scrollAmount}px)`;
});

```
OUTPUT:
![image](https://github.com/user-attachments/assets/92b4a052-15dc-4cf2-85bc-cf75ba7e54ce)
