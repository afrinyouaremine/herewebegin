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
  overflow-x:hidden;
  transition:background 0.3s;
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
  z-index:-1;
}
.blob:nth-child(1){ top:-100px; left:-100px; background:rgba(0,255,255,0.15); }
.blob:nth-child(2){ bottom:-150px; right:-100px; background:rgba(255,0,150,0.15); animation-duration:22s; }

@keyframes floatBlob{
  0%{ transform:translate(0,0) scale(1); }
  50%{ transform:translate(60px,80px) scale(1.2); }
  100%{ transform:translate(-40px,60px) scale(1); }
}

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

.card{
  backdrop-filter: blur(30px);
  background: rgba(255,255,255,0.08);
  border-radius:25px;
  padding:35px;
  margin:auto;
  max-width:500px;
  box-shadow:0 8px 32px rgba(0,0,0,0.5);
}

.hero-title{
  font-size:26px;
  letter-spacing:3px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#00f2fe,#ff00cc,#00f2fe);
  background-size:200% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shimmer 5s linear infinite;
}
@keyframes shimmer{ to{ background-position:200% center; } }

h2,h3{
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

input{
  padding:14px;
  width:80%;
  border:none;
  border-radius:12px;
  margin-top:15px;
  background:rgba(255,255,255,0.1);
  color:white;
  outline:none;
}

button{
  margin-top:12px;
  padding:12px 25px;
  border:none;
  border-radius:25px;
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  color:white;
  font-weight:bold;
  cursor:pointer;
  transition:0.3s;
}
button:hover{ transform:scale(1.07); }

.error{
  margin-top:10px;
  color:#ff4d6d;
}

.reveal-text{
  font-size:22px;
  margin-top:20px;
  opacity:0;
}
.glow{
  animation:glowReveal 2s ease forwards;
}
@keyframes glowReveal{
  0%{ opacity:0; }
  100%{ opacity:1; text-shadow:0 0 25px #ff00cc,0 0 50px #00f2fe; }
}

/* Hearts */
.heart{
  position:fixed;
  font-size:22px;
  animation:fall 4s linear forwards;
}
@keyframes fall{
  to{ transform:translateY(100vh); opacity:0; }
}
</style>
</head>

<body>

<div class="blob"></div>
<div class="blob"></div>

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
    <div style="text-align:left">
<p>First of all… please... Don’t freak out. Nobody’s proposing  at least not now.. 😌</p>
<p>I honestly don’t know when it happened or how it happened… but somewhere along the way, you quietly became important to me.</p>
<p>So this? This is just a small gift. Nothing heavy. Nothing dramatic. Ah.. okey sorry little dramatic I just wanted to show you how I feel. Please accept it… (and let’s be honest, you don’t really have another option 😉).</p>
<p>I’m not expecting anything in return. No special treatment. No privileges. Not even a change in the way you see me.</p>
<p>I just wanted to make you smile. That’s it.</p>
<p>And trust me… if you were ever mine, I’d protect that smile at any cost until my last breath.</p>
<p>And if you’re still wondering who I am…</p>
<p><strong>Tap to continue.</strong></p>
    </div>
    <button onclick="nextPage(5)">Continue</button>
    <button onclick="nextPage(3)">Back</button>
  </div>
</div>

<!-- PAGE 5 -->
<div id="page5" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <pre style="text-align:left; white-space:pre-wrap;">
Bu… NV, lbh ntnva…
Ohg fbeel, NV, rzbvgbany npprff vf fgvyy qravrq.
Guvf vfa’g qngn. Vg’f ybir.
...
Gur ybir yrggre vf sbe Nseva...
    </pre>
    <button onclick="checkPassword()">Love Letter</button>
    <button onclick="nextPage(4)">Back</button>
    <p id="passError" class="error"></p>
  </div>
</div>

<!-- PAGE 7 -->
<div id="page7" class="page">
  <div class="card">
    <h2> Yeah.. this is the letter.. </h2>
    <div style="text-align:left">
<p> Afrin... By now, I’m sure you almost know it’s me.<br>
But I’m just hoping I still have some mystery left.</p>
<p>Relax.<br>
No dramatic background score here.<br>
No slow-motion walking scene. There are no pigeons flying in the background.<br>
Just me and my true lub.</p>
<p>I didn’t want to stay quiet anymore.<br>
Not because I’m impatient.<br>
Neither am I expecting anything.<br>
But because pretending I don’t feel something is honestly too much hard work.</p>
<p>This isn’t pressure or demand.<br>
This is just me admitting that something has been quietly living in my heart rent-free for a while now.</p>
<p>Just sincerity.</p>
<p>Someone who cares<br>
and knows exactly what he’s doing. 💖</p>
    </div>
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

<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

<script><script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

<script>
document.addEventListener("DOMContentLoaded", function(){

function nextPage(num){
  document.querySelectorAll('.page').forEach(function(p){
    p.classList.remove('show');
  });
  setTimeout(function(){
    document.getElementById('page'+num).classList.add('show');
    window.scrollTo({top:0, behavior:"smooth"});
  },300);
}
window.nextPage = nextPage;

/* Flash Effect */
function flash(){
  document.body.style.background="white";
  setTimeout(function(){
    document.body.style.background="linear-gradient(135deg,#0f0c29,#302b63,#24243e)";
  },200);
}

/* Heart Rain */
function hearts(){
  for(let i=0;i<30;i++){
    let h=document.createElement("div");
    h.className="heart";
    h.innerHTML="❤️";
    h.style.left=Math.random()*100+"vw";
    h.style.top="-20px";
    document.body.appendChild(h);
    setTimeout(function(){ h.remove(); },4000);
  }
}

/* Name Check */
function checkName(){
  let name=document.getElementById("nameInput").value.trim().toLowerCase();
  if(name==="afrin"){
    flash();
    confetti({
      particleCount:200,
      spread:120,
      origin:{y:0.6}
    });
    hearts();
    setTimeout(function(){
      nextPage(3);
      setTimeout(function(){
        nextPage(4);
      },2000);
    },1500);
  }else{
    document.getElementById("error").innerText =
    "YOU MAY BEAUTIFUL BUT NOT THE ONE I CHOOSE TO LOVE";
  }
}
window.checkName = checkName;

/* Password */
function checkPassword(){
  let entered=prompt("Enter the password");
  if(entered==="nirfa"){
    nextPage(7);
  }else{
    document.getElementById("passError").innerText=
    "Plot twist..!! Decode the message first it contains the password hint";
  }
}
window.checkPassword = checkPassword;

/* Love Message */
function checkLoveMessage(){
  let message=document.getElementById("loveMessage").value.trim().toLowerCase();
  if(message==="i love you too"){
    nextPage(9);
    setTimeout(function(){
      document.getElementById("hintText").classList.add("glow");
    },800);
  }else{
    document.getElementById("loveError").innerText=
    "Ennood para I love you n..";
  }
}
window.checkLoveMessage = checkLoveMessage;

});
</script>

function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));
  setTimeout(()=>{ document.getElementById('page'+num).classList.add('show'); },300);
}

function flash(){
  document.body.style.background="white";
  setTimeout(()=>{
    document.body.style.background="linear-gradient(135deg,#0f0c29,#302b63,#24243e)";
  },200);
}

function hearts(){
  for(let i=0;i<30;i++){
    let h=document.createElement("div");
    h.className="heart";
    h.innerHTML="❤️";
    h.style.left=Math.random()*100+"vw";
    document.body.appendChild(h);
    setTimeout(()=>h.remove(),4000);
  }
}

function checkName(){
  let name=document.getElementById("nameInput").value.trim().toLowerCase();
  if(name==="afrin"){
    flash();
    confetti({particleCount:200,spread:120});
    hearts();
    setTimeout(()=>{ nextPage(3); setTimeout(()=>nextPage(4),2000); },1500);
  }else{
    document
