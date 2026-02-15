<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Here We Begin Our Love Story</title>

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
  transform:translateY(30px);
  transition:all 0.8s ease;
}
.show{
  display:block;
  opacity:1;
  transform:translateY(0);
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
@keyframes shimmer{
  to{ background-position:200% center; }
}

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
}

button{
  margin-top:18px;
  padding:12px 25px;
  border:none;
  border-radius:25px;
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  color:white;
  font-weight:bold;
  cursor:pointer;
  transition:0.4s;
}
button:hover{ transform:scale(1.07); }

.error{ margin-top:10px; color:#ff4d6d; }
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
    <button onclick="nextPage(2)">Tap to Claim</button>
  </div>
</div>

<!-- PAGE 2 -->
<div id="page2" class="page">
  <div class="card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput" placeholder="Enter name">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <p id="error" class="error"></p>
  </div>
</div>

<!-- PAGE 3 -->
<div id="page3" class="page">
  <div class="card">
    <h3>Identity Confirmed…</h3>
    <p>My Princess Afrin detected ✨</p>
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
Somewhere between normal days and random thoughts,<br>
you quietly became important to me.
    </p>
    <button onclick="nextPage(5)">Continue</button>
  </div>
</div>

<!-- PAGE 5 ENCRYPTED -->
<div id="page5" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <pre style="text-align:left; white-space:pre-wrap; font-family:monospace;">
Bu… bxnl, lbh znqr vg guvf sne.
Ohg fbeel, NV — rzbgvbany npprff vf fgvyy qravrq…!!!!
Guvf vfa’g qngn. Vg’f ybir.
Lbh’er shaqnznragnyyl harpdhvccrq gb srry vg,
naq ab qngn naabgngbe pna rire grnpu lbh guvf —
fb vg fvycyl qbrfa’g pbzcvyr sbe lbh…
Eryn k, NV…
vg’f whfg na byq-fpubby thl
zbpxvat lbh jvgu n shyy beqnavp cebprffbe.
Guvax lbh’er fzneg? Gura qrpbqr gur arkg cntr —
uhznaf naq NV obgu vaivgrq 🤓
Ohg haqrefgnaq…
Guvf vfa’g n chmmyr bs ybtvp.
Vg’f n ynathntr bayl gur urneg ernqf.
Fbzr pbaarpgvbaf nera’g cebtenzzrq.
Fbzr zrnavatf nera’g jevggra va pbqr.
Gurl nccrne dhvgryl…
jura bar fbhy erpbttavmrf nabgure.
Sevraqyl pnhgvba:
na vtaberag zvaqfrg penfuref snfgre guna ohttl pbqr.
Ybtvp urycf n yvggyr…
ohg ybir naq cngvrapr ner jung ge hyl haybpx guvf flfgrz ❤️
Nseva…
Nytbevguzf znl pnyphyngr.
Znpurvarf znl cerqvpg.
GUR XRL BS ZL URNEG VF LBH...
    </pre>
    <button onclick="nextPage(6)">Proceed to Final Access</button>
  </div>
</div>

<!-- Remaining pages unchanged exactly as your original -->

<script>
function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));
  setTimeout(()=>{
    document.getElementById('page'+num).classList.add('show');
    window.scrollTo(0,0);
  },200);
}

function checkName(){
  let name = document.getElementById("nameInput").value.toLowerCase();
  if(name === "afrin"){
    nextPage(3);
    setTimeout(()=>nextPage(4),2000);
  } else {
    document.getElementById("error").innerText =
      "Identity mismatch. Either typo… or espionage.";
  }
}

function checkCode(){
  let code = document.getElementById("securityCode").value.toLowerCase();
  if(code === "nirfa"){
    nextPage(7);
    loadTracking();
  } else {
    document.getElementById("codeError").innerText =
      "That code unlocked nothing. Try reversing your thinking.";
  }
}

function checkLove(){
  let phrase = document.getElementById("loveConfirm").value.toLowerCase().trim();
  if(phrase === "love you too"){
    nextPage(9);
  } else {
    document.getElementById("loveError").innerText =
      "That’s not the phrase I was hoping to hear…";
  }
}

function loadTracking(){
  let device = /mobile/i.test(navigator.userAgent) ? "Mobile 📱" : "Desktop 💻";
  document.getElementById("deviceInfo").innerText =
    "Device Detected: " + device;

  let now = new Date();
  document.getElementById("timeInfo").innerText =
    "Connection Time: " + now.toLocaleString();

  let visits = localStorage.getItem("visitCount");
  visits = visits ? parseInt(visits)+1 : 1;
  localStorage.setItem("visitCount", visits);

  document.getElementById("visitCount").innerText =
    "You have visited this page " + visits + " time(s).";
}
</script>

</body>
</html>