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
  <div id="main" class="glass-card p-10 md:p-14 rounded-3xl text-center max-w-lg mx-4 z-20 relative hidden">
   <div class="text-5xl mb-4">
    🎂
   </div>
   <h1 id="mainTitle" class="title-glow text-3xl md:text-4xl font-bold text-white mb-6" style="font-family: 'Playfair Display', serif;">Happy Birthday My Love ❤️</h1>
   <p id="loveMessage" class="text-pink-100 text-xl mb-8 leading-relaxed">You are my happiness, my forever.</p>
   <div class="flex flex-col gap-4"><button onclick="showLove()" class="cute-btn border-none py-4 px-10 text-lg text-white rounded-full cursor-pointer shadow-lg"> Tap For Love 💕 </button> <button onclick="showSpecialMessage()" class="bg-white/20 hover:bg-white/30 border border-white/30 py-3 px-8 text-white rounded-full cursor-pointer transition-all duration-300 hover:scale-105"> Special Message 💌 </button>
   </div>
  </div><!-- Photo Viewer -->
  <div id="viewer" onclick="closeViewer()" class="fixed inset-0 bg-black/90 viewer-overlay hidden justify-center items-center z-50 cursor-pointer">
   <div class="relative"><img id="viewerImg" class="max-w-[90vw] max-h-[85vh] rounded-2xl shadow-2xl">
    <div class="absolute -bottom-12 left-1/2 -translate-x-1/2 text-white/70 text-sm">
     Tap anywhere to close
    </div>
   </div>
  </div><!-- Love Popup -->
  <div id="lovePopup" class="fixed bottom-8 left-1/2 -translate-x-1/2 bg-gradient-to-r from-pink-500 to-rose-500 py-4 px-8 rounded-full text-white font-semibold shadow-xl hidden love-popup z-40"><span id="popupText">I Love You So Much 💖</span>
  </div><!-- Special Message Modal -->
  <div id="specialModal" class="fixed inset-0 bg-black/80 viewer-overlay hidden justify-center items-center z-50 p-4">
   <div class="glass-card p-8 md:p-12 rounded-3xl text-center max-w-md relative"><button onclick="closeSpecialModal()" class="absolute top-4 right-4 text-white/60 hover:text-white text-2xl">✕</button>
    <div class="text-6xl mb-6">
     💌
    </div>
    <h2 class="text-2xl font-bold text-white mb-4" style="font-family: 'Playfair Display', serif;">To My Dearest</h2>
    <p class="text-pink-100 leading-relaxed mb-6">Every moment with you is a treasure. Your smile lights up my world, and your love makes every day worth living. Here's to another year of beautiful memories together.</p>
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
  "https://drive.google.com/file/d/1RGVfOv7FJq7FGnRphD74NI8xc5vbBJmW/view?usp=sharing",
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
  "Best Birthday Person Ever 🎂",
  "You Make Me So Happy 😊",
  "My Favorite Human 💜"
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
  popup.offsetHeight; // Trigger reflow
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
  
  setTimeout(() => {
    popup.classList.add('hidden');
  }, 3000);
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
  }
});
</script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9c9d890031f789e1',t:'MTc3MDQxMTE4Ny4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
