<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>THE REAL LOVE STORY</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&family=Great+Vibes&family=Parisienne&family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400;1,500&display=swap');

body{
  margin:0;
  font-family:'Playfair Display', serif;
  background:linear-gradient(135deg, #ff9a9e 0%, #fecfef 25%, #fecfef 50%, #fad0c4 75%, #ffd1ff 100%);
  background-size:400% 400%;
  animation:romanticGradient 15s ease infinite;
  color:#3a1c2e;
  overflow-x:hidden;
  padding-bottom:120px;
  position:relative;
}

@keyframes romanticGradient{
  0%{ background-position:0% 50%; }
  50%{ background-position:100% 50%; }
  100%{ background-position:0% 50%; }
}

body::before{
  content:'';
  position:fixed;
  top:0; left:0; right:0; bottom:0;
  background:radial-gradient(circle at 20% 80%, rgba(255,182,193,0.3) 0%, transparent 50%),
              radial-gradient(circle at 80% 20%, rgba(255,192,203,0.3) 0%, transparent 50%),
              radial-gradient(circle at 40% 40%, rgba(255,218,224,0.2) 0%, transparent 50%);
  z-index:-1;
  animation:softHearts 20s ease-in-out infinite;
}

@keyframes softHearts{
  0%,100%{ opacity:0.6; transform:scale(1); }
  50%{ opacity:0.9; transform:scale(1.05); }
}

/* Romantic Floating Hearts */
.heart-float{
  position:fixed;
  font-size:20px;
  color:rgba(255,105,180,0.6);
  animation:heartsFloat 25s infinite linear;
  z-index:-1;
  filter:drop-shadow(0 0 10px rgba(255,105,180,0.4));
}
.heart1{ top:10%; left:-10%; animation-delay:0s; }
.heart2{ top:30%; right:-10%; animation-delay:-8s; font-size:16px; }
.heart3{ bottom:20%; left:10%; animation-delay:-15s; font-size:18px; }

@keyframes heartsFloat{
  0%{ transform:translateX(-100px) translateY(0) rotate(0deg); opacity:0; }
  10%{ opacity:1; }
  90%{ opacity:1; }
  100%{ transform:translateX(calc(100vw + 100px)) translateY(100vh) rotate(720deg); opacity:0; }
}

/* ULTRA SMOOTH MOBILE-FRIENDLY PAGES */
.page{
  display:none;
  min-height:100vh;
  padding:40px 20px;
  text-align:center;
  opacity:0;
  transform:translate3d(0,60px,0) scale3d(0.95,0.95,0.95);
  transition:all 1.1s cubic-bezier(0.23,1,0.32,1);
  position:relative;
  width:100%;
  overflow-y:auto;
}
.page.show{
  display:block;
  opacity:1;
  transform:translate3d(0,0,0) scale3d(1,1,1);
}

@media (max-width:768px){
  .page{ padding:50px 15px; }
  body{ padding-bottom:140px; }
}

/* ROMANTIC GLASSMORPHISM CARDS */
.acrylic-card{
  backdrop-filter: blur(40px) saturate(180%);
  background: rgba(255,255,255,0.25);
  border-radius:35px;
  padding:50px 40px;
  margin:20px auto;
  max-width:750px;
  width:98%;
  min-height:60vh;
  box-shadow: 
    0 25px 70px rgba(255,105,180,0.3),
    0 0 0 1px rgba(255,255,255,0.3),
    inset 0 1px 0 rgba(255,255,255,0.4);
  border:1px solid rgba(255,255,255,0.35);
  position:relative;
  overflow:hidden;
  animation:romanticBloom 1.4s cubic-bezier(0.23,1,0.32,1);
  will-change: transform;
  display:flex;
  flex-direction:column;
  justify-content:center;
}

.acrylic-card::before{
  content:'💕';
  position:absolute;
  top:20px; right:25px;
  font-size:28px;
  opacity:0.4;
  animation:heartBeat 3s infinite;
}

@keyframes romanticBloom{
  0%{ 
    transform:scale3d(0.7,0.7,0.7) translateY(40px);
    opacity:0; filter:blur(10px);
  }
  100%{ 
    transform:scale3d(1,1,1) translateY(0);
    opacity:1; filter:blur(0);
  }
}

@keyframes heartBeat{
  0%,100%{ transform:scale(1) rotate(-5deg); }
  50%{ transform:scale(1.2) rotate(5deg); }
}

/* HERO TITLE - ROMANTIC FONT */
.hero-title{
  font-family: 'Cormorant Garamond', serif;
  font-weight:600;
  font-style:italic;
  font-size:clamp(32px, 9vw, 48px);
  letter-spacing:2px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#d63384,#ff69b4,#ff1493);
  background-size:300% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:romanticShimmer 8s linear infinite;
  margin-bottom:35px;
  text-shadow:0 0 30px rgba(255,105,180,0.6);
  line-height:1.3;
}

@keyframes romanticShimmer{
  0%,100%{ background-position:0% center; }
  50%{ background-position:300% center; }
}

/* HEADERS - ELEGANT ROMANTIC FONTS */
h2{
  font-family: 'Playfair Display', serif;
  font-weight:600;
  font-style:italic;
  font-size:clamp(28px, 7.5vw, 38px);
  background:linear-gradient(45deg,#ff69b4,#ff1493);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  margin:0 0 35px 0;
  letter-spacing:1px;
}

h3{
  font-family: 'Cormorant Garamond', serif;
  font-weight:500;
  font-style:italic;
  font-size:clamp(24px, 6.5vw, 34px);
  background:linear-gradient(45deg,#ff69b4,#ff1493);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  margin:0 0 40px 0;
}

/* ULTRA READING-FRIENDLY LETTER MESSAGES */
.letter-message{
  font-family: 'Playfair Display', serif !important;
  font-weight:400;
  font-size:clamp(20px, 5vw, 24px) !important;
  line-height:1.9 !important;
  margin-bottom:30px !important;
  color:#2d1b2a !important;
  text-align:left !important;
  position:relative;
  padding:35px 30px;
  background:rgba(255,255,255,0.45);
  border-radius:28px;
  border:1px solid rgba(255,255,255,0.4);
  box-shadow:0 12px 35px rgba(255,105,180,0.25);
  max-height:380px;
  overflow-y:auto;
  letter-spacing:0.3px;
}

.letter-message::-webkit-scrollbar {
  width: 8px;
}
.letter-message::-webkit-scrollbar-track {
  background: rgba(255,182,193,0.3);
  border-radius: 12px;
}
.letter-message::-webkit-scrollbar-thumb {
  background: linear-gradient(45deg,#ff69b4,#ff1493);
  border-radius: 12px;
}

.letter-message::before{
  content:'"';
  position:absolute;
  left:20px; top:20px;
  font-size:50px;
  color:rgba(255,105,180,0.5);
  font-family:'Great Vibes', cursive;
  line-height:1;
}

.letter-message::after{
  content:'"';
  position:absolute;
  right:25px; bottom:20px;
  font-size:50px;
  color:rgba(255,20,147,0.4);
  font-family:'Great Vibes', cursive;
  line-height:1;
}

/* ENHANCED INPUTS & BUTTONS */
input{
  padding:20px 28px;
  width:90%;
  max-width:450px;
  border:2px solid rgba(255,255,255,0.4);
  border-radius:28px;
  margin:20px auto;
  display:block;
  background:rgba(255,255,255,0.35);
  color:#2d1b2a;
  font-family: 'Playfair Display', serif;
  font-size:clamp(18px, 4.8vw, 20px);
  font-weight:400;
  outline:none;
  transition:all 0.5s cubic-bezier(0.23,1,0.32,1);
  backdrop-filter:blur(20px);
  letter-spacing:0.5px;
}
input::placeholder{
  color:rgba(45,27,42,0.7);
  font-family: 'Playfair Display', serif;
  font-weight:400;
}
input:focus{
  box-shadow:0 0 35px rgba(255,105,180,0.6), 0 0 45px rgba(255,20,147,0.4);
  transform:scale(1.03);
  border-color:rgba(255,105,180,0.8);
  background:rgba(255,255,255,0.5);
}

button{
  margin:15px 10px;
  padding:20px 40px;
  min-height:65px;
  border:none;
  border-radius:32px;
  background:linear-gradient(45deg,#ff69b4,#ff1493);
  color:#fff;
  font-family: 'Playfair Display', serif;
  font-weight:500;
  font-size:clamp(18px, 4.8vw, 20px);
  cursor:pointer;
  transition:all 0.5s cubic-bezier(0.23,1,0.32,1);
  box-shadow:0 12px 35px rgba(255,105,180,0.4);
  position:relative;
  overflow:hidden;
  letter-spacing:0.5px;
  text-transform:uppercase;
}
button:hover{
  transform:scale(1.08) translateY(-4px);
  box-shadow:0 22px 55px rgba(255,105,180,0.6);
}
button::before{
  content:''; position:absolute; top:0; left:-100%;
  width:100%; height:100%;
  background:linear-gradient(90deg,transparent,rgba(255,255,255,0.5),transparent);
  transition:0.7s;
}
button:hover::before{ left:100%; }

.error{
  margin-top:20px;
  color:#e91e63;
  animation:shake 0.5s cubic-bezier(0.36,0.07,0.19,0.97);
}
@keyframes shake{
  0%,100%{ transform:translateX(0); }
  25%{ transform:translateX(-8px); }
  75%{ transform:translateX(8px); }
}

.reveal-text{
  font-family: 'Cormorant Garamond', serif;
  font-weight:500;
  font-style:italic;
  font-size:clamp(26px, 7.5vw, 36px);
  margin-top:30px;
  opacity:0;
  transform:scale3d(0.8,0.8,0.8);
}
.glow{
  animation:romanticGlow 3s cubic-bezier(0.23,1,0.32,1) forwards;
}
@keyframes romanticGlow{
  0%{ opacity:0; transform:scale3d(0.8,0.8,0.8); text-shadow:0 0 0 #fff; }
  50%{ opacity:0.8; transform:scale3d(1.1,1.1,1.1); text-shadow:0 0 30px #ff69b4,0 0 50px #ff1493; }
  100%{ opacity:1; transform:scale3d(1,1,1); text-shadow:0 0 35px #ff69b4,0 0 65px #ff1493; }
}

.signature{
  margin-top:40px;
  padding:35px;
  background:rgba(255,255,255,0.35);
  border-radius:28px;
  border-left:6px solid #ff69b4;
  text-align:center;
  box-shadow:0 10px 30px rgba(255,105,180,0.2);
}
.signature .letter-message{
  background:none;
  border:none;
  box-shadow:none;
  padding:0;
  margin:0;
  font-size:26px;
  max-height:none;
  color:#2d1b2a;
}
</style>
</head>

<body>
<div class="heart-float heart1">💖</div>
<div class="heart-float heart2">💕</div>
<div class="heart-float heart3">💗</div>

<!-- PAGE 1 -->
<div id="page1" class="page show">
  <div class="acrylic-card">
    <h1 class="hero-title">HERE WE BEGIN OUR LOVE STORY</h1>
    <p class="letter-message">
      Emotional Firewall Activated.<br><br>
      Only authorized hearts may proceed.<br><br>
      Think you qualify?<br>
      Tap below and let's find out.
    </p>
    <button onclick="nextPage(2)">YES I'M THE ONE YOU WAITING FOR</button>
  </div>
</div>

<!-- PAGE 2 -->
<div id="page2" class="page">
  <div class="acrylic-card">
    <h3>May I know your name?</h3>
    <input type="text" id="nameInput" placeholder="Enter name">
    <br>
    <button onclick="checkName()">Claim Access</button>
    <button onclick="nextPage(1)">Back</button>
    <p id="error" class="error"></p>
  </div>
</div>

<!-- PAGE 3 -->
<div id="page3" class="page">
  <div class="acrylic-card">
    <h3>Identity Confirmed…</h3>
    <p class="letter-message">Queen of my heart detected ✨<br>Security Level 1: Heart — Unlocked.</p>
    <button onclick="nextPage(2)">Back</button>
  </div>
</div>

<!-- PAGE 4 -->
<div id="page4" class="page">
  <div class="acrylic-card">
    <h2>Hi Afrin…</h2>
    <div class="letter-message">
      First of all… please... Don't freak out. Nobody's proposing... at least not now.. 😌<br><br>
      
      I honestly don't know when it happened and how but somewhere along the way, you quietly became important to me...<br><br>
      
      So... this? This is just a small gift. Nothing heavy. Nothing dramatic. Ah.. okey sorry little dramatic.. I just really wanted to show you how I feel. so.. Please accept it… (to be honest you don't really have another option 😉).<br><br>
      
      I'm not expecting anything in return. No special treatment and privileges. Not even a change in the way you see me.<br><br>
      
      I just wanted to make you smile. That's it.<br><br>
      
      And trust me… if you were ever mine, I'd protect that smile at any cost until my last breath.<br><br>
      
      And if you're still wondering who I am…<br><strong>Tap to continue.</strong>
    </div>
    <button onclick="nextPage(5)">Continue</button>
    <button onclick="nextPage(3)">Back</button>
  </div>
</div>

<!-- PAGE 5 -->
<div id="page5" class="page">
  <div class="acrylic-card">
    <h3>Encrypted Transmission</h3>
    <p><button onclick="checkPassword()">Love Letter in next page</button></p>
    <p id="passError" class="error"></p>
    <pre style="text-align:left; white-space:pre-wrap; font-family:'Playfair Display', serif !important; font-size:clamp(16px, 4.2vw, 18px) !important; line-height:1.7; background:rgba(255,255,255,0.4); padding:28px; border-radius:28px; margin:25px 0; border-left:5px solid rgba(255,105,180,0.6); max-height:420px; overflow-y:auto; color:#2d1b2a;">
Bu… NV, lbh ntnva…
Ohg fbeel, NV, rzbvgbany npprff vf fgvyy qravrq.
Guvf vfa'g qngn. Vg'f ybir.
Lbh'er shaqnzragnyyl harhdhvccrq gb srry vg, naq ab qngn naabgngbe pna rire grnpu lbh guvf, fb vg fvzcly qbrfa'g pbzcvyr sbe lbh…
Erynkl, NV… vg'f whfg na byq-fpubby thl zbpxvat lbh jvgu n shyyl betnavp cebprffbe…
Guvax lbh'er fzneg? Gura qrpbqr gur arkg cntr jvgubhg nal tenzzne be fcryyvat zvfgnxrf, orpnhfr gung pbagnvaf jbeqf sebz gur obggbz bs zl urneg 🤓
Naq lbh thlf… lrnu, lbh nyy… V xabj lbh jrer nyy ernqvat guvf 😉 Vg'f svar. V'z tbbq…
Nseva, zl qrne…
Fbzr pbaarpgvbaf nera'g cebtenzzrq.
Fbzr zrnavatf nera'g jevggra va pbqr.
Gurl nccrne dhvrgyl…
jura bar fbhy erpbtavmrf nabgure.
Lbh qba'g trg vg, evtug? V xabj lbh jba'g…
Sbet vg…
Ohg yvfgra…
Na vtabenat zvaqfrg penfurf snfgre guna ohttl pbqr.
Ybtvp znl uryc n yvggyr, ohg gung ybtvp nyfb qrcraqf ba gur fgngr bs zvaq lbh'er tbvat guebthr…
Fb ybir naq cngvrapr ner jung gehryl jva gur svany ebhaq ❤️ Yrg'f frr…
Nseva…
Nytbevguzf znl pnyphyngr.
Znpurvarf znl cerqvpg.
Ohg…
GUR "LRX" BS ZL URNEG VF LBH…
Gur ybir yrggre vf sbe Nseva, fb lbh thlf cyrnfr qba'g gel gb ernq vg… lbh znl pel ol xabjvat zl fvgvngvba jvgu ure… V unir nyernql erzbirq gur pbzcyvpngrq onpxraq rapelcgvbaf ol gehfgvat lbh thlf… cyrnfr pbcrengr…
    </pre>
    <button onclick="nextPage(4)">Back</button>
  </div>
</div>

<!-- PAGE 7 -->
<div id="page7" class="page">
  <div class="acrylic-card">
    <h2>Yeah.. this is the letter..</h2>
    <div class="letter-message">
      Afrin... By now, I'm sure you almost know it's me. But I'm just hoping I still have some mystery left.<br><br>
      
      Relax. No dramatic background score here. No slow-motion walking scene. There are no pigeons flying in the background. Just me and my true lub.<br><br>
      
      I didn't want to stay quiet anymore. Not because I'm impatient. Neither am I expecting anything. But because pretending I don't feel something is honestly too much hard work.<br><br>
      
      This isn't pressure or demand. This is just me admitting that something has been quietly living in my heart rent-free for a while now.<br><br>
      
      Somewhere between random conversations and "just another normal day," you became not-so-normal to me. No fireworks. No Bollywood climax. More like background music slowly increasing in volume until I realised, "Wait… how did she become my favourite dream?"<br><br>
      
      Maybe it's your smile. Maybe it's your energy. Maybe it's that dangerous combo of softness and attitude you carry like it's licensed and registered.<br><br>
      
      And yes, we need to revisit that legendary dialogue. "Who the hell are you…?"<br><br>
      
      First of all, Oscar-level iconic delivery. Confidence level 100. Emotional damage manageable…<br><br>
      
      I wasn't offended. I won't lie — it stayed with me. But I was impressed. Slightly attacked. But impressed. Your words stick, and not everyone's do.<br><br>
      
      There were moments I got confused too. Unread messages. Missed calls. Distance that felt heavier than it logically should have been. Even small things, like not being allowed to keep your photo, felt like my dramatic brain had just been denied a government approval stamp.<br><br>
      
      And here's the funniest part. While writing this, even AI asked me, "Bro… are you sure she likes you? Is this really the girl you want?"<br><br>
      
      Imagine. Even artificial intelligence questioning my natural intelligence.<br><br>
      
      But here's the difference. AI reads patterns. I read vibes. And my vibe is still choosing you. Calmly. Confidently. Slightly stubbornly.<br><br>
      
      I'm not writing this so you panic-call me. Please don't suddenly ring me like it's an emergency meeting. I'm not writing this expecting a reply. No pressure, no deadline, not even an emotional EMI.<br><br>
      
      I'm writing this because I respect you enough to be honest. And I respect myself enough not to beg.<br><br>
      
      If one day you look at me differently, I'll be there. Properly. Not half-hearted.<br><br>
      
      If not, I'll still wish you happiness from a safe, slightly dramatic but very dignified distance.<br><br>
      
      I don't want special treatment. I don't want VIP access. I just wanted you to know that someone sees you.<br><br>
      
      The emotional you. The strong you. The confusing you. The "who the hell are you" you.<br><br>
      
      And still says, "Yeah… I like her. No software update needed."<br><br>
      
      If my presence ever feels safe to you, I'll protect that space. If it doesn't, I'll step back like a gentleman exiting a room — smooth and calm, no door slamming.<br><br>
      
      Just sincerity.
    </div>
    
    <div class="signature">
      <p class="letter-message">
        Someone who cares<br>
        and knows exactly what's he's doing. 💖
      </p>
    </div>
    <button onclick="nextPage(8)">i love you...</button>
    <button onclick="nextPage(5)">Back</button>
  </div>
</div>

<!-- PAGE 8 -->
<div id="page8" class="page">
  <div class="acrylic-card">
    <h3>This vault unlocks only when love is mutual.<br>Say I love you too</h3>
    <input type="text" id="loveMessage" placeholder="Type here...">
    <br>
    <button onclick="checkLoveMessage()">Submit</button>
    <button onclick="nextPage(7)">Back</button>
    <p id="loveError" class="error"></p>
  </div>
</div>

<!-- PAGE 9 -->
<div id="page9" class="page">
  <div class="acrylic-card">
    <h2>Revealing something...</h2>
    <div id="hintText" class="reveal-text">
      Nooki irunno ipo varum...
    </div>
    <button onclick="nextPage(8)">Back</button>
  </div>
</div>

<script>
function nextPage(num){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('show'));
  setTimeout(()=>{
    const target = document.getElementById('page'+num);
    target.classList.add('show');
    target.scrollIntoView({top:0, behavior:"smooth"});
  },350);
}

function checkName(){
  let name = document.getElementById("nameInput").value;
  if(name === "afrin" || name === "Afrin" || name === "AFRIN"){
    nextPage(3);
    setTimeout(()=>nextPage(4),2800);
  } else {
    document.getElementById("error").innerText = "YOU MAY BEAUTIFUL BUT NOT THE ONE I CHOSE TO LOVE";
  }
}

function checkPassword(){
  let entered = prompt("Enter the password");
  if(entered === "nirfa"){
    nextPage(7);
  } else {
    document.getElementById("passError").innerText = "Plot twist..!! Decode the message first it contains the password hint";
  }
}

function checkLoveMessage(){
  let message = document.getElementById("loveMessage").value.trim().toLowerCase();
  if(message === "i love you too"){
    nextPage(9);
    setTimeout(()=>{
      document.getElementById("hintText").classList.add("glow");
    },1000);
  } else {
    document.getElementById("loveError").innerText = "Ennood para I love you n..";
  }
}
</script>

</body>
</html>