<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Catch Me If You Can</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Poppins:wght@300;400&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;}

body{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:'Poppins',sans-serif;
    overflow:hidden;
    transition:background 1.5s ease;
}

/* LUXURY GRADIENTS */
.bg1{background:linear-gradient(135deg,#2b1055,#7597de);}
.bg2{background:linear-gradient(135deg,#3a1c71,#d76d77,#ffaf7b);}
.bg3{background:linear-gradient(135deg,#141e30,#243b55);}
.bg4{background:linear-gradient(135deg,#42275a,#734b6d);}

/* FLOATING LIGHT PARTICLES */
.particle{
    position:absolute;
    width:6px;
    height:6px;
    background:rgba(255,255,255,0.6);
    border-radius:50%;
    animation:float 12s linear infinite;
}

@keyframes float{
    from{transform:translateY(100vh);opacity:0;}
    50%{opacity:0.6;}
    to{transform:translateY(-10vh);opacity:0;}
}

/* ACRYLIC GLASS CARD */
.page{
    position:relative;
    width:90%;
    max-width:480px;
    padding:40px;
    border-radius:25px;
    background:rgba(255,255,255,0.12);
    backdrop-filter:blur(30px);
    border:1px solid rgba(255,255,255,0.3);
    box-shadow:0 0 40px rgba(255,255,255,0.2);
    text-align:center;
    display:none;
    animation:fadeIn 1.5s ease forwards;
}

/* Shine Sweep */
.page::before{
    content:'';
    position:absolute;
    top:0;
    left:-100%;
    width:100%;
    height:100%;
    background:linear-gradient(120deg,transparent,rgba(255,255,255,0.4),transparent);
    transform:skewX(-20deg);
    animation:shine 5s infinite;
}

@keyframes shine{
    0%{left:-100%;}
    50%{left:100%;}
    100%{left:100%;}
}

.active{display:block;}

h1{
    font-family:'Playfair Display',serif;
    font-size:26px;
    color:#fff;
    margin-bottom:20px;
    letter-spacing:1px;
}

p{
    color:#f1f1f1;
    line-height:1.6;
    margin-bottom:12px;
    font-size:15px;
}

input{
    width:100%;
    padding:12px;
    border-radius:30px;
    border:1px solid rgba(255,255,255,0.6);
    background:rgba(255,255,255,0.2);
    color:#fff;
    text-align:center;
    outline:none;
    margin-top:15px;
}

button{
    margin-top:18px;
    padding:10px;
    width:100%;
    border-radius:30px;
    border:none;
    background:linear-gradient(90deg,#ffd700,#ffb347);
    color:#000;
    font-weight:600;
    cursor:pointer;
    transition:0.4s;
}

button:hover{
    transform:scale(1.05);
    box-shadow:0 0 20px gold;
}

.backBtn{
    background:rgba(255,255,255,0.3);
    color:#fff;
}

@keyframes fadeIn{
    from{opacity:0;transform:translateY(20px);}
    to{opacity:1;transform:translateY(0);}
}

/* FINAL TEXT REVEAL */
.reveal{
    opacity:0;
    animation:fadeIn 2s forwards;
}
</style>
</head>

<body class="bg1">

<script>
/* Create floating particles */
for(let i=0;i<40;i++){
    let p=document.createElement("div");
    p.className="particle";
    p.style.left=Math.random()*100+"%";
    p.style.animationDuration=(10+Math.random()*10)+"s";
    document.body.appendChild(p);
}
</script>

<!-- PAGE 1 -->
<div class="page active" id="page1">
    <h1>Before we begin...</h1>
    <p>Tell me your name.</p>
    <input type="text" id="nameInput" placeholder="Type your name">
    <button onclick="unlockPage1()">Enter</button>
</div>

<!-- PAGE 2 -->
<div class="page" id="page2">
    <h1 style="color:gold;">Catch Me If You Can</h1>
    <p style="white-space:pre-line;font-size:14px;">
Fbeel NV — rzbgvbany npprff qravrq…!!!!
...
GUR XRL BS ZL URNEG VF LBH NAQ PBZZBA GJB QVT VGF ORGJRRA HF
    </p>
    <button onclick="goToPage3()">Click here after decoding</button>
    <button class="backBtn" onclick="goBack(1)">Back</button>
</div>

<!-- PAGE 3 -->
<div class="page" id="page3">
    <h1>Enter the Encryption Key</h1>
    <input type="text" id="codeInput" placeholder="Enter key">
    <button onclick="unlockPage3()">Reveal</button>
    <button class="backBtn" onclick="goBack(2)">Back</button>
</div>

<!-- FINAL PAGE -->
<div class="page" id="page4">
    <h1 class="reveal">The Beginning</h1>
    <p class="reveal" style="animation-delay:1s;">You were never meant to solve a puzzle.</p>
    <p class="reveal" style="animation-delay:2s;">You were always the key.</p>
    <p class="reveal" style="animation-delay:3s;">Afrin…</p>
    <p class="reveal" style="animation-delay:4s;">The key of my heart is you.</p>
    <p class="reveal" style="animation-delay:5s;">– By Anonymous ❤</p>
</div>

<!-- VIOLIN MUSIC -->
<audio id="bgMusic" loop>
    <source src="violin.mp3" type="audio/mpeg">
</audio>

<script>
function switchPage(from,to,bg){
    document.getElementById(from).classList.remove("active");
    document.getElementById(to).classList.add("active");
    document.body.className=bg;
}

function unlockPage1(){
    const name=document.getElementById("nameInput").value.trim().toLowerCase();
    if(name==="afrin"){
        switchPage("page1","page2","bg2");
        document.getElementById("bgMusic").play();
    }
}

function goToPage3(){
    switchPage("page2","page3","bg3");
}

function unlockPage3(){
    const input=document.getElementById("codeInput").value.trim().toLowerCase();
    if(input==="afrin87"){
        switchPage("page3","page4","bg4");
    }
}

function goBack(page){
    if(page===1){switchPage("page2","page1","bg1");}
    if(page===2){switchPage("page3","page2","bg2");}
}
</script>

</body>
</html>
