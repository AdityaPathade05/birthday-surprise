<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday My Love</title>

<style>

/* 🌌 Night Sky */
body{
 margin:0;
 font-family:Segoe UI, sans-serif;
 background: radial-gradient(circle at bottom,#1b2735,#090a0f);
 height:100vh;
 overflow:hidden;
 display:flex;
 justify-content:center;
 align-items:center;
}

body::before{
 content:"";
 position:fixed;
 width:100%;
 height:100%;
 background-image:radial-gradient(white 1px, transparent 1px);
 background-size:3px 3px;
 opacity:0.25;
}

/* Glass Card */
.card{
 background:rgba(255,255,255,0.1);
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

/* Floating Photo */
.photo{
 position:fixed;
 width:110px;
 height:150px;
 border-radius:18px;
 object-fit:cover;
 cursor:pointer;
 animation:floatPhoto linear infinite;
}
@keyframes floatPhoto{
 from{ transform:translateY(110vh);}
 to{ transform:translateY(-20vh);}
}

/* Viewer */
#viewer{
 position:fixed;
 width:100%;
 height:100%;
 background:black;
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

/* Hearts Float */
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

/* ❤️ Big Heart Container */
.heart-container{
 position:fixed;
 bottom:50px;
 right:50px;
 width:300px;
 height:300px;
 z-index:2;
}
.small-heart{
 position:absolute;
 font-size:16px;
 animation:pop 1.5s infinite alternate;
}
@keyframes pop{
 from{ transform:scale(1);}
 to{ transform:scale(1.3);}
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

<!-- Viewer -->
<div id="viewer" onclick="closeViewer()">
<img id="viewerImg">
</div>

<!-- Big Heart -->
<div class="heart-container" id="bigHeart"></div>

<script>

/* 🔥 ADD YOUR REAL PHOTOS HERE */
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
 makeBigHeart();
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

/* Viewer */
function openViewer(src){
 viewer.style.display="flex";
 viewerImg.src=src;
}
function closeViewer(){
 viewer.style.display="none";
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

/* ❤️ Big Heart Made of Small Hearts */
function heartShape(t){
 return {
   x:16*Math.pow(Math.sin(t),3),
   y:-(13*Math.cos(t)-5*Math.cos(2*t)-2*Math.cos(3*t)-Math.cos(4*t))
 };
}

function makeBigHeart(){
 const container=document.getElementById("bigHeart");
 for(let i=0;i<80;i++){
   let t=i/80*Math.PI*2;
   let pos=heartShape(t);

   let heart=document.createElement("div");
   heart.className="small-heart";
   heart.innerHTML="❤️";

   heart.style.left=(150+pos.x*6)+"px";
   heart.style.top=(150+pos.y*6)+"px";

   container.appendChild(heart);
 }
}

</script>

</body>
</html>
