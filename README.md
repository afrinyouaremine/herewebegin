<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>THE REAL LOVE STORY</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&family=Great+Vibes&family=Parisienne&display=swap');

body{
  margin:0;
  font-family:'Segoe UI', sans-serif;
  background:linear-gradient(135deg,#0f0c29,#302b63,#24243e);
  color:white;
  overflow-x:hidden;
  padding-bottom:100px;
}

/* Enhanced Floating Acrylic Blobs */
.blob{
  position:fixed;
  border-radius:50%;
  filter:blur(80px);
  animation:floatBlob 20s infinite alternate ease-in-out;
  z-index:-1;
  opacity:0.8;
}
.blob1{
  width:450px; height:450px;
  background:linear-gradient(45deg, rgba(0,255,255,0.2), rgba(0,150,255,0.1));
  top:-120px; left:-120px; 
  animation-duration:24s;
}
.blob2{
  width:380px; height:380px;
  background:linear-gradient(45deg, rgba(255,0,150,0.25), rgba(255,100,200,0.15));
  bottom:-180px; right:-120px; 
  animation-duration:28s; animation-delay:-8s;
}
.blob3{
  width:320px; height:320px;
  background:linear-gradient(45deg, rgba(0,255,255,0.15), rgba(255,0,150,0.1));
  top:20%; right:5%; 
  animation-duration:26s; animation-delay:-12s;
}

@keyframes floatBlob{
  0%{ transform:translate(0,0) scale(1) rotate(0deg); }
  50%{ transform:translate(80px,100px) scale(1.25) rotate(180deg); }
  100%{ transform:translate(-50px,80px) scale(1.1) rotate(360deg); }
}

/* ULTRA SMOOTH MOBILE-FRIENDLY PAGES */
.page{
  display:none;
  min-height:100vh;
  padding:50px 25px;
  text-align:center;
  opacity:0;
  transform:translate3d(0,60px,0) scale3d(0.95,0.95,0.95);
  transition:all 1.1s cubic-bezier(0.23,1,0.32,1);
  position:relative;
  width:100%;
}
.page.show{
  display:block;
  opacity:1;
  transform:translate3d(0,0,0) scale3d(1,1,1);
}

/* MOBILE WIDE & SMOOTH */
@media (max-width:768px){
  .page{ padding:60px 20px; }
  body{ padding-bottom:120px; }
}

/* ACRYLIC GLASS CARDS WITH ANIMATION */
.acrylic-card{
  backdrop-filter: blur(35px) saturate(160%);
  background: rgba(255,255,255,0.12);
  border-radius:35px;
  padding:45px 35px;
  margin:20px auto;
  max-width:600px;
  width:95%;
  box-shadow: 
    0 25px 70px rgba(0,0,0,0.6),
    0 0 0 1px rgba(255,255,255,0.1),
    inset 0 1px 0 rgba(255,255,255,0.2);
  border:1px solid rgba(255,255,255,0.15);
  position:relative;
  overflow:hidden;
  animation:acrylicBloom 1.4s cubic-bezier(0.23,1,0.32,1);
  will-change: transform;
}

.acrylic-card::before{
  content:'✨';
  position:absolute;
  top:20px; right:25px;
  font-size:28px;
  opacity:0.3;
  animation:sparkle 4s infinite;
}

@keyframes acrylicBloom{
  0%{ 
    transform:scale3d(0.7,0.7,0.7) translateY(40px);
    opacity:0; filter:blur(10px);
  }
  100%{ 
    transform:scale3d(1,1,1) translateY(0);
    opacity:1; filter:blur(0);
  }
}

@keyframes sparkle{
  0%,100%{ opacity:0; transform:scale(0.5) rotate(0deg); }
  50%{ opacity:1; transform:scale(1.5) rotate(180deg); }
}

/* HERO TITLE */
.hero-title{
  font-family: 'Dancing Script', cursive;
  font-weight:700;
  font-size:clamp(28px, 8vw, 40px);
  letter-spacing:4px;
  text-transform:uppercase;
  background:linear-gradient(90deg,#00f2fe,#ff00cc,#00f2fe);
  background-size:300% auto;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  animation:shimmer 6s linear infinite;
  margin-bottom:35px;
  text-shadow:0 0 30px rgba(0,242,254,0.6);
  line-height:1.3;
}

@keyframes shimmer{
  0%,100%{ background-position:0% center; }
  50%{ background-position:300% center; }
}

/* HEADERS */
h2{
  font-family: 'Parisienne', cursive;
  font-size:clamp(26px, 7vw, 36px);
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  margin-bottom:25px;
}

h3{
  font-family: 'Great Vibes', cursive;
  font-size:clamp(24px, 6vw, 32px);
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  margin-bottom:30px;
}

/* BEAUTIFUL HANDWRITTEN MESSAGES */
.handwritten{
  font-family: 'Dancing Script', cursive !important;
  font-weight:500;
  font-size:clamp(16px, 4.5vw, 20px) !important;
  line-height:1.9 !important;
  margin-bottom:25px !important;
  color:rgba(255,255,255,0.95) !important;
  text-align:left !important;
  position:relative;
  padding:20px;
  background:rgba(255,255,255,0.05);
  border-radius:20px;
  border-left:4px solid rgba(0,242,254,0.5);
}

.handwritten::before{
  content:'"';
  position:absolute;
  left:-15px; top:10px;
  font-size:40px;
  color:rgba(0,242,254,0.3);
  font-family:'Great Vibes', cursive;
}

/* INPUT & BUTTONS */
input{
  padding:18px 25px;
  width:90%;
  max-width:450px;
  border:2px solid rgba(255,255,255,0.2);
  border-radius:25px;
  margin:20px auto;
  display:block;
  background:rgba(255,255,255,0.1);
  color:white;
  font-family: 'Dancing Script', cursive;
  font-size:clamp(16px, 4.5vw, 19px);
  outline:none;
  transition:all 0.5s cubic-bezier(0.23,1,0.32,1);
  backdrop-filter:blur(15px);
}
input::placeholder{
  color:rgba(255,255,255,0.6);
  font-family: 'Dancing Script', cursive;
}
input:focus{
  box-shadow:0 0 30px rgba(0,242,254,0.6), 0 0 40px rgba(255,0,204,0.4);
  transform:scale(1.05);
  border-color:rgba(0,242,254,0.8);
  background:rgba(255,255,255,0.2);
}

button{
  margin:15px 10px;
  padding:18px 35px;
  min-height:60px;
  border:none;
  border-radius:30px;
  background:linear-gradient(45deg,#00f2fe,#ff00cc);
  color:white;
  font-family: 'Dancing Script', cursive;
  font-weight:600;
  font-size:clamp(16px, 4.5vw, 19px);
  cursor:pointer;
  transition:all 0.5s cubic-bezier(0.23,1,0.32,1);
  box-shadow:0 10px 30px rgba(0,242,254,0.4);
  position:relative;
  overflow:hidden;
}
button:hover{
  transform:scale(1.1) translateY(-5px);
  box-shadow:0 20px 50px rgba(0,242,254,0.6);
}
button::before{
  content:''; position:absolute; top:0; left:-100%;
  width:100%; height:100%;
  background:linear-gradient(90deg,transparent,rgba(255,255,255,0.4),transparent);
  transition:0.7s;
}
button:hover::before{ left:100%; }

.error{
  margin-top:20px;
  color:#ff4d6d;
  animation:shake 0.5s cubic-bezier(0.36,0.07,0.19,0.97);
}
@keyframes shake{
  0%,100%{ transform:translateX(0); }
  25%{ transform:translateX(-8px); }
  75%{ transform:translateX(8px); }
}

.reveal-text{
  font-family: 'Great Vibes', cursive;
  font-size:clamp(24px, 7vw, 34px);
  margin-top:30px;
  opacity:0;
  transform:scale3d(0.8,0.8,0.8);
}
.glow{
  animation:glowReveal 2.5s cubic-bezier(0.23,1,0.32,1) forwards;
}
@keyframes glowReveal{
  0%{ opacity:0; transform:scale3d(0.8,0.8,0.8); text-shadow:0 0 0 #fff; }
  50%{ opacity:0.7; transform:scale3d(1.1,1.1,1.1); text-shadow:0 0 25px #ff00cc,0 0 45px #00f2fe; }
  100%{ opacity:1; transform:scale3d(1,1,1); text-shadow:0 0 30px #ff00cc,0 0 60px #00f2fe; }
}

.signature{
  margin-top:40px;
  padding:30px;
  background:rgba(255,255,255,0.08);
  border-radius:25px;
  border-left:5px solid #00f2fe;
  text-align:center;
}
.signature .handwritten{
  background:none;
  border-left:none;
  padding:0;
  font-size:22px;
}
</style>
</head>

<body>
<div class="blob blob1"></div>
<div class="blob blob2"></div>
<div class="blob blob3"></div>

<!-- PAGE 1 -->
<div id="page1" class="page show">
  <div class="acrylic-card">
    <h1 class="hero-title">HERE WE BEGIN OUR LOVE STORY</h1>
    <p class="handwritten">
      Emotional Firewall Activated.
      <br><br>
      Only authorized hearts may proceed.
      <br><br>
      Think you qualify?
      <br>
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
    <p class="handwritten">Queen of my heart detected ✨</p>
    <p class="handwritten">Security Level 1: Heart — Unlocked.</p>
    <button onclick="nextPage(2)">Back</button>
  </div>
</div>

<!-- PAGE 4 -->
<div id="page4" class="page">
  <div class="acrylic-card">
    <h2>Hi Afrin…</h2>
    <p class="handwritten">
      First of all… please... Don't freak out. Nobody's proposing... at least not now.. 😌
    </p>
    <p class="handwritten">
      I honestly don't know when it happened and how but somewhere along the way, you quietly became important to me...
    </p>
    <p class="handwritten">
      So... this? This is just a small gift. Nothing heavy. Nothing dramatic. Ah.. okey sorry little dramatic.. I just really wanted to show you how I feel. so.. Please accept it… (to be honest you don't really have another option 😉).
    </p>
    <p class="handwritten">
      I'm not expecting anything in return. No special treatment and privileges. Not even a change in the way you see me.
    </p>
    <p class="handwritten">
      I just wanted to make you smile. That's it.
    </p>
    <p class="handwritten">
      And trust me… if you were ever mine, I'd protect that smile at any cost until my last breath.
    </p>
    <p class="handwritten">
      And if you're still wondering who I am…
    </p>
    <p class="handwritten"><strong>Tap to continue.</strong></p>
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
    <pre style="text-align:left; white-space:pre-wrap; font-family:'Dancing Script', cursive !important; font-size:clamp(14px, 3.8vw, 16px) !important; line-height:1.6; background:rgba(255,255,255,0.08); padding:25px; border-radius:25px; margin:25px 0; border-left:4px solid rgba(0,242,254,0.5);">
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
    <p class="handwritten">
      Afrin... By now, I'm sure you almost know it's me. But I'm just hoping I still have some mystery left.
    </p>
    <p class="handwritten">
      Relax. No dramatic background score here. No slow-motion walking scene. There are no pigeons flying in the background. Just me and my true lub.
    </p>
    <p class="handwritten">
      I didn't want to stay quiet anymore. Not because I'm impatient. Neither am I expecting anything. But because pretending I don't feel something is honestly too much hard work.
    </p>
    <p class="handwritten">
      This isn't pressure or demand. This is just me admitting that something has been quietly living in my heart rent-free for a while now.
    </p>
    <p class="handwritten">
      Somewhere between random conversations and "just another normal day," you became not-so-normal to me. No fireworks. No Bollywood climax. More like background music slowly increasing in volume until I realised, "Wait… how did she become my favourite dream?"
    </p>
    <p class="handwritten">
      Maybe it's your smile. Maybe it's your energy. Maybe it's that dangerous combo of softness and attitude you carry like it's licensed and registered.
    </p>
    <p class="handwritten">
      And yes, we need to revisit that legendary dialogue. "Who the hell are you…?"
    </p>
    <p class="handwritten">
      First of all, Oscar-level iconic delivery. Confidence level 100. Emotional damage manageable…
    </p>
    <p class="handwritten">
      I wasn't offended. I won't lie — it stayed with me. But I was impressed. Slightly attacked. But impressed. Your words stick, and not everyone's do.
    </p>
    <p class="handwritten">
      There were moments I got confused too. Unread messages. Missed calls. Distance that felt heavier than it logically should have been. Even small things, like not being allowed to keep your photo, felt like my dramatic brain had just been denied a government approval stamp.
    </p>
    <p class="handwritten">
      And here's the funniest part. While writing this, even AI asked me, "Bro… are you sure she likes you? Is this really the girl you want?"
    </p>
    <p class="handwritten">
      Imagine. Even artificial intelligence questioning my natural intelligence.
    </p>
    <p class="handwritten">
      But here's the difference. AI reads patterns. I read vibes. And my vibe is still choosing you. Calmly. Confidently. Slightly stubbornly.
    </p>
    <p class="handwritten">
      I'm not writing this so you panic-call me. Please don't suddenly ring me like it's an emergency meeting. I'm not writing this expecting a reply. No pressure, no deadline, not even an emotional EMI.
    </p>
    <p class="handwritten">
      I'm writing this because I respect you enough to be honest. And I respect myself enough not to beg.
    </p>
    <p class="handwritten">
      If one day you look at me differently, I'll be there. Properly. Not half-hearted.
    </p>
    <p class="handwritten">
      If not, I'll still wish you happiness from a safe, slightly dramatic but very dignified distance.
    </p>
    <p class="handwritten">
      I don't want special treatment. I don't want VIP access. I just wanted you to know that someone sees you.
    </p>
    <p class="handwritten">
      The emotional you. The strong you. The confusing you. The "who the hell are you" you.
    </p>
    <p class="handwritten">
      And still says, "Yeah… I like her. No software update needed."
    </p>
    <p class="handwritten">
      If my presence ever feels safe to you, I'll protect that space. If it doesn't, I'll step back like a gentleman exiting a room — smooth and calm, no door slamming.
    </p>
    <p class="handwritten">
      Just sincerity.
    </p>
    
    <div class="signature">
      <p class="handwritten">
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