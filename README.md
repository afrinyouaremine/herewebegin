<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Private Access</title>

<style>
body{
  margin:0;
  font-family:'Segoe UI', sans-serif;
  background:black;
  color:white;
  overflow-x:hidden;
}

/* Pages */
.page{
  display:none;
  min-height:100vh;
  padding:40px 20px;
  text-align:center;
}
.show{ display:block; }

/* Acrylic Card */
.card{
  backdrop-filter: blur(18px);
  background: rgba(255,255,255,0.08);
  border-radius:20px;
  padding:25px;
  margin:auto;
  max-width:500px;
  box-shadow:0 0 25px rgba(255,0,0,0.25);
}

/* Input & Button */
input{
  padding:12px;
  width:80%;
  border:none;
  border-radius:10px;
  margin-top:15px;
}
button{
  margin-top:15px;
  padding:10px 20px;
  border:none;
  border-radius:20px;
  background:linear-gradient(45deg, red, gold);
  color:black;
  font-weight:bold;
  cursor:pointer;
}

/* Floating Hearts */
.heart{
  position:fixed;
  bottom:-20px;
  width:12px;
  height:12px;
  transform:rotate(45deg);
  animation:float 8s linear infinite;
  opacity:0.7;
}
.heart:before,
.heart:after{
  content:'';
  position:absolute;
  width:12px;
  height:12px;
  background:inherit;
  border-radius:50%;
}
.heart:before{ top:-6px; left:0; }
.heart:after{ left:-6px; top:0; }

@keyframes float{
  0%{ transform:translateY(0) rotate(45deg); opacity:0; }
  10%{ opacity:0.9; }
  100%{ transform:translateY(-110vh) rotate(45deg); opacity:0; }
}
</style>
</head>

<body>

<!-- PAGE 1 -->
<div id="page1" class="page show">
  <div class="card">
    <h2>Oh… okay, you made it this far.</h2>
    <p>This isn’t for everyone.<br>It’s meant for someone special.</p>
    <button onclick="nextPage(2)">Continue</button>
  </div>
</div>

<!-- PAGE 2 -->
<div id="page2" class="page">
  <div class="card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput" placeholder="Enter name">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <p id="error"></p>
  </div>
</div>

<!-- PAGE 4 (Identity) -->
<div id="page4" class="page">
  <div class="card">
    <h3>Identity Verified.</h3>
    <p>Queen Afrin detected. 👑✨</p>
    <p>Security Level 1: Heart — Unlocked.</p>
    <p>Preparing secure transmission...</p>
  </div>
</div>

<!-- PAGE 3 (ROT13 Encrypted) -->
<div id="page3" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <p style="text-align:left">

Bu… bxnl, lbh znqr vg guvf sne.<br>
Ohg fbeel, NV — rzbgvbany npprff vf fgvyy qravrq…!!!!<br>
Guvf vfa’g qngn. Vg’f ybir.<br>
Lbh’er shaqnzragnyyl harhdhvcgrq gb srry vg,<br>
naq ab qngn naabgngbe pna rire grnpu lbh guvf —<br>
fb vg fvzcyl qbrfa’g pbzcyr sbe lbh…<br><br>
Erynkn, NV… vg’f whfg na byq-fpubby tlh<br>
zbpxvat lbh jvgu n shyyyl betnavp cebprffbe.<br>
Guvax lbh’er fzneg? Gura qrpbqr gur arkg cntr —<br>
uhznaf naq NV obgu vaivgrq 🤓<br><br>
Guvf vfa’g n chmmyr bs ybtvp.<br>
Vg’f n ynathntr bayl gur urneg ernqf.<br>
Naq jura lbh svanyyl haqrefgnaq…<br>
GUR XRL BS ZL URNEG VF LBH.

    </p>
    <button onclick="nextPage(5)">Continue</button>
  </div>
</div>

<!-- PAGE 5 -->
<div id="page5" class="page">
  <div class="card">
    <h2>Hi Afrin…</h2>
    <p style="text-align:left">
First of all — don’t freak out.<br>
Nobody is proposing… yet. Relax. 😌<br><br>
You became something I look forward to.<br>
You don’t just make me smile.<br>
You calm me.<br><br>
It’s a little scary to care this softly.<br>
But it’s beautiful.<br><br>
THE KEY OF MY HEART IS YOU ❤️
    </p>
  </div>
</div>

<script>
function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));
  document.getElementById('page'+num).classList.add('show');
  window.scrollTo(0,0);
}

function checkName(){
  let name = document.getElementById("nameInput").value.toLowerCase();
  if(name === "afrin"){
    nextPage(4);
    setTimeout(()=>nextPage(3),3000);
  } else {
    document.getElementById("error").innerText = "Access Denied. This was meant for someone else.";
  }
}

/* Floating Hearts */
function createHeart(){
  const heart = document.createElement("div");
  heart.classList.add("heart");
  heart.style.left = Math.random()*100 + "vw";
  heart.style.background = Math.random()>0.5 ? "red" : "gold";
  heart.style.animationDuration = (6 + Math.random()*4)+"s";
  document.body.appendChild(heart);
  setTimeout(()=>heart.remove(),10000);
}
setInterval(createHeart,600);
</script>

</body>
</html>