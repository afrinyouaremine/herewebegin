<!DOCTYPE html>
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
}

/* Fade In */
body{
  animation:fadeIn 1.5s ease forwards;
}
@keyframes fadeIn{
  from{opacity:0;}
  to{opacity:1;}
}

/* Floating Romantic Particles */
.particle{
  position:fixed;
  width:6px;
  height:6px;
  background:rgba(255,255,255,0.5);
  border-radius:50%;
  animation:floatUp 10s linear infinite;
  z-index:-1;
}
@keyframes floatUp{
  0%{transform:translateY(100vh) scale(0.5); opacity:0;}
  50%{opacity:1;}
  100%{transform:translateY(-10vh) scale(1.2); opacity:0;}
}

/* Glass Card */
.card{
  backdrop-filter: blur(40px);
  background: rgba(255,255,255,0.08);
  border-radius:30px;
  padding:40px 25px;
  width:90%;
  max-width:520px;
  margin:auto;
  margin-top:20vh;
  box-shadow:0 20px 50px rgba(0,0,0,0.6);
  animation:zoomIn 1s ease;
  text-align:center;
}
@keyframes zoomIn{
  from{transform:scale(0.9); opacity:0;}
  to{transform:scale(1); opacity:1;}
}

/* Title Shimmer */
.hero-title{
  font-size:22px;
  letter-spacing:3px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#00f2fe,#ff00cc,#00f2fe);
  background-size:200% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shimmer 4s linear infinite;
}
@keyframes shimmer{
  to{ background-position:200% center; }
}

/* Heartbeat Effect */
.heartbeat{
  font-size:40px;
  animation:beat 1.2s infinite;
}
@keyframes beat{
  0%,100%{transform:scale(1);}
  50%{transform:scale(1.2);}
}

/* Button */
button{
  margin-top:20px;
  padding:14px 28px;
  border:none;
  border-radius:30px;
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  color:white;
  font-weight:bold;
  font-size:15px;
  cursor:pointer;
  transition:0.3s;
}
button:hover{ transform:scale(1.1); }

/* Decode Text */
.decode{
  font-family:monospace;
  white-space:pre-wrap;
  font-size:15px;
  text-align:left;
  min-height:120px;
  margin-top:20px;
}

</style>
</head>

<body>

<!-- Background Music -->
<audio id="bgMusic" loop>
  <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_c8c8a73467.mp3?filename=romantic-ambient-piano-110624.mp3" type="audio/mpeg">
</audio>

<div class="card" id="page1">
  <h1 class="hero-title">HERE WE BEGIN OUR LOVE STORY</h1>
  <p id="typeText"></p>
  <div class="heartbeat">❤️</div>
  <button onclick="startLove()">YES I'M THE ONE YOU WAITING FOR</button>
</div>

<div class="card" id="page2" style="display:none;">
  <h2>Decrypting Message...</h2>
  <div id="decodeText" class="decode"></div>
  <button onclick="revealFinal()">Continue</button>
</div>

<div class="card" id="page3" style="display:none;">
  <h2>Hint Revealing...</h2>
  <p style="font-size:18px;">
    Almost you got me right..? It's two digit common between us.
  </p>
</div>

<script>

/* Start Music on First Click (Mobile Safe) */
function startLove(){
  document.getElementById("bgMusic").play();
  document.getElementById("page1").style.display="none";
  document.getElementById("page2").style.display="block";
  decodeEffect();
}

/* Typing Intro */
const introText = "Emotional Firewall Activated...\nOnly The Love of Life may proceed.";
let i = 0;
function typeWriter(){
  if(i < introText.length){
    document.getElementById("typeText").innerHTML += introText.charAt(i);
    i++;
    setTimeout(typeWriter,40);
  }
}
typeWriter();

/* Romantic Particles */
for(let i=0;i<30;i++){
  let p = document.createElement("div");
  p.className="particle";
  p.style.left=Math.random()*100+"vw";
  p.style.animationDuration=(6+Math.random()*6)+"s";
  document.body.appendChild(p);
}

/* Decoding Animation */
const encrypted = 
"Bu… bxnl, lbh znqr vg guvf sne.\nGuvf vfa’g qngn. Vg’f ybir.\nDecode it if you can...";
let index=0;

function decodeEffect(){
  let output="";
  let interval=setInterval(()=>{
    output += encrypted.charAt(index);
    document.getElementById("decodeText").innerText=output;
    index++;
    if(index>=encrypted.length){
      clearInterval(interval);
    }
  },35);
}

/* Final Reveal */
function revealFinal(){
  document.getElementById("page2").style.display="none";
  document.getElementById("page3").style.display="block";
}

</script>

</body>
</html>