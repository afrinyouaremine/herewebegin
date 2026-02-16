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

/* Cinematic Fade In */
body{
  animation:cinemaIntro 1.5s ease forwards;
}
@keyframes cinemaIntro{
  from{ opacity:0; }
  to{ opacity:1; }
}

/* Floating Acrylic Motion */
.blob{
  position:fixed;
  width:400px;
  height:400px;
  border-radius:50%;
  filter:blur(100px);
  animation:floatBlob 20s infinite alternate ease-in-out;
  z-index:-1;
}
.blob:nth-child(1){ top:-100px; left:-100px; background:rgba(0,255,255,0.18); }
.blob:nth-child(2){ bottom:-150px; right:-100px; background:rgba(255,0,150,0.18); }

@keyframes floatBlob{
  0%{ transform:translate(0,0) scale(1); }
  50%{ transform:translate(80px,60px) scale(1.2); }
  100%{ transform:translate(-60px,80px) scale(1); }
}

/* Page Transition */
.page{
  position:absolute;
  width:100%;
  min-height:100vh;
  padding:40px 20px;
  display:flex;
  justify-content:center;
  align-items:center;
  text-align:center;
  opacity:0;
  transform:scale(1.05);
  transition:all 0.8s ease;
}
.show{
  opacity:1;
  transform:scale(1);
  z-index:2;
}

/* Premium Glass Card */
.card{
  backdrop-filter: blur(40px);
  background: rgba(255,255,255,0.08);
  border-radius:28px;
  padding:40px 25px;
  width:90%;
  max-width:520px;
  box-shadow:0 15px 40px rgba(0,0,0,0.6);
  animation:cardZoom 1s ease;
}
@keyframes cardZoom{
  from{ transform:scale(0.9); opacity:0; }
  to{ transform:scale(1); opacity:1; }
}

/* Titles */
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

h2,h3{
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

/* Inputs */
input{
  padding:16px;
  width:85%;
  border:none;
  border-radius:14px;
  margin-top:15px;
  background:rgba(255,255,255,0.12);
  color:white;
  font-size:16px;
  outline:none;
  transition:0.4s;
}
input:focus{
  box-shadow:0 0 20px #ff00cc, 0 0 35px #00f2fe;
  transform:scale(1.04);
}

/* Buttons */
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

.error{
  margin-top:10px;
  color:#ff4d6d;
}

/* Cinematic Text Reveal */
.reveal-text{
  font-size:20px;
  opacity:0;
  transform:translateY(20px);
}
.glow{
  animation:cinematicReveal 2s ease forwards;
}
@keyframes cinematicReveal{
  0%{ opacity:0; transform:translateY(30px); text-shadow:0 0 0px #fff; }
  50%{ opacity:0.6; text-shadow:0 0 30px #ff00cc; }
  100%{ opacity:1; transform:translateY(0); text-shadow:0 0 50px #00f2fe; }
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
    <p id="typeText"></p>
    <button onclick="nextPage(2)">YES I'M THE ONE YOU WAITING FOR</button>
  </div>
</div>

<!-- PAGE 9 FINAL -->
<div id="page9" class="page">
  <div class="card">
    <h2>Hint Revealing...</h2>
    <div id="hintText" class="reveal-text">
      Almost you got me right..? It's two digit common between us.
    </div>
  </div>
</div>

<script>

/* Cinematic Typing Effect */
const text = "Emotional Firewall Activated...\nOnly The Love of Life may proceed.";
let i = 0;
function typeWriter(){
  if(i < text.length){
    document.getElementById("typeText").innerHTML += text.charAt(i);
    i++;
    setTimeout(typeWriter,40);
  }
}
typeWriter();

/* Smooth Page Transition */
function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));
  setTimeout(()=>{
    document.getElementById('page'+num).classList.add('show');
    window.scrollTo({top:0});
  },400);
}

/* Dramatic Glow Trigger */
function revealHint(){
  nextPage(9);
  setTimeout(()=>{
    document.getElementById("hintText").classList.add("glow");
  },800);
}
</script>

</body>
</html>