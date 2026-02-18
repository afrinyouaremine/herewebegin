<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>THE REAL LOVE STORY</title>

<style>
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
  
  /* Romantic floating hearts */
  animation: heartBeat 20s ease-in-out infinite;
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
  transform:translateY(30px);
  transition:all 0.8s cubic-bezier(.23,1.01,.32,1);
  position:relative;
  z-index:2;
}
.show{
  opacity:1;
  transform:translateY(0);
}

/* Perfect card for romantic theme */
.card{
  backdrop-filter: blur(25px) saturate(180%);
  background: rgba(255,255,255,0.85);
  border-radius:35px;
  padding:35px 30px;
  margin:20px auto;
  max-width:95vw;
  width:100%;
  box-shadow:0 25px 70px rgba(255,105,180,0.3), 0 0 0 1px rgba(255,182,193,0.5), inset 0 1px 0 rgba(255,255,255,0.8);
  border:1px solid rgba(255,192,203,0.6);
  animation:cardBloom 1.2s cubic-bezier(.23,1,.32,1);
  position:relative;
  overflow:hidden;
  box-sizing:border-box;
}

.card::before{
  content:'💖';
  position:absolute;
  top:-20px; right:-20px;
  font-size:40px;
  opacity:0.1;
  animation: floatHeart 6s infinite linear;
  z-index:0;
}

.card::after{
  content:'✨';
  position:absolute;
  bottom:10px; left:10px;
  font-size:20px;
  opacity:0.3;
  animation: sparkle 3s infinite;
}

@keyframes cardBloom{
  0%{ transform:scale(0.7) rotateX(15deg); opacity:0; }
  100%{ transform:scale(1) rotateX(0deg); opacity:1; }
}

@keyframes floatHeart{
  0%{ transform:translateY(0) rotate(0deg); }
  100%{ transform:translateY(-20px) rotate(360deg); }
}

.hero-title{
  font-size:clamp(28px, 6vw, 36px);
  letter-spacing:2px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#ff1493,#ff69b4,#ffb6c1,#ff1493);
  background-size:300% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shimmer 3s linear infinite;
  position:relative;
  margin-bottom:25px;
  text-shadow:0 0 20px rgba(255,105,180,0.5);
}

h2{
  font-size:clamp(24px, 6vw, 30px);
  color:#8b008b;
}
h3{
  font-size:clamp(22px, 5vw, 26px);
  color:#c71585;
}

p {
  font-size:clamp(15px, 4.2vw, 17px);
  line-height:1.7;
  margin-bottom:18px;
  color:#4a1a4a;
}

.card p {
  text-align:left;
  hyphens:auto;
  word-wrap:break-word;
}

input{
  padding:18px;
  width:92%;
  max-width:420px;
  border:2px solid rgba(255,182,193,0.6);
  border-radius:25px;
  margin:18px auto;
  display:block;
  background:rgba(255,255,255,0.9);
  color:#4a1a4a;
  outline:none;
  transition:all 0.4s;
  font-size:clamp(16px, 4vw, 18px);
  box-sizing:border-box;
  box-shadow:0 4px 15px rgba(255,105,180,0.2);
}
input::placeholder{
  color:rgba(139,0,139,0.6);
}
input:focus{
  box-shadow:0 0 30px rgba(255,105,180,0.6), 0 8px 25px rgba(255,20,147,0.3);
  transform:scale(1.03);
  border-color:rgba(255,20,147,0.8);
  background:rgba(255,255,255,0.95);
}

button{
  margin:12px 8px;
  padding:18px 40px;
  min-height:55px;
  border:none;
  border-radius:30px;
  background:linear-gradient(45deg,#ff1493,#ff69b4,#ffb6c1);
  color:white;
  font-weight:700;
  cursor:pointer;
  font-size:clamp(16px, 4vw, 19px);
  position:relative;
  overflow:hidden;
  transition:all 0.4s;
  display:inline-block;
  touch-action:manipulation;
  box-shadow:0 6px 20px rgba(255,105,180,0.4);
}
button::before{
  content:'';
  position:absolute;
  top:0; left:-100%;
  width:100%; height:100%;
  background:linear-gradient(90deg,transparent,rgba(255,255,255,0.5),transparent);
  transition:0.6s;
}
button:hover, button:active{
  transform:scale(1.06) translateY(-3px);
  box-shadow:0 12px 35px rgba(255,105,180,0.6);
}
button:active{
  transform:scale(0.99);
}

/* Enhanced romantic blobs (hearts instead of blobs) */
.blob{
  position:fixed;
  border-radius:50% 0 50% 0;
  filter:blur(10px);
  animation:floatHeartBlob 25s infinite ease-in-out;
  z-index:-1;
  opacity:0.6;
}
.blob1{ 
  width:280px; height:280px; 
  background:linear-gradient(45deg, rgba(255,182,193,0.5), rgba(255,105,180,0.4), rgba(255,20,147,0.3)); 
  top:-80px; left:-60px; 
  animation-duration:28s; 
}
.blob2{ 
  width:240px; height:240px; 
  background:linear-gradient(45deg, rgba(255,192,203,0.45), rgba(255,105,180,0.35), rgba(255,182,193,0.4)); 
  bottom:-100px; right:-100px; 
  animation-duration:32s; 
  animation-delay:-8s; 
}
.blob3{ 
  width:200px; height:200px; 
  background:linear-gradient(45deg, rgba(255,182,193,0.4), rgba(255,20,147,0.35), rgba(255,192,203,0.3)); 
  top:20%; right:5%; 
  animation-duration:30s; 
  animation-delay:-12s; 
}
.blob4{ 
  width:160px; height:160px; 
  background:linear-gradient(45deg, rgba(255,105,180,0.45), rgba(255,182,193,0.35), rgba(255,20,147,0.3)); 
  bottom:20%; left:8%; 
  animation-duration:34s; 
  animation-delay:-18s; 
}

@keyframes floatHeartBlob{
  0%{ transform:translate(0,0) scale(1) rotate(0deg); }
  25%{ transform:translate(40px,50px) scale(1.08) rotate(90deg); }
  50%{ transform:translate(60px,25px) scale(1.12) rotate(180deg); }
  75%{ transform:translate(25px,60px) scale(1.08) rotate(270deg); }
  100%{ transform:translate(0px,35px) scale(1) rotate(360deg); }
}

/* Romantic floating hearts */
.floating-heart{
  position:fixed;
  font-size:20px;
  color:rgba(255,105,180,0.8);
  pointer-events:none;
  z-index:1;
  animation:heartFloat 15s infinite linear;
}
@keyframes heartFloat{
  0%{ transform:translateY(100vh) rotate(0deg) scale(0); opacity:1; }
  20%{ opacity:1; }
  80%{ opacity:0.4; }
  100%{ transform:translateY(-100px) rotate(720deg) scale(1); opacity:0; }
}

@keyframes shimmer{
  0%,100%{ background-position:0% center; }
  50%{ background-position:200% center; }
}
@keyframes sparkle{
  0%,100%{ opacity:0; transform:scale(0.5) rotate(0deg); }
  50%{ opacity:1; transform:scale(1.3) rotate(180deg); }
}

.reveal-text{
  font-size:clamp(22px, 5.5vw, 28px);
  margin-top:30px;
  opacity:0;
  transform:scale(0.85);
  font-weight:700;
  color:#c71585;
}
.glow{
  animation:glowReveal 2.8s cubic-bezier(.23,1,.32,1) forwards;
}
@keyframes glowReveal{
  0%{ opacity:0; transform:scale(0.85) rotate(-8deg); text-shadow:0 0 0 #fff; }
  30%{ opacity:0.8; transform:scale(1.08) rotate(3deg); text-shadow:0 0 25px #ff69b4,0 0 45px #ff1493; }
  70%{ opacity:1; transform:scale(1); text-shadow:0 0 35px #ff69b4,0 0 65px #ff1493; }
  100%{ opacity:1; transform:scale(1) rotate(0deg); text-shadow:0 0 30px #ff69b4,0 0 55px #ff1493; }
}

.error{
  margin-top:15px;
  color:#ff1493;
  animation:shake 0.5s ease;
}
@keyframes shake{
  0%,100%{ transform:translateX(0); }
  20%{ transform:translateX(-10px); }
  40%{ transform:translateX(10px); }
  60%{ transform:translateX(-6px); }
  80%{ transform:translateX(6px); }
}

/* Perfect mobile scrolling */
@media (max-width: 768px) {
  .page {
    min-height:auto;
    padding:20px 15px;
    margin-bottom:30px;
  }
  .show {
    opacity: 1;
    transform: none;
  }
  body {
    overflow-y: auto;
    padding-bottom:40px;
  }
  .card {
    max-width: 100%;
    margin: 15px auto 25px;
    padding: 30px 25px;
  }
  
  /* Ensure content stays visible */
  .page:last-child {
    margin-bottom: 50px;
  }
}

@media (max-width: 768px) and (orientation: landscape) {
  .card {
    padding: 25px 20px;
    margin-bottom: 20px;
  }
  body {
    padding-bottom: 30px;
  }
}
</style>
</head>

<body>
<div class="blob blob1"></div>
<div class="blob blob2"></div>
<div class="blob blob3"></div>
<div class="blob blob4"></div>
<div class="fireworks" id="fireworks"></div>

<!-- Perfect scrolling pages -->
<div id="page1" class="page show">
  <div class="card">
    <h1 class="hero-title">HERE WE BEGIN OUR LOVE STORY</h1>
    <p>
      Emotional Firewall Activated.<br><br>
      Only authorized hearts may proceed.<br><br>
      Think you qualify?<br>
      Tap below and let’s find out.
    </p>
    <button onclick="nextPage(2)">YES I'M THE ONE YOU WAITING FOR</button>
  </div>
</div>

<!-- Rest of your HTML content stays exactly the same -->
<div id="page2" class="page" style="display:none;">
  <div class="card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput" placeholder="Enter name">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <button onclick="nextPage(1)">Back</button>
    <p id="error" class="error"></p>
  </div>
</div>

<div id="page3" class="page" style="display:none;">
  <div class="card">
    <h3>Identity Confirmed…</h3>
    <p> Queen of my heart detected ✨</p>
    <p>Security Level 1: Heart — Unlocked.</p>
    <button onclick="nextPage(2)">Back</button>
  </div>
</div>

<div id="page4" class="page" style="display:none;">
  <div class="card">
    <h2>Hi Afrin…</h2>
    <p>First of all… please... Don't freak out. Nobody's proposing... at least not now.. 😌</p>

    <p>I honestly don't know when it happened and how but somewhere along the way, you quietly became important to me... </p>

    <p>So... this? This is just a small gift. Nothing heavy. Nothing dramatic. Ah.. okey sorry little dramatic..  I just really wanted to show you how I feel. so.. Please accept it… (to be honest you don't really have another option 😉).</p>

    <p>I'm not expecting anything in return. No special treatment and privileges. Not even a change in the way you see me.</p>

    <p>I just wanted to make you smile. That's it.</p>

    <p>And trust me… if you were ever mine, I'd protect that smile at any cost until my last breath.</p>

    <p>And if you're still wondering who I am…</p>

    <p><strong>Tap to continue.</strong></p>
    <button onclick="nextPage(5)">Continue</button>
    <button onclick="nextPage(3)">Back</button>
  </div>
</div>

<div id="page5" class="page" style="display:none;">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <p><button onclick="checkPassword()">Love Letter in next page </button></p>
    <p id="passError" class="error"></p>
    <pre style="text-align:left; white-space:pre-wrap; font-family:monospace; font-size:clamp(12px, 3vw, 14px); line-height:1.4; background:rgba(255,255,255,0.7); padding:15px; border-radius:15px; margin:15px 0;">
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
  <div class="card">
    <h2> Yeah.. this is the letter.. </h2>
    <p> Afrin... By now, I'm sure you almost know it's me.<br>
    But I'm just hoping I still have some mystery left.</p>

    <p>Relax.<br>
    No dramatic background score here.<br>
    No slow-motion walking scene. There are no pigeons flying in the background.<br>
    Just me and my true lub.</p>

    <p>I didn't want to stay quiet anymore.<br>
    Not because I'm impatient.<br>
    Neither am I expecting anything.<br>
    But because pretending I don't feel something is honestly too much hard work.</p>

    <p>This isn't pressure or demand.<br>
    This is just me admitting that something has been quietly living in my heart rent-free for a while now.</p>

    <p>Somewhere between random conversations and "just another normal day," you became not-so-normal to me.<br>
    No fireworks.<br>
    No Bollywood climax.<br>
    More like background music slowly increasing in volume until I realised,<br>
    "Wait… how did she become my favourite dream?"</p>

    <p>Maybe it's your smile.<br>
    Maybe it's your energy.<br>
    Maybe it's that dangerous combo of softness and attitude you carry like it's licensed and registered.</p>

    <p>And yes, we need to revisit that legendary dialogue.<br>
    "Who the hell are you…?"</p>

    <p>First of all, Oscar-level iconic delivery.<br>
    Confidence level 100.<br>
    Emotional damage manageable…</p>

    <p>I wasn't offended. I won't lie — it stayed with me.<br>
    But I was impressed. Slightly attacked. But impressed.<br>
    Your words stick, and not everyone's do.</p>

    <p>There were moments I got confused too.<br>
    Unread messages.<br>
    Missed calls.<br>
    Distance that felt heavier than it logically should have been.<br>
    Even small things, like not being allowed to keep your photo, felt like my dramatic brain had just been denied a government approval stamp.</p>

    <p>And here's the funniest part.<br>
    While writing this, even AI asked me,<br>
    "Bro… are you sure she likes you? Is this really the girl you want?"</p>

    <p>Imagine.<br>
    Even artificial intelligence questioning my natural intelligence.</p>

    <p>But here's the difference.<br>
    AI reads patterns.<br>
    I read vibes.<br>
    And my vibe is still choosing you. Calmly. Confidently. Slightly stubbornly.</p>

    <p>I'm not writing this so you panic-call me.<br>
    Please don't suddenly ring me like it's an emergency meeting.<br>
    I'm not writing this expecting a reply.<br>
    No pressure, no deadline, not even an emotional EMI.</p>

    <p>I'm writing this because I respect you enough to be honest.<br>
    And I respect myself enough not to beg.</p>

    <p>If one day you look at me differently,<br>
    I'll be there. Properly. Not half-hearted.</p>

    <p>If not,<br>
    I'll still wish you happiness from a safe, slightly dramatic but very dignified distance.</p>

    <p>I don't want special treatment.<br>
    I don't want VIP access.<br>
    I just wanted you to know that someone sees you.</p>

    <p>The emotional you.<br>
    The strong you.<br>
    The confusing you.<br>
    The "who the hell are you" you.</p>

    <p>And still says,<br>
    "Yeah… I like her. No software update needed."</p>

    <p>If my presence ever feels safe to you, I'll protect that space.<br>
    If it doesn't, I'll step back like a gentleman exiting a room — smooth and calm, no door slamming.</p>

    <p>Just sincerity.</p>

    <div class="signature" style="margin-top:30px; padding:20px; background:rgba(255,182,193,0.2); border-radius:20px; border-left:4px solid #ff1493;">
    <p style="font-size:18px; margin:0;"><strong>Someone who cares<br>
    and knows exactly what's he's doing. 💖</strong></p>
    </div>
    <button onclick="nextPage(8)">i love you...</button>
    <button onclick="nextPage(5)">Back</button>
  </div>
</div>

<div id="page8" class="page" style="display:none;">
  <div class="card">
    <h3>This vault unlocks only when love is mutual.<br>Say I love you too</h3>
    <input type="text" id="loveMessage" placeholder="Type here...">
    <br>
    <button onclick="checkLoveMessage()">Submit</button>
    <button onclick="nextPage(7)">Back</button>
    <p id="loveError" class="error"></p>
  </div>
</div>

<div id="page9" class="page" style="display:none;">
  <div class="card">
    <h2>Revealing something...</h2>
    <div id="hintText" class="reveal-text">
      Nooki irunno ipo varum...
    </div>
    <button onclick="nextPage(8)">Back</button>
  </div>
</div>

<script>
// Enhanced page transitions with perfect scrolling
function nextPage(num){
  const pages = document.querySelectorAll('.page');
  pages.forEach(p => {
    p.style.display = 'none';
    p.classList.remove('show');
  });
  
  setTimeout(()=>{
    const targetPage = document.getElementById('page'+num);
    targetPage.style.display = 'block';
    
    // Perfect scroll positioning
    targetPage.scrollIntoView({ 
      behavior: 'smooth', 
      block: 'start',
      inline: 'nearest'
    });
    
    targetPage.classList.add('show');
    
    // Extra padding for perfect visibility
    setTimeout(() => {
      window.scrollBy(0, -20);
    }, 400);
  }, 250);
}

// Romantic floating hearts
function createFloatingHeart() {
  const heart = document.createElement('div');
  heart.className = 'floating-heart';
  heart.innerHTML = ['💖', '💕', '💗', '💝', '🌸'][Math.floor(Math.random() * 5)];
  heart.style.left = Math.random() * 100 + 'vw';
  heart.style.animationDuration = (12 + Math.random() * 8) + 's';
  document.body.appendChild(heart);
  
  setTimeout(() => heart.remove(), 20000);
}

// All your existing JavaScript functions remain the same
function checkName(){
  let name = document.getElementById("nameInput").value;
  if(name === "afrin" || name === "Afrin" || name === "AFRIN"){
    createFireworks();
    setTimeout(()=>{
      nextPage(3);
      setTimeout(()=>nextPage(4), 2000);
    }, 3500);
  } else {
    document.getElementById("error").innerText =
      "YOU MAY BEAUTIFUL BUT NOT THE ONE I CHOSE TO LOVE";
  }
}

function createFireworks(){
  const fireworks = document.getElementById('fireworks');
  fireworks.classList.add('show');
  
  for(let burst=0; burst<6; burst++){
    setTimeout(()=>launchFirework(), burst*500);
  }
  
  setTimeout(()=>fireworks.classList.remove('show'), 4000);
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
    progress += 2.5;
    firework.style.transform = `translateY(-${progress*8}px)`;
    
    if(progress >= 45){
      clearInterval(riseInterval);
      explodeFirework(firework, x, progress*8);
    }
  }, 35);
}

function explodeFirework(firework, x, height){
  firework.style.width = '4px';
  firework.style.height = '4px';
  
  for(let i=0; i<18; i++){
    const particle = document.createElement('div');
    particle.className = 'firework-explosion';
    particle.style.left = x + 'px';
    particle.style.top = (height + window.scrollY) + 'px';
    
    const angle = (i / 18) * Math.PI * 2;
    const velocity = 120 + Math.random() * 80;
    const size = 2.5 + Math.random() * 3;
    
    const color = firework.style.backgroundColor || '#ff1493';
    particle.style.background = color;
    particle.style.width = size + 'px';
    particle.style.height = size + 'px';
    particle.style.boxShadow = `0 0 ${size*2}px ${color}`;
    
    document.getElementById('fireworks').appendChild(particle);
    
    let vx = Math.cos(angle) * velocity;
    let vy = Math.sin(angle) * velocity;
    let life = 90;
    
    const particleInterval = setInterval(()=>{
      vx *= 0.97;
      vy += 3.5;
      
      particle.style.left = (parseFloat(particle.style.left) + vx * 0.02) + 'px';
      particle.style.top = (parseFloat(particle.style.top) + vy * 0.02) + 'px';
      
      life -= 2;
      particle.style.opacity = life / 90;
      particle.style.transform = `scale(${life/90})`;
      
      if(life <= 0){
        clearInterval(particleInterval);
        particle.remove();
      }
    }, 25);
  }
  
  setTimeout(()=>firework.remove(), 200);
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
    },800);
  } else {
    document.getElementById("loveError").innerText =
      "Ennood para I love you n..";
  }
}

// Romantic floating hearts + optimized particles
setInterval(createFloatingHeart, 2000);
setInterval(()=>{
  const particle = document.createElement('div');
  particle.className = 'particle';
  particle.style.left = (Math.random() * 100) + 'vw';
  particle.style.animationDuration = (8 + Math.random() * 5) + 's';
  particle.style.background = 'radial-gradient(circle, #ff69b4, transparent)';
  document.body.appendChild(particle);
  
  setTimeout(()=>particle.remove(), 15000);
}, 1500);
</script>

</body>
</html>