<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday My Love</title>

<style>

/* 🌌 Night Sky Background */
body{
  margin:0;
  font-family:'Segoe UI',sans-serif;
  background: radial-gradient(circle at bottom, #1b2735 0%, #090a0f 100%);
  height:100vh;
  overflow:hidden;
  display:flex;
  justify-content:center;
  align-items:center;
}

/* Stars */
body::before{
  content:"";
  position:fixed;
  width:100%;
  height:100%;
  background-image:radial-gradient(white 1px, transparent 1px);
  background-size:3px 3px;
  opacity:0.3;
}

/* Glass Card */
.card{
  background:rgba(255,255,255,0.15);
  backdrop-filter:blur(15px);
  padding:40px;
  border-radius:25px;
  text-align:center;
  color:white;
  z-index:5;
}

/* Button */
button{
  background:linear-gradient(45deg,#ff4f81,#ff85a2);
  border:none;
  padding:18px 40px;
  font-size:20px;
  color:white;
  border-radius:40px;
  cursor:pointer;
}

/* Floating Photos */
.photo{
  position:fixed;
  width:120px;
  height:160px;
  border-radius:20px;
  object-fit:cover;
  cursor:pointer;
  box-shadow:0 10px 25px rgba(0,0,0,0.5);
  animation:floatPhoto linear infinite;
}

@keyframes floatPhoto{
  from{ transform:translateY(110vh);}
  to{ transform:translateY(-20vh);}
}

/* Full Screen Viewer */
#viewer{
  position:fixed;
  top:0;
  left:0;
  width:100%;
  height:100%;
  background:rgba(0,0,0,0.95);
  display:none;
  justify-content:center;
  align-items:center;
  z-index:999;
}

#viewer img{
  max-width:90%;
  max-height:90%;
  border-radius:20px;
}

/* Hearts */
.heart{
  position:fixed;
  animation:float 6s linear infinite;
}
@keyframes float{
  from{ transform:translateY(100vh);}
  to{ transform:translateY(-10vh);}
}

/* Petals */
.petal{
  position:fixed;
  animation:fall linear infinite;
}
@keyframes fall{
  from{ transform:translateY(-10vh) rotate(0);}
  to{ transform:translateY(110vh) rotate(360deg);}
}

</style>
</head>

<body>

<audio id="music" loop>
<source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_c8c8a73467.mp3">
</audio>

<!-- Start -->
<div id="start" class="card">
<h1>💖 Birthday Surprise 💖</h1>
<p>Click to open your surprise</p>
<button onclick="openSite()">Click To Open ✨</button>
</div>

<!-- Main -->
<div id="main" class="card" style="display:none;">
<h1>Happy Birthday My Love ❤️</h1>
<p>You are my happiness, my forever.</p>
</div>

<!-- Full Screen Viewer -->
<div id="viewer" onclick="closeViewer()">
  <img id="viewerImg">
</div>

<script>

/* 🔥 ADD YOUR REAL PHOTO LINKS */
const photos=[
"https://picsum.photos/300/400?1",
"https://picsum.photos/300/400?2",
"https://picsum.photos/300/400?3",
"https://picsum.photos/300/400?4"
];

function openSite(){
 document.getElementById("start").style.display="none";
 document.getElementById("main").style.display="block";
 document.getElementById("music").play();

 startPhotos();
 startHearts();
 startPetals();
}

/* Floating Photos */
function startPhotos(){
 setInterval(()=>{
   let img=document.createElement("img");
   img.src=photos[Math.floor(Math.random()*photos.length)];
   img.className="photo";
   img.style.left=Math.random()*100+"vw";
   img.style.animationDuration=(Math.random()*6+6)+"s";

   img.onclick=()=>openViewer(img.src);

   document.body.appendChild(img);
   setTimeout(()=>img.remove(),12000);
 },1500);
}

/* Full Screen View */
function openViewer(src){
 document.getElementById("viewer").style.display="flex";
 document.getElementById("viewerImg").src=src;
}
function closeViewer(){
 document.getElementById("viewer").style.display="none";
}

/* Hearts */
function startHearts(){
 setInterval(()=>{
   let heart=document.createElement("div");
   heart.innerHTML="💖";
   heart.className="heart";
   heart.style.left=Math.random()*100+"vw";
   document.body.appendChild(heart);
   setTimeout(()=>heart.remove(),6000);
 },600);
}

/* Petals */
function startPetals(){
 setInterval(()=>{
   let petal=document.createElement("div");
   petal.innerHTML="🌹";
   petal.className="petal";
   petal.style.left=Math.random()*100+"vw";
   petal.style.animationDuration=(Math.random()*3+4)+"s";
   document.body.appendChild(petal);
   setTimeout(()=>petal.remove(),7000);
 },400);
}

</script>

</body>
</html>
