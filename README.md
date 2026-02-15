<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Private Access</title>

<style>
body{
  margin:0;
  font-family:'Segoe UI', sans-serif;
  background:radial-gradient(circle at center, #0a0a0a 0%, #000000 80%);
  color:white;
  overflow-x:hidden;
}

/* Smooth page transition */
.page{
  display:none;
  min-height:100vh;
  padding:40px 20px;
  text-align:center;
  opacity:0;
  transform:translateY(20px);
  transition:all 0.8s ease;
}
.show{
  display:block;
  opacity:1;
  transform:translateY(0);
}

/* Cinematic Glass Card */
.card{
  backdrop-filter: blur(25px);
  background: rgba(255,255,255,0.06);
  border-radius:25px;
  padding:35px;
  margin:auto;
  max-width:500px;
  box-shadow:
    0 0 30px rgba(255,215,0,0.2),
    0 0 60px rgba(255,0,0,0.15);
  animation:fadeIn 1.2s ease;
}

/* Text Glow */
h2, h3{
  background:linear-gradient(45deg, gold, #ff4d4d);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

p{
  line-height:1.7;
}

/* Inputs */
input{
  padding:14px;
  width:80%;
  border:none;
  border-radius:12px;
  margin-top:15px;
  background:rgba(255,255,255,0.1);
  color:white;
  outline:none;
  box-shadow:0 0 10px rgba(255,215,0,0.2);
  transition:0.3s;
}
input:focus{
  box-shadow:0 0 15px gold;
}

/* Buttons */
button{
  margin-top:18px;
  padding:12px 25px;
  border:none;
  border-radius:25px;
  background:linear-gradient(45deg, gold, #ff4d4d);
  color:black;
  font-weight:bold;
  cursor:pointer;
  transition:0.4s;
  box-shadow:0 0 15px rgba(255,215,0,0.4);
}
button:hover{
  transform:scale(1.05);
  box-shadow:0 0 25px gold;
}

/* Subtle Pulse Effect */
@keyframes pulseGlow{
  0%{ text-shadow:0 0 5px gold; }
  50%{ text-shadow:0 0 20px #ff4d4d; }
  100%{ text-shadow:0 0 5px gold; }
}

.highlight{
  animation:pulseGlow 2.5s infinite;
}

/* Fade Animation */
@keyframes fadeIn{
  from{ opacity:0; transform:translateY(15px); }
  to{ opacity:1; transform:translateY(0); }
}
</style>
</head>

<body>

<!-- PAGE 1 -->
<div id="page1" class="page show">
  <div class="card">
    <h2>Someone special left something here for you…</h2>
    <p>
      This isn’t random.<br>
      It’s intentional.<br><br>
      If you feel this might be yours…<br>
      tap below to claim the gift.
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
    <p id="error"></p>
  </div>
</div>

<!-- PAGE 3 -->
<div id="page3" class="page">
  <div class="card">
    <h3>Identity Verified.</h3>
    <p class="highlight">Queen Afrin detected. 👑✨</p>
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

<!-- PAGE 5 -->
<div id="page5" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <p style="text-align:left">
Bu… bxnl, lbh znqr vg guvf sne.<br>
Ohg fbeel, NV — rzbgvbany npprff vf fgvyy qravrq…!!!!<br>
Guvf vfa’g qngn. Vg’f ybir.<br>
Vg’f n ynathntr bayl gur urneg ernqf.<br>
Naq jura lbh svanyyl haqrefgnaq…<br>
GUR XRL BS ZL URNEG VF LBH.
    </p>
    <button onclick="nextPage(6)">Proceed to Final Access</button>
  </div>
</div>

<!-- PAGE 6 -->
<div id="page6" class="page">
  <div class="card">
    <h3>Security Level 2</h3>
    <p>Enter the security code to unlock final access.</p>
    <input type="password" id="securityCode" placeholder="Enter security code">
    <br>
    <button onclick="checkCode()">Unlock</button>
    <p id="codeError"></p>
  </div>
</div>

<!-- PAGE 7 -->
<div id="page7" class="page">
  <div class="card">
    <h2 class="highlight">Final Message</h2>
    <p style="text-align:left">
You don’t just make me smile.<br>
You calm me.<br><br>
It’s a little scary to care this softly.<br>
But it’s beautiful.<br><br>
And if life ever offers me a place beside someone meaningful…<br>
I would quietly hope it’s you.<br><br>
<span class="highlight">THE KEY OF MY HEART IS YOU ❤️</span>
    </p>
  </div>
</div>

<script>
function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>{
    p.classList.remove('show');
  });
  setTimeout(()=>{
    document.getElementById('page'+num).classList.add('show');
    window.scrollTo(0,0);
  },200);
}

function checkName(){
  let name = document.getElementById("nameInput").value.toLowerCase();
  if(name === "afrin"){
    nextPage(3);
    setTimeout(()=>nextPage(4),2500);
  } else {
    document.getElementById("error").innerText =
      "This message was written for someone else.";
  }
}

function checkCode(){
  let code = document.getElementById("securityCode").value.toLowerCase();
  if(code === "nirfa87"){
    nextPage(7);
  } else {
    document.getElementById("codeError").innerText =
      "Incorrect security code. Try again.";
  }
}
</script>

</body>
</html>