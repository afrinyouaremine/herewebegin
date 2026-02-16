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
  z-index:-2;
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
  transition:opacity 0.6s ease;
  z-index:5;
}
.cinema-overlay.active{
  opacity:0.6;
}

/* Page Animation */
.page{
  display:none;
  min-height:100vh;
  padding:40px 20px;
  text-align:center;
  opacity:0;
  transform:scale(1.05);
  transition:opacity 0.6s ease, transform 0.6s ease;
}
.show{
  display:block;
  opacity:1;
  transform:scale(1);
}

/* Card */
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
  width:80%;
  border:none;
  border-radius:12px;
  margin-top:15px;
  background:rgba(255,255,255,0.1);
  color:white;
  outline:none;
}

/* Button */
button{
  margin-top:18px;
  padding:12px 25px;
  border:none;
  border-radius:25px;
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  color:white;
  font-weight:bold;
  cursor:pointer;
}

.error{
  margin-top:10px;
  color:#ff4d6d;
}

/* Dramatic Reveal */
.reveal-text{
  font-size:22px;
  margin-top:20px;
  opacity:0;
  transform:scale(0.8);
}
.glow{
  animation:glowReveal 2s ease forwards;
}
@keyframes glowReveal{
  0%{ opacity:0; transform:scale(0.8); }
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
  z-index:-1;
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

<!-- ALL YOUR ORIGINAL PAGES 1–9 EXACTLY AS YOU WROTE THEM -->
<!-- (Content unchanged for brevity — keep your exact page HTML here) -->

<script>

function nextPage(num){
  let overlay = document.getElementById("overlay");
  overlay.classList.add("active");

  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));

  setTimeout(()=>{
    document.getElementById('page'+num).classList.add('show');
    window.scrollTo({top:0, behavior:"smooth"});
    overlay.classList.remove("active");
  },500);
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
    },800);
  } else {
    document.getElementById("loveError").innerText =
      "Hint veno..? enna ennood para i love you n.";
  }
}

/* Floating Light Particles */
for(let i=0;i<25;i++){
  let l=document.createElement("div");
  l.className="light";
  l.style.left=Math.random()*100+"vw";
  l.style.animationDuration=(6+Math.random()*8)+"s";
  document.body.appendChild(l);
}

</script>

</body>
</html>