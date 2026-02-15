<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Here We Begin Our Love Story</title>

<style>
body{
  margin:0;
  font-family:'Segoe UI', sans-serif;
  background:linear-gradient(135deg,#141E30,#243B55);
  color:white;
  overflow-x:hidden;
}

/* Floating Acrylic Motion */
.blob{
  position:fixed;
  width:350px;
  height:350px;
  border-radius:50%;
  filter:blur(100px);
  animation:floatBlob 20s infinite alternate ease-in-out;
  z-index:-1;
}
.blob:nth-child(1){ top:-120px; left:-120px; background:rgba(0,200,255,0.25); }
.blob:nth-child(2){ bottom:-150px; right:-120px; background:rgba(255,0,150,0.25); }

@keyframes floatBlob{
  0%{ transform:translate(0,0) scale(1); }
  50%{ transform:translate(70px,80px) scale(1.2); }
  100%{ transform:translate(-50px,60px) scale(1); }
}

.page{
  display:none;
  min-height:100vh;
  padding:40px 20px;
  text-align:center;
  opacity:0;
  transform:translateY(40px);
  transition:opacity 0.6s ease, transform 0.6s ease;
}

.page.show{
  display:block;
  opacity:1;
  transform:translateY(0);
}

.card{
  backdrop-filter: blur(25px);
  background: rgba(255,255,255,0.08);
  border-radius:25px;
  padding:35px;
  margin:auto;
  max-width:520px;
  box-shadow:0 10px 40px rgba(0,0,0,0.6);
}

.hero-title{
  font-size:24px;
  letter-spacing:2px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#00d2ff,#ff00cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

h2,h3{
  background:linear-gradient(45deg,#00d2ff,#ff00cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}

input{
  padding:14px;
  width:85%;
  border:none;
  border-radius:12px;
  margin-top:15px;
  background:rgba(255,255,255,0.1);
  color:white;
  outline:none;
  font-size:15px;
}

input:focus{
  box-shadow:0 0 15px rgba(255,0,150,0.5);
}

button{
  margin-top:18px;
  padding:12px 28px;
  border:none;
  border-radius:25px;
  background:linear-gradient(45deg,#00d2ff,#ff00cc);
  color:white;
  font-weight:bold;
  cursor:pointer;
  transition:0.3s ease;
}

button:hover{
  box-shadow:0 0 20px rgba(255,0,150,0.6);
}

.error{
  margin-top:12px;
  color:#ff6b81;
  font-size:14px;
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
    <button onclick="nextPage(2)">Tap to Claim</button>
  </div>
</div>

<!-- (All other pages remain EXACTLY as your original HTML content) -->

<script>
function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>{
    p.classList.remove('show');
  });

  setTimeout(()=>{
    document.getElementById('page'+num).classList.add('show');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  },200);
}

function checkName(){
  let name = document.getElementById("nameInput").value.trim().toLowerCase();
  if(name === "afrin"){
    nextPage(3);
    setTimeout(()=>nextPage(4),2000);
  } else {
    document.getElementById("error").innerText =
      "Identity mismatch. Either typo… or espionage.";
  }
}

function checkCode(){
  let code = document.getElementById("securityCode").value.trim().toLowerCase();
  if(code === "nirfa"){
    nextPage(7);
    loadTracking();
  } else {
    document.getElementById("codeError").innerText =
      "That code unlocked nothing. Try reversing your thinking.";
  }
}

function checkLove(){
  let phrase = document.getElementById("loveConfirm").value.trim().toLowerCase();
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