# To the Queen of My Heart
Deploying emotions to production
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Here We Begin</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Montserrat:wght@300;400&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;}

body{
    min-height:100vh;
    font-family:'Montserrat',sans-serif;
    overflow-y:auto;
    display:flex;
    justify-content:center;
    padding:30px 15px;
    transition:background 1s ease;
}

/* Different romantic backgrounds */
.bg1{
    background: linear-gradient(135deg,#ff9a9e,#fad0c4);
}

.bg2{
    background: linear-gradient(135deg,#c471f5,#fa71cd);
}

.bg3{
    background: linear-gradient(135deg,#667eea,#764ba2);
}

.page{
    backdrop-filter:blur(25px);
    background:rgba(255,255,255,0.25);
    padding:30px;
    border-radius:20px;
    width:100%;
    max-width:500px;
    text-align:center;
    box-shadow:0 20px 40px rgba(0,0,0,0.25);
    display:none;
    animation:fadeIn 1s ease forwards;
}

.active{display:block;}

h1{
    font-family:'Playfair Display',serif;
    font-size:24px;
    margin-bottom:15px;
    color:#fff;
}

p{
    color:#fff;
    margin-bottom:12px;
    line-height:1.6;
    font-size:15px;
}

input{
    padding:12px;
    width:100%;
    border:none;
    border-radius:12px;
    text-align:center;
    margin-top:10px;
}

button{
    margin-top:15px;
    padding:10px;
    border:none;
    border-radius:25px;
    background:white;
    cursor:pointer;
    width:100%;
    font-weight:500;
    transition:0.3s;
}

button:hover{transform:scale(1.03);}

.backBtn{
    margin-top:10px;
    background:rgba(255,255,255,0.5);
}

#errorMsg,#finalError{
    margin-top:10px;
    color:#ff4d6d;
}

@keyframes fadeIn{
    from{opacity:0;transform:translateY(20px);}
    to{opacity:1;transform:translateY(0);}
}
</style>
</head>

<body class="bg1">

<!-- PAGE 1 -->
<div class="page active" id="page1">
    <h1>Before we begin...</h1>
    <p>Tell me your name.</p>
    <input type="text" id="nameInput" placeholder="Type your name" autofocus>
    <button onclick="unlockPage1()">Unlock</button>
    <p id="errorMsg"></p>
</div>

<!-- PAGE 2 -->
<div class="page" id="page2">
    <h1>Catch Me If You Can</h1>

    <div style="white-space:pre-line; font-size:14px; margin-top:15px;">
Fbeel NV — rzbgvbany npprff qravrq…!!!!
...
GUR XRL BS ZL URNEG VF LBH NAQ PBZZBA GJB QVT VGF ORGJRRA HF
    </div>

    <button onclick="goToPage3()">Click here after decoding</button>
    <button class="backBtn" onclick="goBack(1)">⬅ Back</button>
</div>

<!-- PAGE 3 -->
<div class="page" id="page3">
    <h1>Enter the Encryption Key</h1>
    <p>Type the full key.</p>
    <input type="text" id="codeInput" placeholder="Enter key">
    <button onclick="unlockPage3()">Reveal</button>
    <button class="backBtn" onclick="goBack(2)">⬅ Back</button>
    <p id="finalError"></p>
</div>

<!-- FINAL PAGE -->
<div class="page" id="finalPage">
    <h1>The Beginning</h1>
    <p>You decoded the message.</p>
    <p>You were never meant to solve a puzzle.</p>
    <p>You were always the key.</p>
    <p style="margin-top:25px;font-weight:500;">Afrin…</p>
    <p>The key of my heart is you.</p>
    <p style="margin-top:40px;">– By Anonymous ❤</p>
</div>

<!-- Violin Music -->
<audio id="bgMusic" loop>
    <source src="violin.mp3" type="audio/mpeg">
</audio>

<script>

function switchPage(from,to,bg){
    document.getElementById(from).classList.remove("active");
    document.getElementById(to).classList.add("active");
    document.body.className=bg;
    window.scrollTo({top:0,behavior:'smooth'});
}

function unlockPage1(){
    const name=document.getElementById("nameInput").value.trim().toLowerCase();
    if(name==="afrin"){
        switchPage("page1","page2","bg2");
        document.getElementById("bgMusic").play();
    }else{
        document.getElementById("errorMsg").innerHTML=
        "Hmm… this story is waiting for someone specific 😉";
    }
}

function goToPage3(){
    switchPage("page2","page3","bg3");
}

function unlockPage3(){
    const input=document.getElementById("codeInput").value.trim().toLowerCase();
    if(input==="afrin87"){
        switchPage("page3","finalPage","bg1");
    }else{
        document.getElementById("finalError").innerHTML=
        "That’s not the full key… look deeper 😉";
    }
}

function goBack(page){
    if(page===1){
        switchPage("page2","page1","bg1");
    }
    if(page===2){
        switchPage("page3","page2","bg2");
    }
}

</script>

</body>
</html>
