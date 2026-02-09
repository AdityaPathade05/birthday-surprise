<!doctype html>
<html lang="en" class="h-full">
 <head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday My Love</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="/_sdk/element_sdk.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&amp;family=Quicksand:wght@400;500;600&amp;display=swap" rel="stylesheet">
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
    radial-gradient(#ffffff 1px, transparent 1px),
    radial-gradient(#ffffff88 1px, transparent 1px);
  background-size: 50px 50px, 30px 30px;
  background-position: 0 0, 25px 25px;
  opacity: 0.3;
  animation: twinkle 4s ease-in-out infinite alternate;
  pointer-events: none;
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

@keyframes floatAroundSlideshow {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}

</style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body class="h-full m-0 overflow-hidden flex justify-center items-center starfield" style="font-family: 'Quicksand', sans-serif; background: linear-gradient(180deg, #0f172a 0%, #1e1b4b 50%, #312e81 100%);"><!-- Start Screen -->
  <div id="start" class="glass-card p-10 md:p-12 rounded-3xl text-center max-w-md mx-4 z-20 relative">
   <div class="text-6xl mb-6 animate-bounce">
    💝
   </div>
   <h1 class="text-3xl md:text-4xl font-bold text-white mb-4" style="font-family: 'Playfair Display', serif;">Birthday Surprise</h1>
   <p class="text-pink-200 mb-8 text-lg">A special gift awaits you...</p><button onclick="openSite()" class="cute-btn border-none py-4 px-10 text-lg text-white rounded-full cursor-pointer shadow-lg"> Open Your Surprise ✨ </button>
  </div><!-- Main Content -->
  <div id="main" class="glass-card p-8 md:p-12 rounded-3xl text-center max-w-2xl mx-4 z-20 relative hidden overflow-y-auto max-h-[90vh]">
   <div class="text-5xl mb-4">
    🎂
   </div>
   <h1 id="mainTitle" class="title-glow text-3xl md:text-4xl font-bold text-white mb-4" style="font-family: 'Playfair Display', serif;">Happy Birthday My Love ❤️</h1>
   <p id="loveMessage" class="text-pink-100 text-lg mb-6 leading-relaxed">You are my happiness, my forever.</p><!-- Main Action Buttons -->
   <div class="flex flex-col gap-4 mb-8"><button onclick="showLove()" class="cute-btn border-none py-4 px-10 text-lg text-white rounded-full cursor-pointer shadow-lg"> Tap For Love 💕 </button> <button onclick="showSpecialMessage()" class="bg-white/20 hover:bg-white/30 border border-white/30 py-3 px-8 text-white rounded-full cursor-pointer transition-all duration-300 hover:scale-105"> Special Message 💌 </button>
   </div><!-- Interactive Buttons Grid -->
   <div class="mb-8 p-6 bg-white/5 rounded-2xl border border-white/10">
    <h3 class="text-pink-300 font-semibold mb-4 text-lg">Click to see my thoughts behind these words 👇</h3>
    <div class="button-grid"><button onclick="showThought('Beautiful 💫', 'Your beauty isn\'t just what I see—it\'s the way you light up every room you enter')" class="small-btn">Beautiful 💫</button> <button onclick="showThought('Elegant 👑', 'The grace with which you carry yourself is absolutely captivating')" class="small-btn">Elegant 👑</button> <button onclick="showThought('Gorgeous 😍', 'Every time I look at you, I wonder how I got so lucky')" class="small-btn">Gorgeous 😍</button> <button onclick="showThought('Charming 💕', 'Your charm could win over anyone—but I\'m the one who gets to keep you')" class="small-btn">Charming 💕</button> <button onclick="showThought('Radiant ✨', 'You glow with a light that makes the world brighter')" class="small-btn">Radiant ✨</button> <button onclick="showThought('Stunning 🌟', 'You take my breath away every single day')" class="small-btn">Stunning 🌟</button> <button onclick="showThought('Enchanting 🪄', 'You cast a spell on me—one I never want to break')" class="small-btn">Enchanting 🪄</button> <button onclick="showThought('Kind 😇', 'Your gentle soul is more beautiful than any face could be')" class="small-btn">Kind 😇</button> <button onclick="showThought('Amazing 🌸', 'Everything you do, you do with such passion and care')" class="small-btn">Amazing 🌸</button> <button onclick="showThought('Graceful 💃', 'The way you move through life is like watching poetry in motion')" class="small-btn">Graceful 💃</button> <button onclick="showThought('Perfect 💎', 'You\'re not perfect, but you\'re perfect for me in every way')" class="small-btn">Perfect 💎</button> <button onclick="showThought('Precious 🎀', 'You\'re the greatest gift I could ever ask for')" class="small-btn">Precious 🎀</button> <button onclick="showThought('Magical 🧚', 'Being with you feels like living in a beautiful dream')" class="small-btn">Magical 🧚</button> <button onclick="showThought('Wonderful 🌷', 'You wonder me every day����I wonder how you\'re so incredible')" class="small-btn">Wonderful 🌷</button> <button onclick="showThought('Lovely 💗', 'Everything about you—inside and out—is absolutely lovely')" class="small-btn">Lovely 💗</button> <button onclick="showThought('Stunning 🦋', 'Like a butterfly, you\'ve transformed my life into something beautiful')" class="small-btn">Stunning 🦋</button>
    </div>
   </div><!-- Cute Words Section -->
   <div class="p-6 bg-white/5 rounded-2xl border border-white/10">
    <h3 class="text-pink-300 font-semibold mb-4">More things she is:</h3>
    <div class="text-white text-lg leading-relaxed space-y-2">
     <p><span class="cute-word" onclick="celebrateWord('Captivating', 'Your smile melts my heart and I can\'t look away')">Captivating</span>, <span class="cute-word" onclick="celebrateWord('Luminous', 'You light up my world like the sun')">luminous</span>, <span class="cute-word" onclick="celebrateWord('Breathtaking', 'You steal my breath away')">breathtaking</span></p>
     <p><span class="cute-word" onclick="celebrateWord('Elegant', 'So elegant, so graceful')">elegant</span>, <span class="cute-word" onclick="celebrateWord('Graceful', 'Pure elegance and grace')">graceful</span>, <span class="cute-word" onclick="celebrateWord('Alluring', 'You make my heart race')">alluring</span></p>
     <p><span class="cute-word" onclick="celebrateWord('Soulmate', 'You are my soulmate')">soulmate</span>, <span class="cute-word" onclick="celebrateWord('Angelic', 'My angel on earth')">angelic</span>, <span class="cute-word" onclick="celebrateWord('Delightful', 'You make me so happy')">delightful</span></p>
     <p><span class="cute-word" onclick="celebrateWord('Sweet', 'My sweet darling')">sweet</span>, <span class="cute-word" onclick="celebrateWord('Enchanting', 'Absolutely enchanting')">enchanting</span>, <span class="cute-word" onclick="celebrateWord('Radiant', 'The light of my life')">radiant</span></p>
    </div>
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
    <h2 class="text-2xl font-bold text-white mb-4" style="font-family: 'Playfair Display', serif;">To My Dearest</h2>
    <p class="text-pink-100 leading-relaxed mb-6">Every moment with you is a treasure. Your smile lights up my world, and your love makes every day worth living. Here's to another year of beautiful memories together. You're my dream girl, my everything, and I'm so blessed to celebrate you today.</p>
    <p class="text-pink-300 text-lg font-semibold">Forever Yours 💗</p>
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

// Sample photos - replace with your own
const photos = [
  "https://raw.githubusercontent.com/AdityaPathade05/birthday-surprise/main/IMG-20250921-WA0041.jpg
",
  "https://images.unsplash.com/photo-1516589178581-6cd7833ae3b2?w=300&h=400&fit=crop",
  "https://images.unsplash.com/photo-1529333166437-7750a6dd5a70?w=300&h=400&fit=crop",
  "https://images.unsplash.com/photo-1522673607200-164d1b6ce486?w=300&h=400&fit=crop"
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
  const img = document.createElement('img');
  img.src = photos[Math.floor(Math.random() * photos.length)];
  img.className = 'photo';
  img.style.left = Math.random() * 80 + 5 + '%';
  img.style.top = '100%';
  img.style.animationDuration = (Math.random() * 8 + 10) + 's';
  img.onclick = (e) => {
    e.stopPropagation();
    openViewer(img.src);
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
function openViewer(src) {
  const viewer = document.getElementById('viewer');
  const viewerImg = document.getElementById('viewerImg');
  viewer.style.display = 'flex';
  viewerImg.src = src;
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

// Close modal on background click
document.getElementById('specialModal').addEventListener('click', (e) => {
  if (e.target === document.getElementById('specialModal')) {
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
  photos.forEach((photoUrl, index) => {
    const slide = document.createElement('div');
    slide.className = 'slide';
    if (index === 0) slide.classList.add('active');
    
    const img = document.createElement('img');
    img.src = photoUrl;
    img.loading = 'lazy';
    img.onerror = function() {
      this.style.background = 'linear-gradient(135deg, #ff7eb3, #ff758c)';
      this.alt = 'Photo unavailable';
    };
    
    slide.appendChild(img);
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
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9c9db734d29189e1',t:'MTc3MDQxMzA4MC4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
