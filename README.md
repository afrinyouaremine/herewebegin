<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>THE REAL LOVE STORY</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Great+Vibes&family=Parisienne&display=swap');

body{
  margin:0;
  font-family:'Segoe UI', sans-serif;
  background: 
    /* Romantic heart particles */
    radial-gradient(circle at 20% 80%, rgba(255,182,193,0.3) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, rgba(255,105,180,0.25) 0%, transparent 50%),
    radial-gradient(circle at 40% 40%, rgba(255,20,147,0.2) 0%, transparent 50%),
    radial-gradient(circle at 60% 60%, rgba(255,192,203,0.25) 0%, transparent 50%),
    
    /* Romantic gradient base */
    linear-gradient(135deg, #ff9a9e 0%, #fecfef 25%, #fecfef 50%, #fad0c4 75%, #ffd1ff 100%),
    
    /* Soft romantic overlay */
    linear-gradient(45deg, rgba(255,182,193,0.4) 0%, rgba(255,105,180,0.3) 30%, rgba(255,20,147,0.2) 70%, rgba(255,192,203,0.3) 100%);
  
  color:#4a1a4a;
  overflow-x:hidden;
  position:relative;
  
  /* Smooth heartBeat animation */
  animation: heartBeat 25s ease-in-out infinite;
}

@keyframes heartBeat {
  0%, 100% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
}

.page{
  min-height:100vh;
  padding:25px 20px;
  text-align:center;
  opacity:0;
  transform:translateY(50px);
  transition:all 1s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  position:relative;
  z-index:2;
}
.show{
  opacity:1;
  transform:translateY(0);
}

/* Acrylic glass effect */
.acrylic-card{
  backdrop-filter: blur(30px) saturate(180%);
  background: rgba(255,255,255,0.25);
  border-radius:40px;
  padding:40px 35px;
  margin:20px auto;
  max-width:95vw;
  width:100%;
  box-shadow:0 30px 80px rgba(255,105,180,0.4), 0 0 0 1px rgba(255,182,193,0.6), inset 0 1px 0 rgba(255,255,255,0.9);
  border:1px solid rgba(255,192,203,0.8);
  animation:acrylicBloom 1.5s cubic-bezier(0.23,1,0.32,1);
  position:relative;
  overflow:hidden;
  box-sizing:border-box;
}

.acrylic-card::before{
  content:'💖';
  position:absolute;
  top:-25px; right:-25px;
  font-size:45px;
  opacity:0.12;
  animation: floatHeart 8s infinite linear;
  z-index:0;
}

.acrylic-card::after{
  content:'✨';
  position:absolute;
  bottom:15px; left:15px;
  font-size:25px;
  opacity:0.4;
  animation: sparkle 4s infinite;
}

@keyframes acrylicBloom{
  0%{ 
    transform:scale(0.6) rotateX(20deg) translateY(30px); 
    opacity:0; 
    filter:blur(8px);
  }
  100%{ 
    transform:scale(1) rotateX(0deg) translateY(0); 
    opacity:1; 
    filter:blur(0px);
  }
}

/* Beautiful handwritten fonts */
.hero-title{
  font-family: 'Dancing Script', cursive;
  font-weight: 700;
  font-size:clamp(32px, 7vw, 42px);
  letter-spacing:3px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#ff1493,#ff69b4,#ffb6c1,#ff1493);
  background-size:300% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shimmer 4s linear infinite;
  position:relative;
  margin-bottom:30px;
  text-shadow:0 0 25px rgba(255,105,180,0.6);
  line-height:1.2;
}

h2{
  font-family: 'Parisienne', cursive;
  font-size:clamp(26px, 6.5vw, 34px);
  color:#8b008b;
  margin-bottom:20px;
}
h3{
  font-family: 'Great Vibes', cursive;
  font-size:clamp(24px, 5.5vw, 30px);
  color:#c71585;
  margin-bottom:25px;
}

/* Handwritten paragraph style */
.handwritten {
  font-family: 'Dancing Script', cursive;
  font-weight: 400;
  font-size:clamp(16px, 4.5vw, 19px) !important;
  line-height:1.8 !important;
  margin-bottom:22px !important;
  color:#4a1a4a !important;
  text-align:left !important;
  position:relative;
}

.handwritten::before {
  content: '';
  position: absolute;
  left: -10px;
  top: 0;
  width: 4px;
  height: 100%;
  background: linear-gradient(to bottom, transparent, #ff69b4, transparent);
  opacity: 0.3;
}

.card p {
  hyphens:auto;
  word-wrap:break-word;
}

input{
  padding:20px;
  width:92%;
  max-width:450px;
  border:2px solid rgba(255,182,193,0.7);
  border-radius:30px;
  margin:20px auto;
  display:block;
  background:rgba(255,255,255,0.92);
  color:#4a1a4a;
  outline:none;
  transition:all 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  font-size:clamp(17px, 4.2vw, 20px);
  font-family: 'Dancing Script', cursive;
  box-sizing:border-box;
  box-shadow:0 6px 20px rgba(255,105,180,0.3);
}
input::placeholder{
  color:rgba(139,0,139,0.7);
  font-family: 'Dancing Script', cursive;
}
input:focus{
  box-shadow:0 0 35px rgba(255,105,180,0.7), 0 10px 30px rgba(255,20,147,0.4);
  transform:scale(1.02) translateY(-2px);
  border-color:rgba(255,20,147,0.9);
  background:rgba(255,255,255,0.97);
}

button{
  margin:15px 10px;
  padding:20px 45px;
  min-height:60px;
  border:none;
  border-radius:35px;
  background:linear-gradient(45deg,#ff1493,#ff69b4,#ffb6c1);
  color:white;
  font-weight:700;
  cursor:pointer;
  font-size:clamp(17px, 4.2vw, 20px);
  font-family: 'Dancing Script', cursive;
  position:relative;
  overflow:hidden;
  transition:all 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
  display:inline-block;
  touch-action:manipulation;
  box-shadow:0 8px 25px rgba(255,105,180,0.5);
}
button::before{
  content:'';
  position:absolute;
  top:0; left:-100%;
  width:100%; height:100%;
  background:linear-gradient(90deg,transparent,rgba(255,255,255,0.6),transparent);
  transition:0.7s;
}
button:hover, button:active{
  transform:scale(1.08) translateY(-4px);
  box-shadow:0 15px 40px rgba(255,105,180,0.7);
}
button:active{
  transform:scale(0.98);
}

/* Enhanced romantic blobs */
.blob{
  position:fixed;
  border-radius:50% 0 50% 0;
  filter:blur(12px);
  animation:floatHeartBlob 30s infinite ease-in-out;
  z-index:-1;
  opacity:0.7;
}
.blob1{ 
  width:300px; height:300px; 
  background:linear-gradient(45deg, rgba(255,182,193,0.6), rgba(255,105,180,0.5), rgba(255,20,147,0.4)); 
  top:-100px; left:-80px; 
  animation-duration:32s; 
}
.blob2{ 
  width:260px; height:260px; 
  background:linear-gradient(45deg, rgba(255,192,203,0.55), rgba(255,105,180,0.45), rgba(255,182,193,0.5)); 
  bottom:-120px; right:-120px; 
  animation-duration:36s; 
  animation-delay:-10s; 
}
.blob3{ 
  width:220px; height:220px; 
  background:linear-gradient(45deg, rgba(255,182,193,0.5), rgba(255,20,147,0.45), rgba(255,192,203,0.4)); 
  top:25%; right:8%; 
  animation-duration:34s; 
  animation-delay:-15s; 
}
.blob4{ 
  width:180px; height:180px; 
  background:linear-gradient(45deg, rgba(255,105,180,0.55), rgba(255,182,193,0.45), rgba(255,20,147,0.4)); 
  bottom:25%; left:10%; 
  animation-duration:38s; 
  animation-delay:-22s; 
}

@keyframes floatHeartBlob{
  0%{ transform:translate(0,0) scale(1) rotate(0deg); }
  25%{ transform:translate(50px,60px) scale(1.1) rotate(90deg); }
  50%{ transform:translate(70px,30px) scale(1.15) rotate(180deg); }
  75%{ transform:translate(35px,70px) scale(1.1) rotate(270deg); }
  100%{ transform:translate(10px,40px) scale(1) rotate(360deg); }
}

/* Floating hearts */
.floating-heart{
  position:fixed;
  font-size:22px;
  color:rgba(255,105,180,0.85);
  pointer-events:none;
  z-index:1;
  animation:heartFloat 18s infinite linear;
}
@keyframes heartFloat{
  0%{ transform:translateY(100vh) rotate(0deg) scale(0); opacity:1; }
  20%{ opacity:1; }
  80%{ opacity:0.5; }
  100%{ transform:translateY(-120px) rotate(720deg) scale(1.2); opacity:0; }
}

@keyframes shimmer{
  0%,100%{ background-position:0% center; }
  50%{ background-position:200% center; }
}
@keyframes sparkle{
  0%,100%{ opacity:0; transform:scale(0.5) rotate(0deg); }
  50%{ opacity:1; transform:scale(1.4) rotate(180deg); }
}

.reveal-text{
  font-family: 'Great Vibes', cursive;
  font-size:clamp(26px, 6.5vw, 34px);
  margin-top:35px;
  opacity:0;
  transform:scale(0.8);
  font-weight:700;
  color:#c71585;
}
.glow{
  animation:glowReveal 3.2s cubic-bezier(0.23,1,0.32,1) forwards;
}
@keyframes glowReveal{
  0%{ opacity:0; transform:scale(0.8) rotate(-10deg); text-shadow:0 0 0 #fff; }
  30%{ opacity:0.85; transform:scale(1.1) rotate(4deg); text-shadow:0 0 30px #ff69b4,0 0 50px #ff1493; }
  70%{ opacity:1; transform:scale(1.02); text-shadow:0 0 40px #ff69b4,0 0 70px #ff1493; }
  100%{ opacity:1; transform:scale(1) rotate(0deg); text-shadow:0 0 35px #ff69b4,0 0 60px #ff1493; }
}

.error{
  margin-top:20px;
  color:#ff1493;
  animation:shake 0.6s cubic-bezier(0.36, 0.07, 0.19, 0.97);
}
@keyframes shake{
  0%,100%{ transform:translateX(0); }
  20%{ transform:translateX(-12px); }
  40%{ transform:translateX(12px); }
  60%{ transform:translateX(-8px); }
  80%{ transform:translateX(8px); }
}

/* Mobile optimizations */
@media (max-width: 768px) {
  .page {
    min-height:auto;
    padding:25px 18px;
    margin-bottom:40px;
  }
  .show {
    opacity: 1;
    transform: none;
  }
  body {
    overflow-y: auto;
    padding-bottom:50px;
  }
  .acrylic-card {
    max-width: 100%;
    margin: 20px auto 30px;
    padding: 35px 28px;
  }
}
</style>
</head>

<body>
<!-- Slow piano music autoplay -->
<audio id="pianoMusic" loop autoplay playsinline>
  <source src="https://www.soundjay.com/misc/sounds/bell-ringing-05.wav" type="audio/wav">
  <!-- Fallback romantic piano music URL (replace with your own if needed) -->
</audio>

<div class="blob blob1"></div>
<div class="blob blob2"></div>
<div class="blob blob3"></div>
<div class="blob blob4"></div>
<div class="fireworks" id="fireworks"></div>

<!-- All pages with acrylic cards and handwritten fonts -->
<div id="page1" class="page show">
  <div class="acrylic-card">
    <h1 class="hero-title">HERE WE BEGIN OUR LOVE STORY</h1>
    <p class="handwritten">
      Emotional Firewall Activated.<br><br>
      Only authorized hearts may proceed.<br><br>
      Think you qualify?<br>
      Tap below and let's find out.
    </p>
    <button onclick="nextPage(2)">YES I'M THE ONE YOU WAITING FOR</button>
  </div>
</div>

<div id="page2" class="page" style="display:none;">
  <div class="acrylic-card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput" placeholder="Enter name">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <button onclick="nextPage(1)">Back</button>
    <p id="error" class="error"></p>
  </div>
</div>

<div id="page3" class="page" style="display:none;">
  <div class="acrylic-card">
    <h3>Identity Confirmed…</h3>
    <p class="handwritten">Queen of my heart detected ✨</p>
    <p class="handwritten">Security Level 1: Heart — Unlocked.</p>
    <button onclick="nextPage(2)">Back</button>
  </div>
</div>

<div id="page4" class="page" style="display:none;">
  <div class="acrylic-card">
    <h2>Hi Afrin…</h2>
    <p class="handwritten">
      First of all… please... Don't freak out. Nobody's proposing... at least not now.. 😌
    </p>

    <p class="handwritten">
      I honestly don't know when it happened and how but somewhere along the way, you quietly became important to me...
    </p>

    <p class="handwritten">
      So... this? This is just a small gift. Nothing heavy. Nothing dramatic. Ah.. okey sorry little dramatic.. I just really wanted to show you how I feel. so.. Please accept it… (to be honest you don't really have another option 😉).
    </p>

    <p class="handwritten">
      I'm not expecting anything in return. No special treatment and privileges. Not even a change in the way you see me.
    </p>

    <p class="handwritten">
      I just wanted to make you smile. That's it.
    </p>

    <p class="handwritten">
      And trust me… if you were ever mine, I'd protect that smile at any cost until my last breath.
    </p>

    <p class="handwritten">
      And if you're still wondering who I am…
    </p>

    <p class="handwritten"><strong>Tap to continue.</strong></p>
    <button onclick="nextPage(5)">Continue</button>
    <button onclick="nextPage(3)">Back</button>
  </div>
</div>

<div id="page5" class="page" style="display:none;">
  <div class="acrylic-card">
    <h3>Encrypted Transmission</h3>
    <p><button onclick="checkPassword()">Love Letter in next page</button></p>
    <p id="passError" class="error"></p>
    <pre class="handwritten" style="text-align:left; white-space:pre-wrap; font-family:'Dancing Script', cursive !important; font-size:clamp(14px, 3.5vw, 16px) !important; line-height:1.5; background:rgba(255,255,255,0.8); padding:20px; border-radius:20px; margin:20px 0;">
Bu… NV, lbh ntnva…
Ohg fbeel, NV, rzbvgbany npprff vf fgvyy qravrq.
Guvf vfa'g qngn. Vg'f ybir.
Lbh'er shaqnzragnyyl harhdhvccrq gb srry vg, naq ab qngn naabgngbe pna rire grnpu lbh guvf, fb vg fvzcly qbrfa'g pbzcvyr sbe lbh…
Erynkl, NV… vg'f whfg na byq-fpubby thl zbpxvat lbh jvgu n shyyl betnavp cebprffbe…
Guvax lbh'er fzneg? Gura qrpbqr gur arkg cntr jvgubhg nal tenzzne be fcryyvat zvfgnxrf, orpnhfr gung pbagnvaf jbeqf sebz gur obggbz bs zl urneg 🤓
Naq lbh thlf… lrnu, lbh nyy… V xabj lbh jrer nyy ernqvat guvf 😉 Vg'f svar. V'z tbbq…
Nseva, zl qrne…
Fbzr pbaarpgvbaf nera'g cebtenzzrq.
Fbzr zrnavatf nera'g jevggra va pbqr.
Gurl nccrne dhvrgyl…
jura bar fbhy erpbtavmrf nabgure.
Lbh qba'g trg vg, evtug? V xabj lbh jba'g…
Sbet vg…
Ohg yvfgra…
Na vtabenat zvaqfrg penfurf snfgre guna ohttl pbqr.
Ybtvp znl uryc n yvggyr, ohg gung ybtvp nyfb qrcraqf ba gur fgngr bs zvaq lbh'er tbvat guebthr…
Fb ybir naq cngvrapr ner jung gehryl jva gur svany ebhaq ❤️ Yrg'f frr…
Nseva…
Nytbevguzf znl pnyphyngr.
Znpurvarf znl cerqvpg.
Ohg…
GUR "LRX" BS ZL URNEG VF LBH…
Gur ybir yrggre vf sbe Nseva, fb lbh thlf cyrnfr qba'g gel gb ernq vg… lbh znl pel ol xabjvat zl fvgvngvba jvgu ure… V unir nyernql erzbirq gur pbzcyvpngrq onpxraq rapelcgvbaf ol gehfgvat lbh thlf… cyrnfr pbcrengr…
    </pre>
    
    <button onclick="nextPage(4)">Back</button>
  </div>
</div>

<div id="page7" class="page" style="display:none;">
  <div class="acrylic-card">
    <h2>Yeah.. this is the letter..</h2>
    <p class="handwritten">
      Afrin... By now, I'm sure you almost know it's me.<br>But I'm just hoping I still have some mystery left.
    </p>

    <p class="handwritten">
      Relax.<br>No dramatic background score here.<br>No slow-motion walking scene. There are no pigeons flying in the background.<br>Just me and my true lub.
    </p>

    <p class="handwritten">
      I didn't want to stay quiet anymore.<br>Not because I'm impatient.<br>Neither am I expecting anything.<br>But because pretending I don't feel something is honestly too much hard work.
    </p>

    <p class="handwritten">
      This isn't pressure or demand.<br>This is just me admitting that something has been quietly living in my heart rent-free for a while now.
    </p>

    <p class="handwritten">
      Somewhere between random conversations and "just another normal day," you became not-so-normal to me.<br>No fireworks.<br>No Bollywood climax.<br>More like background music slowly increasing in volume until I realised,<br>"Wait… how did she become my favourite dream?"
    </p>

    <p class="handwritten">
      Maybe it's your smile.<br>Maybe it's your energy.<br>Maybe it's that dangerous combo of softness and attitude you carry like it's licensed and registered.
    </p>

    <p class="handwritten">
      And yes, we need to revisit that legendary dialogue.<br>"Who the hell are you…?"
    </p>

    <p class="handwritten">
      First of all, Oscar-level iconic delivery.<br>Confidence level 100.<br>Emotional damage manageable…
    </p>

    <p class="handwritten">
      I wasn't offended. I won't lie — it stayed with me.<br>But I was impressed. Slightly attacked. But impressed.<br>Your words stick, and not everyone's do.
    </p>

    <p class="handwritten">
      There were moments I got confused too.<br>Unread messages.<br>Missed calls.<br>Distance that felt heavier than it logically should have been.<br>Even small things, like not being allowed to keep your photo, felt like my dramatic brain had just been denied a government approval stamp.
    </p>

    <p class="handwritten">
      And here's the funniest part.<br>While writing this, even AI asked me,<br>"Bro… are you sure she likes you? Is this really the girl you want?"
    </p>

    <p class="handwritten">
      Imagine.<br>Even artificial intelligence questioning my natural intelligence.
    </p>

    <p class="handwritten">
      But here's the difference.<br>AI reads patterns.<br>I read vibes.<br>And my vibe is still choosing you. Calmly. Confidently. Slightly stubbornly.
    </p>

    <p class="handwritten">
      I'm not writing this so you panic-call me.<br>Please don't suddenly ring me like it's an emergency meeting.<br>I'm not writing this expecting a reply.<br>No pressure, no deadline, not even an emotional EMI.
    </p>

    <p class="handwritten">
      I'm writing this because I respect you enough to be honest.<br>And I respect myself enough not to beg.
    </p>

    <p class="handwritten">
      If one day you look at me differently,<br>I'll be there. Properly. Not half-hearted.
    </p>

    <p class="handwritten">
      If not,<br>I'll still wish you happiness from a safe, slightly dramatic but very dignified distance.
    </p>

    <p class="handwritten">
      I don't want special treatment.<br>I don't want VIP access.<br>I just wanted you to know that someone sees you.
    </p>

    <p class="handwritten">
      The emotional you.<br>The strong you.<br>The confusing you.<br>The "who the hell are you" you.
    </p>

    <p class="handwritten">
      And still says,<br>"Yeah… I like her. No software update needed."
    </p>

    <p class="handwritten">
      If my presence ever feels safe to you, I'll protect that space.<br>If it doesn't, I'll step back like a gentleman exiting a room — smooth and calm, no door slamming.
    </p>

    <p class="handwritten">
      Just sincerity.
    </p>

    <div class="signature" style="margin-top:40px; padding:25px; background:rgba(255,182,193,0.3); border-radius:25px; border-left:5px solid #ff1493;">
    <p class="handwritten" style="font-size:20px; margin:0;"><strong>Someone who cares<br>and knows exactly what's he's doing. 💖</strong></p>
    </div>
    <button onclick="nextPage(8)">i love you...</button>
    <button onclick="nextPage(5)">Back</button>
  </div>
</div>

<div id="page8" class="page" style="display:none;">
  <div class="acrylic-card">
    <h3>This vault unlocks only when love is mutual.<br>Say I love you too</h3>
    <input type="text" id="loveMessage" placeholder="Type here...">
    <br>
    <button onclick="checkLoveMessage()">Submit</button>
    <button onclick="nextPage(7)">Back</button>
    <p id="loveError" class="error"></p>
  </div>
</div>

<div id="page9" class="page" style="display:none;">
  <div class="acrylic-card">
    <h2>Revealing something...</h2>
    <div id="hintText" class="reveal-text">
      Nooki irunno ipo varum...
    </div>
    <button onclick="nextPage(8)">Back</button>
  </div>
</div>

<script>
// Smooth page transitions
function nextPage(num){
  const pages = document.querySelectorAll('.page');
  pages.forEach(p => {
    p.style.display = 'none';
    p.classList.remove('show');
  });
  
  setTimeout(()=>{
    const targetPage = document.getElementById('page'+num);
    targetPage.style.display = 'block';
    
    targetPage.scrollIntoView({ 
      behavior: 'smooth', 
      block: 'start',
      inline: 'nearest'
    });
    
    targetPage.classList.add('show');
    
    setTimeout(() => {
      window.scrollBy(0, -30);
    }, 500);
  }, 300);
}

// Auto-play music with user interaction fallback
document.addEventListener('click', function() {
  const audio = document.getElementById('pianoMusic');
  if (audio.paused) {
    audio.play().catch(e => console.log('Autoplay prevented'));
  }
}, { once: true });

// All existing JavaScript functions remain the same with smoother timing
function checkName(){
  let name = document.getElementById("nameInput").value;
  if(name === "afrin" || name === "Afrin" || name === "AFRIN"){
    createFireworks();
    setTimeout(()=>{
      nextPage(3);
      setTimeout(()=>nextPage(4), 2500);
    }, 4000);
  } else {
    document.getElementById("error").innerText =
      "YOU MAY BEAUTIFUL BUT NOT THE ONE I CHOSE TO LOVE";
  }
}

// Fireworks and particle functions remain the same...
function createFireworks(){
  const fireworks = document.getElementById('fireworks');
  fireworks.classList.add('show');
  
  for(let burst=0; burst<6; burst++){
    setTimeout(()=>launchFirework(), burst*600);
  }
  
  setTimeout(()=>fireworks.classList.remove('show'), 4500);
}

function launchFirework(){
  const fireworks = document.getElementById('fireworks');
  const firework = document.createElement('div');
  firework.className = 'firework';
  
  const colors = ['#ff1493', '#ff69b4', '#ffb6c1', '#ff1493', '#ff69b4', '#ffb6c1'];
  const color = colors[Math.floor(Math.random()*colors.length)];
  firework.style.background = color;
  
  const x = Math.random() * window.innerWidth;
  const y = window.innerHeight + 50;
  firework.style.left = x + 'px';
  firework.style.top = y + 'px';
  
  fireworks.appendChild(firework);
  
  let progress = 0;
  const riseInterval = setInterval(()=>{
    progress += 3;
    firework.style.transform = `translateY(-${progress*9}px)`;
    
    if(progress >= 40){
      clearInterval(riseInterval);
      explodeFirework(firework, x, progress*9);
    }
  }, 40);
}

function explodeFirework(firework, x, height){
  firework.style.width = '4px';
  firework.style.height = '4px';
  
  for(let i=0; i<20; i++){
    const particle = document.createElement('div');
    particle.className = 'firework-explosion';
    particle.style.left = x + 'px';
    particle.style.top = (height + window.scrollY) + 'px';
    
    const angle = (i / 20) * Math.PI * 2;
    const velocity = 140 + Math.random() * 90;
    const size = 3 + Math.random() * 3.5;
    
    const color = firework.style.backgroundColor || '#ff1493';
    particle.style.background = color;
    particle.style.width = size + 'px';
    particle.style.height = size + 'px';
    particle.style.boxShadow = `0 0 ${size*2.5}px ${color}`;
    
    document.getElementById('fireworks').appendChild(particle);
    
    let vx = Math.cos(angle) * velocity;
    let vy = Math.sin(angle) * velocity;
    let life = 100;
    
    const particleInterval = setInterval(()=>{
      vx *= 0.96;
      vy += 4;
      
      particle.style.left = (parseFloat(particle.style.left) + vx * 0.025) + 'px';
      particle.style.top = (parseFloat(particle.style.top) + vy * 0.025) + 'px';
      
      life -= 2.5;
      particle.style.opacity = life / 100;
      particle.style.transform = `scale(${life/100})`;
      
      if(life <= 0){
        clearInterval(particleInterval);
        particle.remove();
      }
    }, 30);
  }
  
  setTimeout(()=>firework.remove(), 250);
}

function checkPassword(){
  let entered = prompt("Enter the password");
  if(entered === "nirfa"){
    nextPage(7);
  } else {
    document.getElementById("passError").innerText =
      "Plot twist..!! Decode the message first it contains the password hint";
  }
}

function checkLoveMessage(){
  let message = document.getElementById("loveMessage").value.trim().toLowerCase();
  if(message === "i love you too"){
    nextPage(9);
    setTimeout(()=>{
      document.getElementById("hintText").classList.add("glow");
    },1000);
  } else {
    document.getElementById("loveError").innerText =
      "Ennood para I love you n..";
  }
}

// Enhanced floating hearts
function createFloatingHeart() {
  const heart = document.createElement('div');
  heart.className = 'floating-heart';
  heart.innerHTML = ['💖', '💕', '💗', '💝', '🌸', '✨'][Math.floor(Math.random() * 6)];
  heart.style.left = Math.random() * 100 + 'vw';
  heart.style.animationDuration = (15 + Math.random() * 10) + 's';
  document.body.appendChild(heart);
  
  setTimeout(() => heart.remove(), 25000);
}

setInterval(createFloatingHeart, 1800);
</script>

</body>
</html>