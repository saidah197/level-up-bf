# level-up-bf
<!DOCTYPE html>  <html lang="id">  
<head>  
<meta charset="UTF-8">  
<title>Happy Birthday 💖</title>  <style>  
body {  
  margin: 0;  
  background: linear-gradient(pink, #ffb6c1);  
  font-family: Arial;  
  text-align: center;  
  overflow: hidden;  
  color: white;  
}  
  
#openBtn {  
  margin-top: 40vh;  
  padding: 15px 30px;  
  font-size: 20px;  
  border: none;  
  border-radius: 20px;  
  background: white;  
  color: pink;  
  cursor: pointer;  
}  
  
#content {  
  display: none;  
  padding: 20px;  
}  
  
h1 {  
  font-size: 35px;  
}  
  
.slider {  
  width: 250px;  
  height: 300px;  
  margin: 20px auto;  
  overflow: hidden;  
  border-radius: 20px;  
  box-shadow: 0 0 20px white;  
}  
  
.slider img {  
  width: 100%;  
  height: 100%;  
  object-fit: cover;  
  display: none;  
}  
  
p {  
  font-size: 18px;  
  max-width: 600px;  
  margin: auto;  
}  
  
.heart {  
  position: absolute;  
  top: -10px;  
  animation: fall linear infinite;  
}  
  
@keyframes fall {  
  to {  
    transform: translateY(100vh);  
  }  
}  
</style>  </head>  <body>  <button id="openBtn" onclick="start()">Klik aku 💖</button>

<div id="content">  
  <h1>Happy Birthday Sayanggggg 💖</h1>    <div class="slider">  
    <img src="foto1.jpg">  
    <img src="foto2.jpg">  
    <img src="foto3.jpg">  
    <img src="foto4.jpg">  
  </div>    <p id="text"></p>  
</div>  <audio id="music" autoplay loop>  
  <source src="https://www.bensound.com/bensound-music/bensound-romantic.mp3">  
</audio>  <script>  
const message = [  
"Hallo sayangnyaa akuu 🤍",  
"Hari ini hari apaa niiii...",  
"iyaa benerr, hari ulang tahun kamu 😆💖",  
"Selamat ulang tahun yaa, Anjas Cryxel Wahyu Pratama 🤍",  
"Selamat berproses di umur kamu yang ke-18 ini ya sayang...",  
"Aku bakal selalu ada nemenin kamu, jadi jangan kemana-mana yaa 🥺",  
"Jadi cowo aku yang paling keren terus yaa!! 😆",  
"Semoga kamu selalu didekatkan sama hal-hal baik...",  
"(termasuk aku, karena aku baik 😋💖)",  
"Aku sayang kamu banyaaaak bangettt 🤍",  
"Lebih dari yang bisa aku jelasin 😭",  
"Happy level up day sayangggg 💖 - saidah cantikkk"  
];  
  
  
let i = 0;  
  
function start() {  
  document.getElementById("openBtn").style.display = "none";  
  document.getElementById("content").style.display = "block";  
  typeWriter();  
  createHearts();  
  startSlider();  
}  
  
function typeWriter() {  
  if (i < message.length) {  
    document.getElementById("text").innerHTML += message[i] + "<br><br>";  
    i++;  
    setTimeout(typeWriter, 2000);  
  }  
}  
  
function startSlider() {  
  let slides = document.querySelectorAll(".slider img");  
  let index = 0;  
  slides[0].style.display = "block";  
  
  setInterval(() => {  
    slides[index].style.display = "none";  
    index = (index + 1) % slides.length;  
    slides[index].style.display = "block";  
  }, 2000);  
}  
  
function createHearts() {  
  setInterval(() => {  
    const heart = document.createElement("div");  
    heart.classList.add("heart");  
    heart.innerHTML = "💖";  
    heart.style.left = Math.random() * 100 + "vw";  
    heart.style.animationDuration = (Math.random() * 3 + 2) + "s";  
    heart.style.fontSize = (Math.random() * 20 + 20) + "px";  
    document.body.appendChild(heart);  
  
    setTimeout(() => {  
      heart.remove();  
    }, 5000);  
  }, 300);  
}  
</script>  </body>  
</html>
