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
  height:100vh;
  overflow:hidden;
}

/* Floating Acrylic Motion */
.blob{
  position:fixed;
  width:400px;
  height:400px;
  background:rgba(255,255,255,0.05);
  border-radius:50%;
  filter:blur(80px);
  animation:floatBlob 18s infinite alternate ease-in-out;
  z-index:-3;
}
.blob:nth-child(1){ top:-100px; left:-100px; background:rgba(0,255,255,0.15); }
.blob:nth-child(2){ bottom:-150px; right:-100px; background:rgba(255,0,150,0.15); animation-duration:22s; }

@keyframes floatBlob{
  0%{ transform:translate(0,0) scale(1); }
  50%{ transform:translate(60px,80px) scale(1.2); }
  100%{ transform:translate(-40px,60px) scale(1); }
}

/* Cinematic Overlay */
.cinema-overlay{
  position:fixed;
  inset:0;
  background:black;
  opacity:0;
  pointer-events:none;
  transition:opacity 0.5s ease;
  z-index:1;
}
.cinema-overlay.active{
  opacity:0.4;
}

/* Page (Mobile Safe) */
.page{
  position:absolute;
  inset:0;
  padding:30px 18px;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
  opacity:0;
  visibility:hidden;
  transform:translateY(20px);
  transition:opacity 0.5s ease, transform 0.5s ease;
}

.show{
  opacity:1;
  visibility:visible;
  transform:translateY(0);
}

/* Card */
.card{
  backdrop-filter: blur(25px);
  background: rgba(255,255,255,0.08);
  border-radius:22px;
  padding:28px 20px;
  width:100%;
  max-width:480px;
  box-shadow:0 10px 30px rgba(0,0,0,0.5);
}

/* Titles */
.hero-title{
  font-size:22px;
  letter-spacing:2px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#00f2fe,#ff00cc,#00f2fe);
  background-size:200% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shimmer 5s linear infinite;
}
@keyframes shimmer{
  to{ background-position:200% center; }
}

h2,h3{
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

/* Input */
input{
  padding:14px;
  width:100%;
  border:none;
  border-radius:12px;
  margin-top:15px;
  background:rgba(255,255,255,0.1);
  color:white;
  outline:none;
  font-size:15px;
}

/* Button */
button{
  margin-top:18px;
  padding:16px 26px;
  border:none;
  border-radius:30px;
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  color:white;
  font-weight:bold;
  font-size:16px;
  cursor:pointer;
  width:100%;
  max-width:280px;
}

.error{
  margin-top:10px;
  color:#ff4d6d;
}

/* Dramatic Reveal */
.reveal-text{
  font-size:20px;
  margin-top:20px;
  opacity:0;
  transform:scale(0.9);
}
.glow{
  animation:glowReveal 2s ease forwards;
}
@keyframes glowReveal{
  0%{ opacity:0; transform:scale(0.9); }
  100%{ opacity:1; transform:scale(1); text-shadow:0 0 25px #ff00cc,0 0 50px #00f2fe; }
}

/* Floating Light Particles */
.light{
  position:fixed;
  width:4px;
  height:4px;
  background:rgba(255,255,255,0.6);
  border-radius:50%;
  pointer-events:none;
  animation:floatLight linear infinite;
  z-index:-2;
}
@keyframes floatLight{
  from{transform:translateY(100vh) scale(0.5); opacity:0;}
  30%{opacity:1;}
  to{transform:translateY(-10vh) scale(1.2); opacity:0;}
}
</style>
</head>

<body>

<div class="cinema-overlay" id="overlay"></div>
<div class="blob"></div>
<div class="blob"></div>

<!-- PAGE 1 -->
<div id="page1" class="page show">
  <div class="card">
    <h1 class="hero-title">HERE WE BEGIN OUR LOVE STORY</h1>
    <p>
      Emotional Firewall Activated.<br><br>
      Only The Love of Life may proceed.<br><br>
      Think you are the one?<br>
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
    <button onclick="checkName()">Claim Access</button>
    <p id="error" class="error"></p>
  </div>
</div>

<!-- PAGE 3 -->
<div id="page3" class="page">
  <div class="card">
    <h3>Identity Confirmed…</h3>
    <p>Princess of my heart detected ✨</p>
    <p>Security Level 1: Heart — Unlocked.</p>
  </div>
</div>

<!-- PAGE 4 -->
<div id="page4" class="page">
  <div class="card">
    <h2>Hi Afrin…</h2>
    <p style="text-align:left">
First of all — don’t freak out.<br>
Nobody is proposing… yet. Relax. 😌<br><br>
I just needed a small moment of honesty.<br>
I Don't know how,when,where.... <br><br>
you quietly became important to me.
    </p>
    <button onclick="nextPage(5)">Continue</button>
  </div>
</div>

<!-- PAGE 5 -->
<div id="page5" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <pre style="text-align:left; white-space:pre-wrap; font-family:monospace;">
Bu… bxnl, lbh znqr vg guvf sne.
Guvf vfa’g qngn. Vg’f ybir.
    </pre>
    <button onclick="nextPage(6)">Enter Passcode to Continue</button>
  </div>
</div>

<!-- PAGE 6 -->
<div id="page6" class="page">
  <div class="card">
    <h3>Enter Passcode</h3>
    <input type="password" id="securityCode" placeholder="Enter passcode">
    <button onclick="checkCode()">Unlock</button>
    <p id="codeError" class="error"></p>
  </div>
</div>

<!-- PAGE 7 -->
<div id="page7" class="page">
  <div class="card">
    <h2>DECODE MY HEART IF YOU CAN</h2>
    <button onclick="nextPage(8)">DECODE HINT</button>
  </div>
</div>

<!-- PAGE 8 -->
<div id="page8" class="page">
  <div class="card">
    <h3>ENNOOD PARA I LOVE YOU NU..</h3>
    <input type="text" id="loveMessage" placeholder="Type here...">
    <button onclick="checkLoveMessage()">Submit</button>
    <p id="loveError" class="error"></p>
  </div>
</div>

<!-- PAGE 9 -->
<div id="page9" class="page">
  <div class="card">
    <h2>Hint Revealing...</h2>
    <div id="hintText" class="reveal-text">
      Almost you got me right..? It's two digit common between us
    </div>
  </div>
</div>

<script>
function nextPage(num){
  let overlay = document.getElementById("overlay");
  overlay.classList.add("active");

  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));

  setTimeout(()=>{
    document.getElementById('page'+num).classList.add('show');
    overlay.classList.remove("active");
  },400);
}

function checkName(){
  let name = document.getElementById("nameInput").value.toLowerCase();
  if(name === "afrin"){
    nextPage(3);
    setTimeout(function(){ nextPage(4); },2000);
  } else {
    document.getElementById("error").innerText =
      "Identity mismatch. Either typo… or espionage.";
  }
}

function checkCode(){
  let code = document.getElementById("securityCode").value.toLowerCase();
  if(code === "nirfa"){
    nextPage(7);
  } else {
    document.getElementById("codeError").innerText =
      "SAY I LOVE YOU...";
  }
}

function checkLoveMessage(){
  let message = document.getElementById("loveMessage").value.trim().toLowerCase();
  if(message === "i love you"){
    nextPage(9);
    setTimeout(()=>{
      document.getElementById("hintText").classList.add("glow");
    },600);
  } else {
    document.getElementById("loveError").innerText =
      "Hint veno..? enna ennood para i love you n.";
  }
}

for(let i=0;i<20;i++){
  let l=document.createElement("div");
  l.className="light";
  l.style.left=Math.random()*100+"vw";
  l.style.animationDuration=(6+Math.random()*6)+"s";
  document.body.appendChild(l);
}
</script>

</body>
</html>