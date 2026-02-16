<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>THE PATRIOTIC LOVE STORY</title>

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

/* Hint animation */
@keyframes hintGlow {
  0% { box-shadow:0 0 10px #ff00cc; }
  50% { box-shadow:0 0 25px #00f2fe; }
  100% { box-shadow:0 0 10px #ff00cc; }
}
.hintBox{
  opacity:0;
  transform:scale(0.95);
  transition:all 0.6s ease;
  padding:10px;
  border-radius:12px;
}
.hintBox.showHint{
  opacity:1;
  transform:scale(1);
  animation:hintGlow 2s infinite alternate;
}
.error{ color:#ff4d6d; margin-top:10px; }
</style>
</head>

<body>

<div class="blob"></div>
<div class="blob"></div>

<!-- PAGE 1 -->
<div id="page1" class="page show">
  <div class="card">
    <h1>HERE WE BEGIN OUR LOVE STORY</h1>
    <button onclick="nextPage(2)">YES I'M THE ONE YOU WAITINGFOR</button>
  </div>
</div>

<!-- PAGE 2 -->
<div id="page2" class="page">
  <div class="card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <p id="error" class="error"></p>
  </div>
</div>

<!-- PAGE 3 -->
<div id="page3" class="page">
  <div class="card">
    <h3>Identity Confirmed…</h3>
  </div>
</div>

<!-- PAGE 4 -->
<div id="page4" class="page">
  <div class="card">
    <h2>Hi Afrin…</h2>
    <button onclick="nextPage(5)">Continue</button>
  </div>
</div>

<!-- PAGE 5 -->
<div id="page5" class="page">
  <div class="card">
    <h3>Encrypted Transmission</h3>
    <pre>
Bu… bxnl, lbh znqr vg guvf sne.
GUR 'LRX' BS ZL URNEG VF LBH.
    </pre>
    <button onclick="nextPage(6)">Enter Passcode to Continue</button>
  </div>
</div>

<!-- PAGE 6 -->
<div id="page6" class="page">
  <div class="card">
    <h3>Enter Passcode</h3>
    <input type="password" id="securityCode">
    <br>
    <button onclick="checkCode()">Unlock</button>
    <p id="codeError" class="error"></p>
  </div>
</div>

<!-- PAGE 7 -->
<div id="page7" class="page">
  <div class="card">
    <h2>DECODE MY HEART IF YOU CAN</h2>

    <p style="text-align:left">
Afrin..
    </p>

    <button onclick="showHintPrompt()">Decode Hint</button>

    <div id="hintSection" style="display:none; margin-top:20px;">
      <input type="text" id="loveConfirm" placeholder="Type LOVE YOU TOO">
      <br>
      <button onclick="checkLove()">Reveal Hint</button>
      <p id="loveError" class="error"></p>
      <p id="realHint" class="hintBox" style="display:none;">
        Hint: Shift each letter forward by 4 😉
      </p>
    </div>
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
  } else {
    document.getElementById("error").innerText =
      "Identity mismatch 😏 Try again Agent.";
  }
}

function checkCode(){
  let code = document.getElementById("securityCode").value.toLowerCase();
  if(code === "nirfa"){
    nextPage(7);
  } else {
    document.getElementById("codeError").innerText =
      "That code unlocked nothing 😌";
  }
}

function showHintPrompt(){
  document.getElementById("hintSection").style.display = "block";
}

function checkLove(){
  let love = document.getElementById("loveConfirm").value.trim().toLowerCase();
  if(love === "love you too"){
    let hint = document.getElementById("realHint");
    hint.style.display = "block";
    setTimeout(()=>{ hint.classList.add("showHint"); },50);
    document.getElementById("loveError").innerText = "";
  } else {
    document.getElementById("loveError").innerText =
      "Hmm 🤔 That doesn’t sound very loving.";
  }
}
</script>

</body>
</html>