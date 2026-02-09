<!doctype html>
<html lang="en" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday My Love</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&amp;family=Quicksand:wght@400;500;600&amp;family=Pacifico&amp;family=Comfortaa:wght@400;700&amp;display=swap" rel="stylesheet">
  <style>
body {
  box-sizing: border-box;
}

/* Soft Stars */
.starfield::before {
  content: "";
  position: fixed;
  width: 100%;
  height: 100%;
  background-image: 
    radial-gradient(#ffb6e1 1px, transparent 1px),
    radial-gradient(#ffc0d9 1px, transparent 1px);
  background-size: 50px 50px, 30px 30px;
  background-position: 0 0, 25px 25px;
  opacity: 0.25;
  animation: twinkle 4s ease-in-out infinite alternate;
  pointer-events: none;
}

/* Cute floating background hearts */
.starfield::after {
  content: "";
  position: fixed;
  width: 100%;
  height: 100%;
  background-image: 
    url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><path d="M50,85 C20,65 5,50 5,38 C5,25 15,15 25,15 C32,15 40,20 50,28 C60,20 68,15 75,15 C85,15 95,25 95,38 C95,50 80,65 50,85Z" fill="%23ffb6e1" opacity="0.08"/></svg>');
  background-size: 150px 150px;
  background-position: 0 0;
  animation: floatPattern 20s linear infinite;
  pointer-events: none;
}

@keyframes floatPattern {
  0% { transform: translateY(0px); }
  100% { transform: translateY(30px); }
}

@keyframes twinkle {
  0% { opacity: 0.2; }
  100% { opacity: 0.4; }
}

/* Glass Card */
.glass-card {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.15);
}

/* Floating Photo */
.photo {
  position: fixed;
  width: 120px;
  height: 160px;
  border-radius: 16px;
  object-fit: cover;
  cursor: pointer;
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.5);
  animation: floatPhoto linear forwards;
  transition: transform 0.3s, box-shadow 0.3s;
  z-index: 10;
}

.photo:hover {
  transform: scale(1.1) !important;
  box-shadow: 0 20px 50px rgba(255, 118, 170, 0.4);
}

@keyframes floatPhoto {
  from { transform: translateY(100%); }
  to { transform: translateY(-200px); }
}

/* Floating Hearts */
.heart {
  position: fixed;
  cursor: pointer;
  font-size: 24px;
  animation: floatHeart linear forwards;
  transition: transform 0.2s;
  z-index: 5;
  user-select: none;
}

.heart:hover {
  transform: scale(1.5) !important;
}

@keyframes floatHeart {
  from { transform: translateY(100%) rotate(0deg); }
  to { transform: translateY(-100px) rotate(20deg); }
}

/* Petals */
.petal {
  position: fixed;
  font-size: 20px;
  animation: fallPetal linear forwards;
  pointer-events: none;
  z-index: 3;
}

@keyframes fallPetal {
  0% { 
    transform: translateY(-50px) rotate(0deg); 
    opacity: 1;
  }
  100% { 
    transform: translateY(100%) rotate(360deg); 
    opacity: 0.3;
  }
}

/* Heart Burst Animation */
.heart-burst {
  position: fixed;
  font-size: 30px;
  animation: burst 0.8s ease-out forwards;
  pointer-events: none;
  z-index: 100;
}

@keyframes burst {
  0% { 
    transform: scale(0.5); 
    opacity: 1; 
  }
  100% { 
    transform: scale(2) translateY(-50px); 
    opacity: 0; 
  }
}

/* Cute Button */
.cute-btn {
  background: linear-gradient(135deg, #ff7eb3, #ff758c, #ff6b6b);
  background-size: 200% 200%;
  animation: gradientShift 3s ease infinite;
  transition: all 0.3s ease;
}

.cute-btn:hover {
  transform: scale(1.08) translateY(-2px);
  box-shadow: 0 15px 35px rgba(255, 118, 170, 0.5);
}

.cute-btn:active {
  transform: scale(0.98);
}

@keyframes gradientShift {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}

/* Love Popup */
.love-popup {
  animation: popIn 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

@keyframes popIn {
  0% { transform: translateX(-50%) scale(0); }
  100% { transform: translateX(-50%) scale(1); }
}

/* Sparkle Effect */
.sparkle {
  position: fixed;
  width: 10px;
  height: 10px;
  background: white;
  border-radius: 50%;
  animation: sparkle 1s ease-out forwards;
  pointer-events: none;
}

@keyframes sparkle {
  0% { transform: scale(0); opacity: 1; }
  50% { transform: scale(1); opacity: 0.8; }
  100% { transform: scale(0); opacity: 0; }
}

/* Viewer Overlay */
.viewer-overlay {
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
}

/* Title Animation */
.title-glow {
  text-shadow: 0 0 20px rgba(255, 118, 170, 0.5), 0 0 40px rgba(255, 118, 170, 0.3);
  animation: glow 2s ease-in-out infinite alternate;
}

@keyframes glow {
  from { text-shadow: 0 0 20px rgba(255, 118, 170, 0.5), 0 0 40px rgba(255, 118, 170, 0.3); }
  to { text-shadow: 0 0 30px rgba(255, 118, 170, 0.8), 0 0 60px rgba(255, 118, 170, 0.5); }
}

@keyframes bounceCute {
  0%, 100% { transform: translateY(0) scale(1); }
  50% { transform: translateY(-15px) scale(1.1); }
}

/* Clickable Word Animation */
.cute-word {
  display: inline-block;
  cursor: pointer;
  padding: 2px 6px;
  border-radius: 6px;
  transition: all 0.3s ease;
  font-weight: 600;
  color: #ff7eb3;
}

.cute-word:hover {
  background: rgba(255, 126, 179, 0.2);
  transform: scale(1.1);
  text-shadow: 0 0 10px rgba(255, 126, 179, 0.6);
}

.cute-word:active {
  transform: scale(0.95);
}

/* Button Grid */
.button-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
}

.small-btn {
  background: rgba(255, 126, 179, 0.3);
  border: 2px solid rgba(255, 126, 179, 0.5);
  color: white;
  padding: 10px 16px;
  border-radius: 20px;
  cursor: pointer;
  font-size: 14px;
  transition: all 0.3s ease;
  font-weight: 600;
}

.small-btn:hover {
  background: rgba(255, 126, 179, 0.6);
  transform: scale(1.05);
  box-shadow: 0 8px 20px rgba(255, 118, 170, 0.3);
}

.small-btn:active {
  transform: scale(0.95);
}

/* Slideshow Container */
.slideshow-container {
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.slide {
  display: none;
  position: relative;
  width: 100%;
  height: 100%;
  animation: slideIn 0.8s ease-in-out;
}

.slide.active {
  display: flex;
  align-items: center;
  justify-content: center;
}

.slide img {
  max-width: 90%;
  max-height: 85%;
  border-radius: 20px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.6);
  animation: imageZoom 0.8s ease-out;
}

@keyframes slideIn {
  0% { opacity: 0; }
  100% { opacity: 1; }
}

@keyframes imageZoom {
  0% { 
    transform: scale(0.8) rotate(-5deg);
    opacity: 0;
  }
  100% { 
    transform: scale(1) rotate(0deg);
    opacity: 1;
  }
}

/* Slideshow Controls */
.slideshow-controls {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 15px;
  z-index: 20;
}

.slide-btn {
  background: rgba(255, 126, 179, 0.6);
  border: 2px solid rgba(255, 255, 255, 0.5);
  color: white;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  cursor: pointer;
  font-size: 20px;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
}

.slide-btn:hover {
  background: rgba(255, 126, 179, 0.9);
  transform: scale(1.1);
  box-shadow: 0 8px 20px rgba(255, 118, 170, 0.5);
}

.slide-btn:active {
  transform: scale(0.95);
}

/* Slide Counter */
.slide-counter {
  position: absolute;
  top: 20px;
  right: 20px;
  background: rgba(255, 126, 179, 0.4);
  border: 1px solid rgba(255, 255, 255, 0.3);
  color: white;
  padding: 8px 16px;
  border-radius: 20px;
  font-size: 14px;
  font-weight: 600;
}

/* Close Slideshow */
.close-slideshow {
  position: absolute;
  top: 20px;
  left: 20px;
  background: rgba(255, 126, 179, 0.4);
  border: 1px solid rgba(255, 255, 255, 0.3);
  color: white;
  width: 45px;
  height: 45px;
  border-radius: 50%;
  cursor: pointer;
  font-size: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
}

.close-slideshow:hover {
  background: rgba(255, 126, 179, 0.8);
  transform: scale(1.1);
}

/* Floating Hearts Around Slideshow */
.slideshow-heart {
  position: absolute;
  font-size: 30px;
  animation: floatAroundSlideshow 4s ease-in-out infinite;
  opacity: 0.7;
}

@keyframes slideThoughtIn {
  0% { transform: translateX(-50%) scale(0); opacity: 0; }
  100% { transform: translateX(-50%) scale(1); opacity: 1; }
}

@keyframes floatAroundSlideshow {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

</style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full m-0 overflow-hidden flex justify-center items-center starfield" style="font-family: 'Comfortaa', cursive; background: linear-gradient(135deg, #ffe4f0 0%, #ffc0e0 25%, #ffb3d9 50%, #ff99c8 75%, #ff80bb 100%); position: relative;">
  <style>
    body::before {
      content: "💕 💕 💕 💕 💕 💕 💕 💕 💕 💕 💕 💕 💕";
      position: fixed;
      top: -50px;
      left: 0;
      right: 0;
      font-size: 80px;
      letter-spacing: 60px;
      animation: slideHearts 25s linear infinite;
      opacity: 0.15;
      white-space: nowrap;
      pointer-events: none;
      z-index: 1;
    }
  </style>
  <style>
    @keyframes slideHearts {
      0% { transform: translateY(0px); }
      100% { transform: translateY(100vh); }
    }
  </style><!-- Start Screen -->
  <div id="start" class="glass-card p-10 md:p-12 rounded-3xl text-center max-w-md mx-4 z-20 relative">
   <div class="text-7xl mb-6 animate-bounce" style="animation: bounceCute 1s infinite;">
    💝
   </div>
   <h1 class="text-4xl md:text-5xl font-bold text-white mb-4" style="font-family: 'Pacifico', cursive; text-shadow: 0 4px 15px rgba(255, 100, 150, 0.4), 0 0 20px rgba(255, 150, 180, 0.3); letter-spacing: 1px;">Happy Birthday Baby 💕</h1>
   <p class="text-pink-100 mb-8 text-xl" style="font-family: 'Comfortaa', cursive;">A special gift from your love 🥰</p><button onclick="openSite()" class="cute-btn border-none py-4 px-12 text-xl text-white rounded-full cursor-pointer shadow-lg font-bold" style="font-family: 'Comfortaa', cursive; letter-spacing: 0.5px;"> 💗 Open Your Surprise 💗 </button>
  </div><!-- Main Content -->
  <div id="main" class="glass-card p-8 md:p-12 rounded-3xl text-center max-w-2xl mx-4 z-20 relative hidden overflow-y-auto max-h-[90vh]">
   <div class="text-5xl mb-4">
    🎂
   </div>
   <h1 id="mainTitle" class="title-glow text-4xl md:text-5xl font-bold text-white mb-4" style="font-family: 'Pacifico', cursive; letter-spacing: 1px;">Happy Birthday My Love ❤️</h1>
   <p id="loveMessage" class="text-pink-100 text-xl mb-6 leading-relaxed" style="font-family: 'Comfortaa', cursive;">You are my happiness, my forever.</p><!-- Main Action Buttons -->
   <div class="flex flex-col gap-4 mb-8"><button onclick="showLove()" class="cute-btn border-none py-4 px-10 text-lg text-white rounded-full cursor-pointer shadow-lg font-bold" style="font-family: 'Comfortaa', cursive; font-size: 18px;"> 💕 Tap For Love 💕 </button> <button onclick="showSpecialMessage()" class="bg-gradient-to-r from-red-300 to-pink-300 hover:from-red-400 hover:to-pink-400 border-none py-3 px-8 text-white rounded-full cursor-pointer transition-all duration-300 hover:scale-105 font-bold" style="font-family: 'Comfortaa', cursive; font-size: 16px;"> 💌 Special Message 💌 </button>
   </div><!-- Interactive Buttons Grid -->
   <div class="mb-8 p-6 bg-white/5 rounded-2xl border border-white/10">
    <h3 class="text-pink-200 font-bold mb-4 text-xl" style="font-family: 'Pacifico', cursive;">✨ Click to see my thoughts behind these words 👇 ✨</h3>
    <div class="button-grid"><button onclick="showThought('Beautiful 💫', 'Your beauty isn\'t just what I see—it\'s the way you light up every room you enter')" class="small-btn">Beautiful 💫</button> <button onclick="showThought('Elegant 👑', 'The grace with which you carry yourself is absolutely captivating')" class="small-btn">Elegant 👑</button> <button onclick="showThought('Gorgeous 😍', 'Every time I look at you, I wonder how I got so lucky')" class="small-btn">Gorgeous 😍</button> <button onclick="showThought('Charming 💕', 'Your charm could win over anyone—but I\'m the one who gets to keep you')" class="small-btn">Charming 💕</button> <button onclick="showThought('Radiant ✨', 'You glow with a light that makes the world brighter')" class="small-btn">Radiant ✨</button> <button onclick="showThought('Stunning ���', 'You take my breath away every single day')" class="small-btn">Stunning 🌟</button> <button onclick="showThought('Enchanting 🪄', 'You cast a spell on me—one I never want to break')" class="small-btn">Enchanting 🪄</button> <button onclick="showThought('Kind 😇', 'Your gentle soul is more beautiful than any face could be')" class="small-btn">Kind 😇</button> <button onclick="showThought('Amazing 🌸', 'Everything you do, you do with such passion and care')" class="small-btn">Amazing 🌸</button> <button onclick="showThought('Graceful 💃', 'The way you move through life is like watching poetry in motion')" class="small-btn">Graceful 💃</button> <button onclick="showThought('Perfect 💎', 'You\'re not perfect, but you\'re perfect for me in every way')" class="small-btn">Perfect 💎</button> <button onclick="showThought('Precious 🎀', 'You\'re the greatest gift I could ever ask for')" class="small-btn">Precious 🎀</button> <button onclick="showThought('Magical 🧚', 'Being with you feels like living in a beautiful dream')" class="small-btn">Magical 🧚</button> <button onclick="showThought('Wonderful 🌷', 'You wonder me every day—I wonder how you\'re so incredible')" class="small-btn">Wonderful 🌷</button> <button onclick="showThought('Lovely 💗', 'Everything about you—inside and out—is absolutely lovely')" class="small-btn">Lovely 💗</button> <button onclick="showThought('Stunning 🦋', 'Like a butterfly, you\'ve transformed my life into something beautiful')" class="small-btn">Stunning 🦋</button>
    </div>
   </div><!-- Cute Words Section -->
   <div class="p-6 bg-white/5 rounded-2xl border border-white/10 mb-8">
    <h3 class="text-pink-200 font-bold mb-4 text-xl" style="font-family: 'Pacifico', cursive;">💖 More things she is: 💖</h3>
    <div class="text-white text-lg leading-relaxed space-y-2" style="font-family: 'Comfortaa', cursive;">
     <p><span class="cute-word" onclick="celebrateWord('Captivating', 'Your smile melts my heart and I can\'t look away')">Captivating</span>, <span class="cute-word" onclick="celebrateWord('Luminous', 'You light up my world like the sun')">luminous</span>, <span class="cute-word" onclick="celebrateWord('Breathtaking', 'You steal my breath away')">breathtaking</span></p>
     <p><span class="cute-word" onclick="celebrateWord('Elegant', 'So elegant, so graceful')">elegant</span>, <span class="cute-word" onclick="celebrateWord('Graceful', 'Pure elegance and grace')">graceful</span>, <span class="cute-word" onclick="celebrateWord('Alluring', 'You make my heart race')">alluring</span></p>
     <p><span class="cute-word" onclick="celebrateWord('Soulmate', 'You are my soulmate')">soulmate</span>, <span class="cute-word" onclick="celebrateWord('Angelic', 'My angel on earth')">angelic</span>, <span class="cute-word" onclick="celebrateWord('Delightful', 'You make me so happy')">delightful</span></p>
     <p><span class="cute-word" onclick="celebrateWord('Sweet', 'My sweet darling')">sweet</span>, <span class="cute-word" onclick="celebrateWord('Enchanting', 'Absolutely enchanting')">enchanting</span>, <span class="cute-word" onclick="celebrateWord('Radiant', 'The light of my life')">radiant</span></p>
    </div>
   </div><!-- Extra Features Section -->
   <div class="flex flex-col gap-3 mb-8"><button onclick="showOurStory()" class="bg-gradient-to-r from-purple-400 to-pink-400 hover:from-purple-500 hover:to-pink-500 border-none py-3 px-8 text-white rounded-full cursor-pointer transition-all duration-300 hover:scale-105 font-bold" style="font-family: 'Comfortaa', cursive; font-size: 16px;"> 📖 Our Love Story 📖 </button> <button onclick="showMemories()" class="bg-gradient-to-r from-blue-400 to-purple-400 hover:from-blue-500 hover:to-purple-500 border-none py-3 px-8 text-white rounded-full cursor-pointer transition-all duration-300 hover:scale-105 font-bold" style="font-family: 'Comfortaa', cursive; font-size: 16px;"> 💭 Our Memories 💭 </button> <button onclick="showReasons()" class="bg-gradient-to-r from-red-400 to-pink-400 hover:from-red-500 hover:to-pink-500 border-none py-3 px-8 text-white rounded-full cursor-pointer transition-all duration-300 hover:scale-105 font-bold" style="font-family: 'Comfortaa', cursive; font-size: 16px;"> 💓 Reasons I Love You 💓 </button> <button onclick="showFutureDreams()" class="bg-gradient-to-r from-yellow-400 to-orange-400 hover:from-yellow-500 hover:to-orange-500 border-none py-3 px-8 text-white rounded-full cursor-pointer transition-all duration-300 hover:scale-105 font-bold" style="font-family: 'Comfortaa', cursive; font-size: 16px;"> ✨ Our Future Dreams ✨ </button>
   </div>
  </div><!-- Photo Viewer -->
  <div id="viewer" onclick="closeViewer()" class="fixed inset-0 bg-black/90 viewer-overlay hidden justify-center items-center z-50 cursor-pointer">
   <div class="relative"><img id="viewerImg" class="max-w-[90vw] max-h-[85vh] rounded-2xl shadow-2xl" loading="lazy" onerror="console.error('Image failed to load:', this.src); this.style.background='linear-gradient(135deg, #ff7eb3, #ff758c)'; this.alt='Photo unavailable';">
    <div class="absolute -bottom-12 left-1/2 -translate-x-1/2 text-white/70 text-sm">
     Tap anywhere to close
    </div>
   </div>
  </div><!-- Slideshow Viewer -->
  <div id="slideshow" class="fixed inset-0 bg-black/95 viewer-overlay hidden z-50">
   <div class="slideshow-container"><button onclick="closeSlideshowViewer()" class="close-slideshow">✕</button>
    <div class="slide-counter"><span id="slideNumber">1</span> / <span id="slideTotalCount">4</span>
    </div>
    <div id="slidesWrapper" class="w-full h-full flex flex-col items-center justify-center relative"><!-- Slides will be generated by JavaScript -->
    </div>
    <div class="slideshow-controls"><button onclick="previousSlide()" class="slide-btn">❮</button> <button onclick="nextSlide()" class="slide-btn">❯</button>
    </div>
   </div>
  </div><!-- Love Popup -->
  <div id="lovePopup" class="fixed bottom-8 left-1/2 -translate-x-1/2 bg-gradient-to-r from-pink-500 to-rose-500 py-4 px-8 rounded-full text-white font-semibold shadow-xl hidden love-popup z-40"><span id="popupText">I Love You So Much 💖</span>
  </div><!-- Compliment Popup -->
  <div id="complimentPopup" class="fixed top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 bg-gradient-to-r from-pink-500 to-rose-500 py-6 px-8 rounded-2xl text-white font-semibold shadow-2xl hidden love-popup z-40 text-center"><span id="complimentText">You're absolutely gorgeous 😍</span>
  </div><!-- Special Message Modal -->
  <div id="specialModal" class="fixed inset-0 bg-black/80 viewer-overlay hidden justify-center items-center z-50 p-4">
   <div class="glass-card p-8 md:p-12 rounded-3xl text-center max-w-md relative"><button onclick="closeSpecialModal()" class="absolute top-4 right-4 text-white/60 hover:text-white text-2xl">✕</button>
    <div class="text-6xl mb-6">
     💌
    </div>
    <h2 class="text-2xl font-bold text-white mb-4" style="font-family: 'Pacifico', cursive;">To My Dearest 💕</h2>
    <p class="text-pink-100 leading-relaxed mb-6" style="font-family: 'Comfortaa', cursive;">Every moment with you is a treasure. Your smile lights up my world, and your love makes every day worth living. Here's to another year of beautiful memories together. You're my dream girl, my everything, and I'm so blessed to celebrate you today.</p>
    <p class="text-pink-300 text-lg font-semibold">Forever Yours 💗</p>
   </div>
  </div><!-- Our Love Story Modal -->
  <div id="storyModal" class="fixed inset-0 bg-black/80 viewer-overlay hidden justify-center items-center z-50 p-4 overflow-y-auto">
   <div class="glass-card p-8 md:p-12 rounded-3xl text-center max-w-2xl relative my-8"><button onclick="closeModal('storyModal')" class="absolute top-4 right-4 text-white/60 hover:text-white text-2xl">✕</button>
    <div class="text-6xl mb-6">
     📖
    </div>
    <h2 class="text-3xl font-bold text-white mb-6" style="font-family: 'Pacifico', cursive;">Our Love Story 💑</h2>
    <div class="text-pink-100 leading-relaxed space-y-4 text-left" style="font-family: 'Comfortaa', cursive;">
     <p>💫 <span class="text-white font-semibold">The Beginning:</span> Our love story began in the most unexpected way — online. But from that moment you came into my life, everything started feeling more real, more beautiful, and more meaningful.</p>
     <p>💕 <span class="text-white font-semibold">First Memories:</span> One of our most special memories was when we met for the first time at the Diwali mela. I was a little nervous… and you looked so beautiful, so pure, like the cutest little girl. The very next day, when we had our first kiss, it felt magical to me — a moment I will never forget.</p>
     <p>✨ <span class="text-white font-semibold">Growing Together:</span> With every passing day, I fall deeper in love with you. You've shown me what true love means, and how beautiful life can be when you have someone who truly understands you.</p>
     <p>🌹 <span class="text-white font-semibold">Forever Promise:</span> You're my soulmate, my best friend, my everything. I promise to love you with all my heart, through every season of life, forever and always.</p>
    </div>
   </div>
  </div><!-- Our Memories Modal -->
  <div id="memoriesModal" class="fixed inset-0 bg-black/80 viewer-overlay hidden justify-center items-center z-50 p-4 overflow-y-auto">
   <div class="glass-card p-8 md:p-12 rounded-3xl text-center max-w-2xl relative my-8"><button onclick="closeModal('memoriesModal')" class="absolute top-4 right-4 text-white/60 hover:text-white text-2xl">✕</button>
    <div class="text-6xl mb-6">
     💭
    </div>
    <h2 class="text-3xl font-bold text-white mb-6" style="font-family: 'Pacifico', cursive;">Our Precious Memories 🌹</h2>
    <div class="text-pink-100 leading-relaxed space-y-4 text-left">
     <div class="bg-white/10 p-4 rounded-xl border border-pink-400/30">
      <p class="text-white font-semibold mb-2">🌙 Midnight Conversations:</p>
      <p>Those late-night talks where we share our dreams, fears, and deepest thoughts. Your voice is the most comforting sound to me.</p>
     </div>
     <div class="bg-white/10 p-4 rounded-xl border border-pink-400/30">
      <p class="text-white font-semibold mb-2">🌅 Sunrise Moments:</p>
      <p>Waking up next to you, seeing the morning light on your face. These moments make me realize how grateful I am for you.</p>
     </div>
     <div class="bg-white/10 p-4 rounded-xl border border-pink-400/30">
      <p class="text-white font-semibold mb-2">🎵 Our Songs:</p>
      <p>Every song that reminds me of you, every moment we danced together. Music will never sound the same without you.</p>
     </div>
     <div class="bg-white/10 p-4 rounded-xl border border-pink-400/30">
      <p class="text-white font-semibold mb-2">🤭 Silly Moments:</p>
      <p>Your laughter, your jokes, the way you make me smile even on my worst days. You're my happiness personified.</p>
     </div>
    </div>
   </div>
  </div><!-- Reasons I Love You Modal -->
  <div id="reasonsModal" class="fixed inset-0 bg-black/80 viewer-overlay hidden justify-center items-center z-50 p-4 overflow-y-auto">
   <div class="glass-card p-8 md:p-12 rounded-3xl text-center max-w-2xl relative my-8"><button onclick="closeModal('reasonsModal')" class="absolute top-4 right-4 text-white/60 hover:text-white text-2xl">✕</button>
    <div class="text-6xl mb-6">
     💓
    </div>
    <h2 class="text-3xl font-bold text-white mb-6" style="font-family: 'Pacifico', cursive;">Reasons I Love You 🥰</h2>
    <div class="text-pink-100 leading-relaxed space-y-2 text-left" style="font-family: 'Comfortaa', cursive;">
     <p>💖 Your kindness—the way you care about everyone around you</p>
     <p>💖 Your strength and resilience in facing life's challenges</p>
     <p>💖 The way you listen to me and understand my heart</p>
     <p>💖 Your infectious laugh that brightens even the darkest days</p>
     <p>💖 Your ambition and the way you pursue your dreams</p>
     <p>💖 The tenderness in your touch and your warm embrace</p>
     <p>💖 Your intelligence and the depth of your thoughts</p>
     <p>💖 The way you love unconditionally and loyally</p>
     <p>💖 Your beauty—inside and out, every single day</p>
     <p>💖 The way you make me want to be a better person</p>
     <p>💖 Your sense of humor and how you make me laugh</p>
     <p>💖 The way you believe in me when I doubt myself</p>
     <p>💖 Your passion for life and everything you do</p>
     <p>💖 The way you hold my hand like it's the most precious thing</p>
     <p>💖 You. Just you. Everything about you, forever.</p>
    </div>
   </div>
  </div><!-- Our Future Dreams Modal -->
  <div id="dreamsModal" class="fixed inset-0 bg-black/80 viewer-overlay hidden justify-center items-center z-50 p-4 overflow-y-auto">
   <div class="glass-card p-8 md:p-12 rounded-3xl text-center max-w-2xl relative my-8"><button onclick="closeModal('dreamsModal')" class="absolute top-4 right-4 text-white/60 hover:text-white text-2xl">✕</button>
    <div class="text-6xl mb-6">
     ✨
    </div>
    <h2 class="text-3xl font-bold text-white mb-6" style="font-family: 'Pacifico', cursive;">Our Future Dreams 💫</h2>
    <div class="text-pink-100 leading-relaxed space-y-4 text-left" style="font-family: 'Comfortaa', cursive;">
     <p>🏡 <span class="text-white font-semibold">Our Home:</span> A cozy place filled with love, laughter, and memories where we build our life together.</p>
     <p>✈️ <span class="text-white font-semibold">Adventures:</span> Traveling the world, exploring new places, and creating unforgettable memories together around the globe.</p>
     <p>👨‍👩‍👧‍👦 <span class="text-white font-semibold">Family:</span> Growing old together, building a family filled with the same love and warmth we share, and watching our love story continue through generations.</p>
     <p>🌺 <span class="text-white font-semibold">Everyday Magic:</span> Growing old together, holding hands through it all, and still feeling butterflies when I see you after 50 years.</p>
     <p>💑 <span class="text-white font-semibold">Forever:</span> A lifetime of love, support, dreams, and growth. I want to wake up next to you every morning and fall asleep beside you every night, forever.</p>
     <p class="text-pink-300 text-lg font-semibold mt-6">🎀 This is just the beginning of our beautiful forever story! 🎀</p>
    </div>
   </div>
  </div>
  <script>
// Default configuration
const defaultConfig = {
  main_title: "Happy Birthday My Love ❤️",
  love_message: "You are my happiness, my forever.",
  popup_message: "I Love You So Much 💖",
  primary_color: "#ff7eb3",
  background_color: "#0f172a",
  text_color: "#ffffff",
  accent_color: "#ff758c",
  font_family: "Quicksand"
};

let config = { ...defaultConfig };

// Cute soft toy plushies with thoughts
const photos = [
  { url: "https://images.unsplash.com/photo-1590080876614-bc517ee5a48c?w=300&h=400&fit=crop", thought: "I'm thinking of you 🥰" },
  { url: "https://images.unsplash.com/photo-1577720643272-265f434d7ba0?w=300&h=400&fit=crop", thought: "Missing your cuddles 💕" },
  { url: "https://images.unsplash.com/photo-1559027615-cd4628902d4a?w=300&h=400&fit=crop", thought: "Forever yours 💗" },
  { url: "https://images.unsplash.com/photo-1585399818219-39ae332b7e9b?w=300&h=400&fit=crop", thought: "You're my favorite 🎀" }
];

const loveMessages = [
  "I Love You So Much 💖",
  "You Mean Everything To Me 💕",
  "Forever & Always 💗",
  "My Heart Is Yours 💝",
  "You Are My Sunshine ☀️",
  "Best Birthday Person Ever 🎉",
  "You Make Me So Happy 😊",
  "My Favorite Human 💜",
  "You're My Everything 🌹",
  "Always In My Heart 💓"
];

let photoInterval, heartInterval, petalInterval;

// Initialize Element SDK
if (window.elementSdk) {
  window.elementSdk.init({
    defaultConfig,
    onConfigChange: async (newConfig) => {
      config = { ...defaultConfig, ...newConfig };
      
      // Update text content
      const mainTitle = document.getElementById('mainTitle');
      const loveMessage = document.getElementById('loveMessage');
      
      if (mainTitle) mainTitle.textContent = config.main_title || defaultConfig.main_title;
      if (loveMessage) loveMessage.textContent = config.love_message || defaultConfig.love_message;
      
      // Update colors
      document.body.style.background = `linear-gradient(180deg, ${config.background_color} 0%, #1e1b4b 50%, #312e81 100%)`;
      
      // Update font
      const fontFamily = config.font_family || defaultConfig.font_family;
      document.body.style.fontFamily = `${fontFamily}, sans-serif`;
    },
    mapToCapabilities: (cfg) => ({
      recolorables: [
        {
          get: () => cfg.background_color || defaultConfig.background_color,
          set: (value) => {
            cfg.background_color = value;
            window.elementSdk.setConfig({ background_color: value });
          }
        },
        {
          get: () => cfg.primary_color || defaultConfig.primary_color,
          set: (value) => {
            cfg.primary_color = value;
            window.elementSdk.setConfig({ primary_color: value });
          }
        },
        {
          get: () => cfg.text_color || defaultConfig.text_color,
          set: (value) => {
            cfg.text_color = value;
            window.elementSdk.setConfig({ text_color: value });
          }
        }
      ],
      borderables: [],
      fontEditable: {
        get: () => cfg.font_family || defaultConfig.font_family,
        set: (value) => {
          cfg.font_family = value;
          window.elementSdk.setConfig({ font_family: value });
        }
      },
      fontSizeable: undefined
    }),
    mapToEditPanelValues: (cfg) => new Map([
      ["main_title", cfg.main_title || defaultConfig.main_title],
      ["love_message", cfg.love_message || defaultConfig.love_message],
      ["popup_message", cfg.popup_message || defaultConfig.popup_message]
    ])
  });
}

function openSite() {
  document.getElementById('start').classList.add('hidden');
  document.getElementById('main').classList.remove('hidden');
  startPhotos();
  startHearts();
  startPetals();
  createSparkles();
}

// Floating Photos
function startPhotos() {
  createPhoto();
  photoInterval = setInterval(createPhoto, 2500);
}

function createPhoto() {
  const photoObj = photos[Math.floor(Math.random() * photos.length)];
  const img = document.createElement('img');
  img.src = photoObj.url;
  img.className = 'photo';
  img.style.left = Math.random() * 80 + 5 + '%';
  img.style.top = '100%';
  img.style.animationDuration = (Math.random() * 8 + 10) + 's';
  img.title = photoObj.thought;
  img.onclick = (e) => {
    e.stopPropagation();
    openViewer(photoObj.url, photoObj.thought);
  };
  img.onerror = function() {
    this.style.background = 'linear-gradient(135deg, #ff7eb3, #ff758c)';
    this.alt = 'Photo unavailable';
  };
  img.loading = 'lazy';
  document.body.appendChild(img);
  setTimeout(() => img.remove(), 18000);
}

// Viewer
function openViewer(src, thought) {
  const viewer = document.getElementById('viewer');
  const viewerImg = document.getElementById('viewerImg');
  viewer.style.display = 'flex';
  viewerImg.src = src;
  
  // Display thought bubble
  let thoughtBubble = document.getElementById('thoughtBubble');
  if (!thoughtBubble) {
    thoughtBubble = document.createElement('div');
    thoughtBubble.id = 'thoughtBubble';
    thoughtBubble.style.cssText = `
      position: absolute;
      bottom: -60px;
      left: 50%;
      transform: translateX(-50%);
      background: linear-gradient(135deg, #ff7eb3, #ff758c);
      color: white;
      padding: 12px 20px;
      border-radius: 20px;
      font-weight: 600;
      white-space: nowrap;
      box-shadow: 0 8px 20px rgba(255, 118, 170, 0.4);
      font-family: 'Pacifico', cursive;
      font-size: 16px;
    `;
    viewer.appendChild(thoughtBubble);
  }
  thoughtBubble.textContent = thought;
}

function closeViewer() {
  document.getElementById('viewer').style.display = 'none';
}

// Floating Hearts
function startHearts() {
  createHeart();
  heartInterval = setInterval(createHeart, 800);
}

function createHeart() {
  const hearts = ['💖', '💕', '💗', '💝', '💜', '🩷', '❤️', '🤍'];
  const heart = document.createElement('div');
  heart.innerHTML = hearts[Math.floor(Math.random() * hearts.length)];
  heart.className = 'heart';
  heart.style.left = Math.random() * 95 + '%';
  heart.style.top = '100%';
  heart.style.fontSize = (Math.random() * 20 + 16) + 'px';
  heart.style.animationDuration = (Math.random() * 4 + 5) + 's';
  heart.onclick = (e) => {
    e.stopPropagation();
    createHeartBurst(e.clientX, e.clientY);
    heart.remove();
  };
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 9000);
}

function createHeartBurst(x, y) {
  for (let i = 0; i < 5; i++) {
    const burst = document.createElement('div');
    burst.innerHTML = '💖';
    burst.className = 'heart-burst';
    burst.style.left = (x + (Math.random() - 0.5) * 50) + 'px';
    burst.style.top = (y + (Math.random() - 0.5) * 50) + 'px';
    document.body.appendChild(burst);
    setTimeout(() => burst.remove(), 800);
  }
}

// Petals
function startPetals() {
  createPetal();
  petalInterval = setInterval(createPetal, 600);
}

function createPetal() {
  const petals = ['🌸', '🌺', '🌷', '💮', '🪷'];
  const petal = document.createElement('div');
  petal.innerHTML = petals[Math.floor(Math.random() * petals.length)];
  petal.className = 'petal';
  petal.style.left = Math.random() * 100 + '%';
  petal.style.top = '-50px';
  petal.style.fontSize = (Math.random() * 15 + 12) + 'px';
  petal.style.animationDuration = (Math.random() * 5 + 8) + 's';
  document.body.appendChild(petal);
  setTimeout(() => petal.remove(), 13000);
}

// Sparkles
function createSparkles() {
  setInterval(() => {
    const sparkle = document.createElement('div');
    sparkle.className = 'sparkle';
    sparkle.style.left = Math.random() * 100 + '%';
    sparkle.style.top = Math.random() * 100 + '%';
    document.body.appendChild(sparkle);
    setTimeout(() => sparkle.remove(), 1000);
  }, 300);
}

// Show Love Popup
function showLove() {
  const popup = document.getElementById('lovePopup');
  const popupText = document.getElementById('popupText');
  const message = config.popup_message || loveMessages[Math.floor(Math.random() * loveMessages.length)];
  
  popupText.textContent = message;
  popup.classList.remove('hidden');
  popup.style.animation = 'none';
  popup.offsetHeight;
  popup.style.animation = 'popIn 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55)';
  
  // Create celebration effect
  for (let i = 0; i < 10; i++) {
    setTimeout(() => {
      createHeartBurst(
        window.innerWidth / 2 + (Math.random() - 0.5) * 200,
        window.innerHeight / 2 + (Math.random() - 0.5) * 200
      );
    }, i * 100);
  }
  
  // Open slideshow after celebration
  setTimeout(() => {
    popup.classList.add('hidden');
    openSlideshowViewer();
  }, 2500);
}

// Show Personalized Thought
function showThought(title, thought) {
  const popup = document.getElementById('complimentPopup');
  const complimentText = document.getElementById('complimentText');
  
  complimentText.innerHTML = `<div style="font-size: 18px; font-weight: 600; margin-bottom: 8px;">${title}</div><div style="font-size: 14px; font-weight: 400; line-height: 1.5;">"${thought}"</div>`;
  popup.classList.remove('hidden');
  popup.style.animation = 'none';
  popup.style.maxWidth = '320px';
  popup.offsetHeight;
  popup.style.animation = 'popIn 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55)';
  
  // Create celebration effect
  for (let i = 0; i < 8; i++) {
    setTimeout(() => {
      createHeartBurst(
        window.innerWidth / 2 + (Math.random() - 0.5) * 150,
        window.innerHeight / 2 + (Math.random() - 0.5) * 150
      );
    }, i * 80);
  }
  
  setTimeout(() => {
    popup.classList.add('hidden');
    popup.style.maxWidth = 'auto';
  }, 3500);
}

// Celebrate Word
function celebrateWord(title, message) {
  const popup = document.getElementById('complimentPopup');
  const complimentText = document.getElementById('complimentText');
  
  complimentText.innerHTML = `<div style="font-size: 18px; font-weight: 600; margin-bottom: 8px;">${title} 💕</div><div style="font-size: 14px; font-weight: 400; line-height: 1.5;">"${message}"</div>`;
  popup.classList.remove('hidden');
  popup.style.animation = 'none';
  popup.style.maxWidth = '320px';
  popup.offsetHeight;
  popup.style.animation = 'popIn 0.5s cubic-bezier(0.68, -0.55, 0.265, 1.55)';
  
  // Create celebration effect
  for (let i = 0; i < 6; i++) {
    setTimeout(() => {
      createHeartBurst(
        window.innerWidth / 2 + (Math.random() - 0.5) * 100,
        window.innerHeight / 3 + (Math.random() - 0.5) * 100
      );
    }, i * 60);
  }
  
  setTimeout(() => {
    popup.classList.add('hidden');
    popup.style.maxWidth = 'auto';
  }, 2200);
}

// Special Message Modal
function showSpecialMessage() {
  document.getElementById('specialModal').style.display = 'flex';
}

function closeSpecialModal() {
  document.getElementById('specialModal').style.display = 'none';
}

// Generic Modal Closer
function closeModal(modalId) {
  document.getElementById(modalId).style.display = 'none';
}

// Show Love Story
function showOurStory() {
  document.getElementById('storyModal').style.display = 'flex';
  createCelebrationHearts();
}

// Show Memories
function showMemories() {
  document.getElementById('memoriesModal').style.display = 'flex';
  createCelebrationHearts();
}

// Show Reasons
function showReasons() {
  document.getElementById('reasonsModal').style.display = 'flex';
  createCelebrationHearts();
}

// Show Future Dreams
function showFutureDreams() {
  document.getElementById('dreamsModal').style.display = 'flex';
  createCelebrationHearts();
}

// Create Celebration Hearts
function createCelebrationHearts() {
  for (let i = 0; i < 12; i++) {
    setTimeout(() => {
      createHeartBurst(
        Math.random() * window.innerWidth,
        Math.random() * window.innerHeight
      );
    }, i * 100);
  }
}

// Close modal on background click
document.addEventListener('click', (e) => {
  if (e.target.id === 'storyModal' || e.target.id === 'memoriesModal' || e.target.id === 'reasonsModal' || e.target.id === 'dreamsModal') {
    closeModal(e.target.id);
  }
  if (e.target.id === 'specialModal') {
    closeSpecialModal();
  }
});

// Keyboard support
document.addEventListener('keydown', (e) => {
  if (e.key === 'Escape') {
    closeViewer();
    closeSpecialModal();
    closeSlideshowViewer();
  }
  if (e.key === 'ArrowLeft') {
    previousSlide();
  }
  if (e.key === 'ArrowRight') {
    nextSlide();
  }
});

// Slideshow Variables
let currentSlideIndex = 0;
let slides = [];

// Open Slideshow
function openSlideshowViewer() {
  const slideshow = document.getElementById('slideshow');
  const slidesWrapper = document.getElementById('slidesWrapper');
  
  // Clear previous slides
  slidesWrapper.innerHTML = '';
  slides = [];
  
  // Create slides for each photo
  photos.forEach((photoObj, index) => {
    const slide = document.createElement('div');
    slide.className = 'slide';
    if (index === 0) slide.classList.add('active');
    
    const img = document.createElement('img');
    img.src = photoObj.url;
    img.loading = 'lazy';
    img.onerror = function() {
      this.style.background = 'linear-gradient(135deg, #ff7eb3, #ff758c)';
      this.alt = 'Photo unavailable';
    };
    
    slide.appendChild(img);
    
    // Add thought bubble
    const thoughtBubble = document.createElement('div');
    thoughtBubble.className = 'slide-thought';
    thoughtBubble.textContent = photoObj.thought;
    thoughtBubble.style.cssText = `
      position: absolute;
      bottom: 100px;
      left: 50%;
      transform: translateX(-50%);
      background: linear-gradient(135deg, #ff7eb3, #ff758c);
      color: white;
      padding: 12px 20px;
      border-radius: 20px;
      font-weight: 600;
      font-family: 'Pacifico', cursive;
      font-size: 18px;
      box-shadow: 0 8px 20px rgba(255, 118, 170, 0.4);
      animation: slideThoughtIn 0.8s ease-in-out;
      z-index: 10;
    `;
    slide.appendChild(thoughtBubble);
    
    slidesWrapper.appendChild(slide);
    slides.push(slide);
  });
  
  // Update counter
  document.getElementById('slideTotalCount').textContent = photos.length;
  currentSlideIndex = 0;
  updateSlideNumber();
  
  slideshow.classList.remove('hidden');
  
  // Add floating hearts around slideshow
  createSlideshowHearts();
}

// Close Slideshow
function closeSlideshowViewer() {
  document.getElementById('slideshow').classList.add('hidden');
}

// Next Slide
function nextSlide() {
  if (slides.length === 0) return;
  
  slides[currentSlideIndex].classList.remove('active');
  currentSlideIndex = (currentSlideIndex + 1) % slides.length;
  slides[currentSlideIndex].classList.add('active');
  
  updateSlideNumber();
  createSlideshowHearts();
}

// Previous Slide
function previousSlide() {
  if (slides.length === 0) return;
  
  slides[currentSlideIndex].classList.remove('active');
  currentSlideIndex = (currentSlideIndex - 1 + slides.length) % slides.length;
  slides[currentSlideIndex].classList.add('active');
  
  updateSlideNumber();
  createSlideshowHearts();
}

// Update Slide Number
function updateSlideNumber() {
  document.getElementById('slideNumber').textContent = currentSlideIndex + 1;
}

// Create Floating Hearts Around Slideshow
function createSlideshowHearts() {
  const wrapper = document.getElementById('slidesWrapper');
  
  // Remove old hearts
  const oldHearts = wrapper.querySelectorAll('.slideshow-heart');
  oldHearts.forEach(heart => heart.remove());
  
  // Create new hearts
  const hearts = ['💖', '💕', '💗', '💝', '🩷'];
  const positions = [
    { top: '10%', left: '5%', delay: '0s' },
    { top: '10%', right: '5%', delay: '0.5s' },
    { bottom: '15%', left: '8%', delay: '1s' },
    { bottom: '15%', right: '8%', delay: '1.5s' },
    { top: '50%', left: '2%', delay: '0.3s' },
    { top: '50%', right: '2%', delay: '0.8s' }
  ];
  
  positions.forEach((pos, index) => {
    const heart = document.createElement('div');
    heart.className = 'slideshow-heart';
    heart.innerHTML = hearts[index % hearts.length];
    heart.style.top = pos.top || 'auto';
    heart.style.bottom = pos.bottom || 'auto';
    heart.style.left = pos.left || 'auto';
    heart.style.right = pos.right || 'auto';
    heart.style.animationDelay = pos.delay;
    wrapper.appendChild(heart);
  });
}
</script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9cb32b95d48cefc3',t:'MTc3MDYzODA0OC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
