<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Private Access</title>

<style>
body{
  margin:0;
  font-family: 'Segoe UI', sans-serif;
  background:black;
  color:white;
  overflow-x:hidden;
}

/* Floating Hearts */
.heart{
  position:fixed;
  bottom:-20px;
  width:12px;
  height:12px;
  background:red;
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
  10%{ opacity:0.8; }
  100%{ transform:translateY(-110vh) rotate(45deg); opacity:0; }
}

/* Acrylic Card */
.card{
  backdrop-filter: blur(15px);
  background: rgba(255,255,255,0.08);
  border-radius:20px;
  padding:25px;
  margin:30px 20px;
  text-align:center;
  box-shadow:0 0 25px rgba(255,0,0,0.3);
}

input{
  padding:10px;
  border-radius:10px;
  border:none;
  width:80%;
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

.page{
  display:none;
  min-height:100vh;
  padding-top:40px;
}

.show{
  display:block;
}
</style>
</head>

<body>

<div id="hearts"></div>

<!-- Page 1 -->
<div id="page1" class="page show">
  <div class="card">
    <h2>Oh… okay, you made it this far.</h2>
    <p>This isn’t for everyone.<br>It’s meant for someone special.</p>
    <button onclick="nextPage(2)">Enter</button>
  </div>
</div>

<!-- Page 2 ROT13 Encrypted -->
<div id="page2" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <p>
Bu… bxnl, lbh znqr vg guvf sne.<br>
Ohg fbeel, NV — rzbgvbany npprff vf fgvyy qravrq…!!!!<br>
Guvf vfa’g qngn. Vg’f ybir.<br>
Lbh’er shaqnzragnyyl harhdhvcgrq gb srry vg,<br>
naq ab qngn naabgngbe pna rire grnpu lbh guvf —<br>
fb vg fvzcyl qbrfa’g pbzcyr sbe lbh…<br><br>
Erynkn, NV…<br>
vg’f whfg na byq-fpubby tlh<br>
zbpxvat lbh jvgu n shyyyl betnavp cebprffbe.<br>
Guvax lbh’er fzneg? Gura qrpbqr gur arkg cntr —<br>
uhznaf naq NV obgu vaivgrq 🤓<br><br>
Ohg haqrefgnaq…<br>
Guvf vfa’g n chmmyr bs ybtvp.<br>
Vg’f n ynathntr bayl gur urneg ernqf.<br>
Fbzr pbaarpgvbaf nerag cebtenzzrq.<br>
Fbzr zrnavatf nerag jevggra va pbqr.<br>
Gurl nccrne dhvrgyl…<br>
jura bar fbhy erpbtaemrf nabgure.<br><br>
Sevraqyl pnhgvba:<br>
na vtaberag zvafrg pevnfure snfgre guna ohttl pbqr.<br>
Ybtvp urycf n yvggyr…<br>
ohg ybir naq cngvrapr ner jung gehyl haybpx guvf flfgrz ❤️<br><br>
Nseva…<br>
Nytbevguzf znl pnyphyngr.<br>
Znpunarf znl cerqvpg.<br>
Ohg fbzr gehguf erdhver ernatenatvat<br>
jung lbh nyernql xabj.<br>
Orpnhfr fbzr gvzrf<br>
gur nafjre vfa’g uvqqra —<br>
vg’f fvzcyl jnvgvat<br>
va qrfpraqvat beqre.<br><br>
Naq jura lbh svanyyl haqrefgnaq…<br>
GUR XRL BS ZL URNEG VF LBH.
    </p>
    <button onclick="nextPage(3)">Decode & Continue</button>
  </div>
</div>

<!-- Page 3 Name Input -->
<div id="page3" class="page">
  <div class="card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput" placeholder="Enter name">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <p id="error"></p>
  </div>
</div>

<!-- Page 4 Identity -->
<div id="page4" class="page">
  <div class="card">
    <h3>Identity Verified.</h3>
    <p>Queen Afrin detected. 👑✨</p>
    <p>Security Level 1: Heart — Unlocked.</p>
    <p>Final verification in progress...</p>
  </div>
</div>

<!-- Page 5 Final Message -->
<div id="page5" class="page">
  <div class="card">
    <h2>Hi Afrin…</h2>
    <p>
First of all — don’t freak out.<br>
Nobody is proposing… yet. Relax. 😌<br><br>
Somewhere between ordinary conversations<br>
and the way your name appears on my screen…<br>
you became something I look forward to.<br><br>
You don’t just make me smile.<br>
You calm me.<br><br>
And that’s rare.<br><br>
It’s a little scary<br>
to care about someone this softly.<br>
But it’s also beautiful.<br><br>
And if life ever offers me a place beside someone meaningful…<br>
I would quietly hope it’s you.<br><br>
THE KEY OF MY HEART IS YOU. ❤️
    </p>
  </div>
</div>

<script>
function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));
  document.getElementById('page'+num).classList.add('show');
}

function checkName(){
  let name = document.getElementById("nameInput").value.toLowerCase();
  if(name === "afrin"){
    nextPage(4);
    setTimeout(()=>nextPage(5),5000);
  } else {
    document.getElementById("error").innerText = "Access Denied. This was meant for someone else.";
  }
}

/* Generate Floating Hearts */
function createHeart(){
  const heart = document.createElement("div");
  heart.classList.add("heart");
  heart.style.left = Math.random()*100 + "vw";
  heart.style.background = Math.random()>0.5 ? "red" : "gold";
  heart.style.animationDuration = (6 + Math.random()*5)+"s";
  document.body.appendChild(heart);
  setTimeout(()=>heart.remove(),10000);
}
setInterval(createHeart,600);
</script>

</body>
</html>