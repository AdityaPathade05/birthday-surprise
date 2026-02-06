<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday My Love</title>

<style>
body{
  margin:0;
  font-family:'Segoe UI',sans-serif;
  background:linear-gradient(135deg,#ffd1dc,#e0c3fc);
  overflow-x:hidden;
}

/* Center container */
.center{
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
}

/* Button */
button{
  background:#ff4f81;
  color:white;
  border:none;
  padding:18px 40px;
  font-size:20px;
  border-radius:30px;
  cursor:pointer;
  box-shadow:0 10px 25px rgba(0,0,0,0.2);
}

/* Card */
.card{
  background:white;
  padding:30px;
  border-radius:25px;
  box-shadow:0 15px 40px rgba(0,0,0,0.2);
  max-width:900px;
  margin:auto;
}

/* Hearts animation */
.heart{
  position:fixed;
  color:#ff4f81;
  animation:float 6s linear infinite;
}

@keyframes float{
  from{
    transform:translateY(100vh);
    opacity:1;
  }
  to{
    transform:translateY(-10vh);
    opacity:0;
  }
}

/* Gallery */
.gallery{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(150px,1fr));
  gap:15px;
  margin-top:20px;
}

.gallery img{
  width:100%;
  height:200px;
  object-fit:cover;
  border-radius:15px;
  box-shadow:0 5px 15px rgba(0,0,0,0.2);
}

h1{ color:#ff4f81; }
</style>
</head>

<body>

<!-- MUSIC -->
<audio id="music" loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_c8c8a73467.mp3?filename=romantic-love-11771.mp3" type="audio/mp3">
</audio>

<!-- CLICK SCREEN -->
<div id="startScreen" class="center">
  <div>
    <h1>❤️ Birthday Surprise ❤️</h1>
    <p>Click to open your surprise</p>
    <button onclick="openSurprise()">Click To Open ✨</button>
  </div>
</div>

<!-- MAIN SITE -->
<div id="mainSite" style="display:none; padding:40px;">

<div class="card">

<h1>Happy Birthday My Love ❤️</h1>

<p>
From the day you came into my life, everything became more beautiful.
You are my happiness, my peace, and my biggest blessing.
</p>

<p>
Your smile makes my worst days better.  
Your presence makes my world complete.
</p>

<p>
I am so lucky to have you.  
I promise to love you more every single day.
</p>

<h2>I Love You Forever ❤️</h2>

<!-- PHOTO GALLERY -->
<h2>Our Memories 📸</h2>

<div class="gallery">
<img src="https://picsum.photos/300/300?1">
<img src="https://picsum.photos/300/300?2">
<img src="https://picsum.photos/300/300?3">
<img src="https://picsum.photos/300/300?4">
</div>

</div>
</div>

<script>

/* CLICK OPEN */
function openSurprise(){
  document.getElementById("startScreen").style.display="none";
  document.getElementById("mainSite").style.display="block";
  document.getElementById("music").play();
  startHearts();
}

/* FLOATING HEARTS */
function startHearts(){
  setInterval(()=>{
    let heart=document.createElement("div");
    heart.innerHTML="❤️";
    heart.className="heart";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(Math.random()*20+20)+"px";
    document.body.appendChild(heart);

    setTimeout(()=>{ heart.remove(); },6000);
  },500);
}

</script>

</body>
</html>
