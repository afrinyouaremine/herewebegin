<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>THE REAL LOVE STORY</title>

<style>
body{
  margin:0;
  font-family:'Segoe UI', sans-serif;
  background:linear-gradient(135deg,#0f0c29,#302b63,#24243e);
  color:white;
  overflow:hidden;
  position:relative;
}

/* Enhanced Vibrant Acrylic Motion - Multiple Blobs */
.blob{
  position:fixed;
  border-radius:50%;
  filter:blur(60px);
  animation:floatBlob 16s infinite ease-in-out;
  z-index:-1;
  opacity:0.6;
}
.blob1{
  width:350px; height:350px;
  background:linear-gradient(45deg, rgba(0,255,255,0.3), rgba(255,0,255,0.2));
  top:-80px; left:-80px;
  animation-duration:18s;
}
.blob2{
  width:280px; height:280px;
  background:linear-gradient(45deg, rgba(255,100,150,0.25), rgba(100,255,200,0.25));
  bottom:-120px; right:-120px;
  animation-duration:22s, animation-delay:-4s;
}
.blob3{
  width:200px; height:200px;
  background:linear-gradient(45deg, rgba(255,255,100,0.2), rgba(150,0,255,0.2));
  top:20%; right:5%;
  animation-duration:20s, animation-delay:-8s;
}
.blob4{
  width:180px; height:180px;
  background:linear-gradient(45deg, rgba(0,200,255,0.25), rgba(255,150,0,0.25));
  bottom:20%; left:10%;
  animation-duration:24s, animation-delay:-12s;
}

@keyframes floatBlob{
  0%{ transform:translate(0,0) scale(1) rotate(0deg); }
  25%{ transform:translate(40px,60px) scale(1.1) rotate(90deg); }
  50%{ transform:translate(80px,20px) scale(1.3) rotate(180deg); }
  75%{ transform:translate(20px,80px) scale(1.2) rotate(270deg); }
  100%{ transform:translate(-20px,40px) scale(1) rotate(360deg); }
}

/* Floating Particles */
.particle{
  position:fixed;
  width:4px; height:4px;
  background:radial-gradient(circle, #00f2fe, transparent);
  border-radius:50%;
  pointer-events:none;
  z-index:10;
  animation:particleFloat 8s infinite linear;
}
@keyframes particleFloat{
  0%{ transform:translateY(100vh) scale(0); opacity:1; }
  50%{ opacity:0.8; }
  100%{ transform:translateY(-100px) scale(1); opacity:0; }
}

/* Page Animation */
.page{
  display:none;
  min-height:100vh;
  padding:40px 20px;
  text-align:center;
  opacity:0;
  transform:translateY(40px) scale(0.98);
  transition:all 0.9s cubic-bezier(.23,1.01,.32,1);
}
.show{
  display:block;
  opacity:1;
  transform:translateY(0) scale(1);
}

/* Enhanced Card */
.card{
  backdrop-filter: blur(40px);
  background: rgba(255,255,255,0.12);
  border-radius:30px;
  padding:40px;
  margin:auto;
  max-width:550px;
  box-shadow:0 20px 60px rgba(0,0,0,0.6), inset 0 1px 0 rgba(255,255,255,0.2);
  border:1px solid rgba(255,255,255,0.1);
  animation:cardPop 1s cubic-bezier(.23,1,.32,1);
  position:relative;
  overflow:hidden;
}
.card::before{
  content:'';
  position:absolute;
  top:-50%; left:-50%;
  width:200%; height:200%;
  background:linear-gradient(45deg, transparent, rgba(0,255,255,0.1), transparent);
  transform:rotate(45deg) translateX(-200%) scale(0.7);
  transition:0.8s;
}
.card:hover::before{
  transform:rotate(45deg) translateX(200%) scale(0.7);
}
@keyframes cardPop{
  0%{ transform:scale(0.8) rotateX(10deg); opacity:0; }
  100%{ transform:scale(1) rotateX(0deg); opacity:1; }
}

.hero-title{
  font-size:28px;
  letter-spacing:4px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#00f2fe,#ff00cc,#00f2fe,#4adeff);
  background-size:300% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shimmer 4s linear infinite;
  position:relative;
}
.hero-title::after{
  content:'✨';
  position:absolute;
  font-size:20px;
  animation:sparkle 2s infinite;
}
@keyframes shimmer{
  0%,100%{ background-position:0% center; }
  50%{ background-position:200% center; }
}
@keyframes sparkle{
  0%,100%{ opacity:0; transform:scale(0.5) rotate(0deg); }
  50%{ opacity:1; transform:scale(1.2) rotate(180deg); }
}

h2,h3{
  background:linear-gradient(45deg,#00f2fe,#ff00cc,#4adeff);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  font-weight:700;
}

input{
  padding:16px;
  width:85%;
  border:1px solid rgba(255,255,255,0.2);
  border-radius:16px;
  margin-top:18px;
  background:rgba(255,255,255,0.08);
  color:white;
  outline:none;
  transition:all 0.4s;
  font-size:16px;
}
input::placeholder{
  color:rgba(255,255,255,0.6);
}
input:focus{
  box-shadow:0 0 25px rgba(0,242,254,0.5), 0 0 40px rgba(255,0,204,0.4);
  transform:scale(1.02);
  border-color:rgba(0,242,254,0.6);
  background:rgba(255,255,255,0.12);
}

button{
  margin:8px;
  padding:14px 30px;
  border:none;
  border-radius:30px;
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  color:white;
  font-weight:700;
  cursor:pointer;
  font-size:16px;
  position:relative;
  overflow:hidden;
  transition:all 0.4s;
}
button::before{
  content:'';
  position:absolute;
  top:0; left:-100%;
  width:100%; height:100%;
  background:linear-gradient(90deg,transparent,rgba(255,255,255,0.4),transparent);
  transition:0.6s;
}
button:hover{
  transform:scale(1.08) translateY(-2px);
  box-shadow:0 10px 30px rgba(0,242,254,0.4);
}
button:hover::before{
  left:100%;
}
button:active{
  transform:scale(0.98);
}

.error{
  margin-top:12px;
  color:#ff4d6d;
  animation:shake 0.4s ease;
}
@keyframes shake{
  0%,100%{ transform:translateX(0); }
  20%{ transform:translateX(-8px); }
  40%{ transform:translateX(8px); }
  60%{ transform:translateX(-4px); }
  80%{ transform:translateX(4px); }
}

.reveal-text{
  font-size:24px;
  margin-top:25px;
  opacity:0;
  transform:scale(0.8);
  font-weight:600;
}
.glow{
  animation:glowReveal 2.5s cubic-bezier(.23,1,.32,1) forwards;
}
@keyframes glowReveal{
  0%{ opacity:0; transform:scale(0.8) rotate(-5deg); text-shadow:0 0 0 #fff; }
  30%{ opacity:0.7; transform:scale(1.05) rotate(2deg); text-shadow:0 0 20px #ff00cc,0 0 40px #00f2fe; }
  70%{ opacity:1; transform:scale(0.98); text-shadow:0 0 30px #ff00cc,0 0 60px #00f2fe; }
  100%{ opacity:1; transform:scale(1) rotate(0deg); text-shadow:0 0 25px #ff00cc,0 0 50px #00f2fe; }
}

/* FIREWORKS ANIMATION */
.fireworks{
  position:fixed;
  top:0; left:0;
  width:100vw; height:100vh;
  pointer-events:none;
  z-index:1000;
  opacity:0;
  transition:opacity 0.5s;
}
.fireworks.show{
  opacity:1;
}
.firework{
  position:absolute;
  width:6px; height:6px;
  background:#00f2fe;
  border-radius:50%;
  pointer-events:none;
}
.firework-explosion{
  position:absolute;
  border-radius:50%;
  pointer-events:none;
}
</style>
</head>

<body>
<div class="blob blob1"></div>
<div class="blob blob2"></div>
<div class="blob blob3"></div>
<div class="blob blob4"></div>
<div class="fireworks" id="fireworks"></div>

<!-- PAGE 1 -->
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

<!-- PAGE 2 -->
<div id="page2" class="page">
  <div class="card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput" placeholder="Enter name">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <button onclick="nextPage(1)">Back</button>
    <p id="error" class="error"></p>
  </div>
</div>

<!-- PAGE 3 -->
<div id="page3" class="page">
  <div class="card">
    <h3>Identity Confirmed…</h3>
    <p> Queen of my heart detected ✨</p>
    <p>Security Level 1: Heart — Unlocked.</p>
    <button onclick="nextPage(2)">Back</button>
  </div>
</div>

<!-- PAGE 4 -->
<div id="page4" class="page">
  <div class="card">
    <h2>Hi Afrin…</h2>
    <p style="text-align:left">
<p>First of all… please... Don't freak out. Nobody's proposing... at least not now.. 😌</p>

<p>I honestly don't know when it happened and how but somewhere along the way, you quietly became important to me... </p>

<p>So... this? This is just a small gift. Nothing heavy. Nothing dramatic. Ah.. okey sorry little dramatic..  I just really wanted to show you how I feel. so.. Please accept it… (to be honest you don't really have another option 😉).</p>

<p>I'm not expecting anything in return. No special treatment and privileges. Not even a change in the way you see me.</p>

<p>I just wanted to make you smile. That's it.</p>

<p>And trust me… if you were ever mine, I'd protect that smile at any cost until my last breath.</p>

<p>And if you're still wondering who I am…</p>

<p><strong>Tap to continue.</strong></p>
    </p>
    <button onclick="nextPage(5)">Continue</button>
    <button onclick="nextPage(3)">Back</button>
  </div>
</div>

<!-- PAGE 5 -->
<div id="page5" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
<p><button onclick="checkPassword()">Love Letter in next page </button></p>
<p id="passError" class="error"></p>
    <pre style="text-align:left; white-space:pre-wrap; font-family:monospace;">
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
Ybtvp znl uryc n yvggyr, ohg gung ybtvp nyfb qrcraqf ba gur fgngr bs zvaq lbh'er tbvat guebhtu…
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

<!-- PAGE 7 -->
<div id="page7" class="page">
  <div class="card">
    <h2> Yeah.. this is the letter.. </h2>
    <p style="text-align:left">
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

<div class="signature">
<p>Someone who cares<br>
and knows exactly what's he's doing. 💖</p>
</div>
    </p>
    <button onclick="nextPage(8)">i love you...</button>
    <button onclick="nextPage(5)">Back</button>
  </div>
</div>

<!-- PAGE 8 -->
<div id="page8" class="page">
  <div class="card">
    <h3>This vault unlocks only when love is mutual.<br>Say I love you too</h3>
    <input type="text" id="loveMessage" placeholder="Type here...">
    <br>
    <button onclick="checkLoveMessage()">Submit</button>
    <button onclick="nextPage(7)">Back</button>
    <p id="loveError" class="error"></p>
  </div>
</div>

<!-- PAGE 9 -->
<div id="page9" class="page">
  <div class="card">
    <h2>Revealing something...</h2>
    <div id="hintText" class="reveal-text">
      Nooki irunno ipo varum...
    </div>
    <button onclick="nextPage(8)">Back</button>
  </div>
</div>

<script>
function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));
  setTimeout(()=>{
    document.getElementById('page'+num).classList.add('show');
    window.scrollTo({top:0, behavior:"smooth"});
  },300);
}

// Enhanced Name Check with Fireworks
function checkName(){
  let name = document.getElementById("nameInput").value;
  if(name === "afrin" || name === "Afrin" || name === "AFRIN"){
    // Trigger fireworks first
    createFireworks();
    setTimeout(()=>{
      nextPage(3);
      setTimeout(()=>nextPage(4),2000);
    }, 3500); // Let fireworks finish
  } else {
    document.getElementById("error").innerText =
      "YOU MAY BEAUTIFUL BUT NOT THE ONE I CHOSE TO LOVE";
  }
}

// Fireworks Animation - Medium speed bursts
function createFireworks(){
  const fireworks = document.getElementById('fireworks');
  fireworks.classList.add('show');
  
  // Multiple firework bursts
  for(let burst=0; burst<8; burst++){
    setTimeout(()=>launchFirework(), burst*400);
  }
  
  setTimeout(()=>fireworks.classList.remove('show'), 4000);
}

function launchFirework(){
  const fireworks = document.getElementById('fireworks');
  const firework = document.createElement('div');
  firework.className = 'firework';
  
  // Random colors
  const colors = ['#00f2fe', '#ff00cc', '#ffd700', '#ff69b4', '#00ff7f', '#ff1493'];
  const color = colors[Math.floor(Math.random()*colors.length)];
  firework.style.background = color;
  
  // Random launch position
  const x = Math.random() * window.innerWidth;
  const y = window.innerHeight + 50;
  firework.style.left = x + 'px';
  firework.style.top = y + 'px';
  
  fireworks.appendChild(firework);
  
  // Launch upward
  let progress = 0;
  const riseInterval = setInterval(()=>{
    progress += 3;
    firework.style.transform = `translateY(-${progress*8}px)`;
    
    if(progress >= 50){
      clearInterval(riseInterval);
      explodeFirework(firework, x, progress*8);
    }
  }, 30);
}

function explodeFirework(firework, x, height){
  firework.style.width = '4px';
  firework.style.height = '4px';
  
  // Create explosion particles
  for(let i=0; i<25; i++){
    const particle = document.createElement('div');
    particle.className = 'firework-explosion';
    particle.style.left = x + 'px';
    particle.style.top = (height + window.scrollY) + 'px';
    
    const angle = (i / 25) * Math.PI * 2;
    const velocity = 150 + Math.random() * 100;
    const size = 3 + Math.random() * 4;
    
    const color = firework.style.backgroundColor || '#00f2fe';
    particle.style.background = color;
    particle.style.width = size + 'px';
    particle.style.height = size + 'px';
    particle.style.boxShadow = `0 0 ${size*2}px ${color}`;
    
    document.getElementById('fireworks').appendChild(particle);
    
    // Particle explosion physics
    let vx = Math.cos(angle) * velocity;
    let vy = Math.sin(angle) * velocity;
    let life = 100;
    
    const particleInterval = setInterval(()=>{
      vx *= 0.98; // Friction
      vy += 4; // Gravity
      
      particle.style.left = (parseFloat(particle.style.left) + vx * 0.02) + 'px';
      particle.style.top = (parseFloat(particle.style.top) + vy * 0.02) + 'px';
      
      life -= 2;
      particle.style.opacity = life / 100;
      particle.style.transform = `scale(${life/100})`;
      
      if(life <= 0){
        clearInterval(particleInterval);
        particle.remove();
      }
    }, 20);
  }
  
  // Remove rocket
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

// Continuous floating particles
setInterval(()=>{
  const particle = document.createElement('div');
  particle.className = 'particle';
  particle.style.left = (Math.random() * 100) + 'vw';
  particle.style.animationDuration = (6 + Math.random() * 4) + 's';
  document.body.appendChild(particle);
  
  setTimeout(()=>particle.remove(), 10000);
}, 800);
</script>

</body>
</html>