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
}

.page{
  display:none;
  min-height:100vh;
  padding:40px 20px;
  text-align:center;
}
.show{ display:block; }

.card{
  backdrop-filter: blur(18px);
  background: rgba(255,255,255,0.08);
  border-radius:20px;
  padding:30px;
  margin:auto;
  max-width:500px;
  box-shadow:0 0 25px rgba(255,255,255,0.1);
}

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
  background:linear-gradient(45deg, #ff4d4d, gold);
  color:black;
  font-weight:bold;
  cursor:pointer;
}
</style>
</head>

<body>

<!-- PAGE 1: Welcome -->
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

<!-- PAGE 2: Name Input -->
<div id="page2" class="page">
  <div class="card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput" placeholder="Enter name">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <p id="error"></p>
  </div>
</div>

<!-- PAGE 3: Identity Verification -->
<div id="page3" class="page">
  <div class="card">
    <h3>Identity Verified.</h3>
    <p>Queen Afrin detected. 👑✨</p>
    <p>Security Level 1: Heart — Unlocked.</p>
  </div>
</div>

<!-- PAGE 4: Hi Afrin Message -->
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

<!-- PAGE 5: ROT13 Encrypted -->
<div id="page5" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <p style="text-align:left">

Bu… bxnl, lbh znqr vg guvf sne.<br>
Ohg fbeel, NV — rzbgvbany npprff vf fgvyy qravrq…!!!!<br>
Guvf vfa’g qngn. Vg’f ybir.<br>
Lbh’er shaqnzragnyyl harhdhvcgrq gb srry vg,<br>
naq ab qngn naabgngbe pna rire grnpu lbh guvf —<br>
fb vg fvzcyl qbrfa’g pbzcyr sbe lbh…<br><br>
Guvf vfa’g n chmmyr bs ybtvp.<br>
Vg’f n ynathntr bayl gur urneg ernqf.<br>
Naq jura lbh svanyyl haqrefgnaq…<br>
GUR XRL BS ZL URNEG VF LBH.

    </p>
    <button onclick="nextPage(6)">Continue</button>
  </div>
</div>

<!-- PAGE 6: Final Heart Message -->
<div id="page6" class="page">
  <div class="card">
    <h2>Final Message</h2>
    <p style="text-align:left">
You don’t just make me smile.<br>
You calm me.<br><br>
It’s a little scary to care this softly.<br>
But it’s beautiful.<br><br>
And if life ever offers me a place beside someone meaningful…<br>
I would quietly hope it’s you.<br><br>
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
    nextPage(3);
    setTimeout(()=>nextPage(4),2500);
  } else {
    document.getElementById("error").innerText =
      "This message was written for someone else.";
  }
}
</script>

</body>
</html>