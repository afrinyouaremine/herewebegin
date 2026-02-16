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
  z-index:-1;
}
.blob:nth-child(1){ top:-100px; left:-100px; background:rgba(0,255,255,0.15); }
.blob:nth-child(2){ bottom:-150px; right:-100px; background:rgba(255,0,150,0.15); animation-duration:22s; }

@keyframes floatBlob{
  0%{ transform:translate(0,0) scale(1); }
  50%{ transform:translate(60px,80px) scale(1.2); }
  100%{ transform:translate(-40px,60px) scale(1); }
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

/* Card Animation */
.card{
  backdrop-filter: blur(30px);
  background: rgba(255,255,255,0.08);
  border-radius:25px;
  padding:35px;
  margin:auto;
  max-width:500px;
  box-shadow:0 8px 32px rgba(0,0,0,0.5);
  animation:cardPop 0.9s ease;
}

@keyframes cardPop{
  0%{ transform:scale(0.9); opacity:0; }
  100%{ transform:scale(1); opacity:1; }
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
  outline:none;
  transition:0.4s;
}
input:focus{
  box-shadow:0 0 15px #ff00cc, 0 0 25px #00f2fe;
  transform:scale(1.03);
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
  transition:0.3s;
}
button:hover{ transform:scale(1.07); }

.error{
  margin-top:10px;
  color:#ff4d6d;
  animation:shake 0.3s ease;
}
@keyframes shake{
  0%,100%{ transform:translateX(0); }
  25%{ transform:translateX(-5px); }
  75%{ transform:translateX(5px); }
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
    <button onclick="nextPage(2)">YES I'M THE ONE YOU WAITINGFOR</button>
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
    <p> Princess of my heart detected ✨</p>
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
I Don't know how,when,where ,<br>
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
Ohg fbeel, NV — rzbvfgvbany npprff vf fgvyy qravrq…!!!!
Guvf vfa’g qngn. Vg’f ybir.
...
GUR 'LRX' BS ZL URNEG VF LBH.
    </pre>
    <button onclick="nextPage(6)">Enter Passcode to Continue</button>
  </div>
</div>

<!-- PAGE 6 -->
<div id="page6" class="page">
  <div class="card">
    <h3>Enter Passcode to Continue</h3>
    <input type="password" id="securityCode" placeholder="Enter passcode">
    <br>
    <button onclick="checkCode()">Unlock</button>
    <p id="codeError" class="error"></p>
  </div>
</div>

<!-- PAGE 7 -->
<div id="page7" class="page">
  <div class="card">
    <h2> DECODE MY HEART IF YOU CAN </h2>
    <p style="text-align:left">
(Your FULL encrypted letter exactly as you wrote it here — unchanged)
    </p>

    <br><br>
    <button onclick="showHintPrompt()">Decode Hint</button>

    <div id="hintSection" style="display:none; margin-top:20px;">
      <input type="text" id="loveConfirm" placeholder="Type LOVE YOU TOO">
      <br>
      <button onclick="checkLove()">Reveal Hint</button>
      <p id="loveError" class="error"></p>
      <p id="realHint" style="display:none; margin-top:15px;">
        Hint: Try shifting letters forward in the alphabet… 
        or maybe it's the reverse of something you already saw 😉
      </p>
    </div>

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

function checkName(){
  let name = document.getElementById("nameInput").value.toLowerCase();
  if(name === "afrin"){
    nextPage(3);
    setTimeout(()=>nextPage(4),2000);
  } else {
    document.getElementById("error").innerText =
      "That's not you 👀 FBI mode activated. Try again, Agent.";
  }
}

function checkCode(){
  let code = document.getElementById("securityCode").value.toLowerCase();
  if(code === "nirfa"){
    nextPage(7);
  } else {
    document.getElementById("codeError").innerText =
      "Nope 😌 Even Google couldn't guess that one. Try again.";
  }
}

function showHintPrompt(){
  document.getElementById("hintSection").style.display = "block";
}

function checkLove(){
  let love = document.getElementById("loveConfirm").value.trim().toLowerCase();
  if(love === "love you too"){
    document.getElementById("realHint").style.display = "block";
    document.getElementById("loveError").innerText = "";
  } else {
    document.getElementById("loveError").innerText =
      "Wrong password 😭 Did autocorrect break your feelings too?";
  }
}
</script>

</body>
</html>