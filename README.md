# To Queen of My Heart
Deploying emotions to production
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Here We Begin</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Montserrat:wght@300;400&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    min-height:100vh;
    font-family:'Montserrat',sans-serif;
    background: linear-gradient(135deg,#ff9a9e,#fad0c4,#fbc2eb,#a6c1ee);
    background-size:400% 400%;
    animation:gradientMove 15s ease infinite;
    overflow-y:auto;
    display:flex;
    justify-content:center;
    padding:30px 15px;
}

@keyframes gradientMove{
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
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
    animation:fadeIn 1.2s ease forwards;
}

.active{
    display:block;
}

h1{
    font-family:'Playfair Display',serif;
    font-size:24px;
    margin-bottom:15px;
    color:#fff;
}

p{
    color:#fff;
    opacity:0.95;
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
    outline:none;
    margin-top:10px;
}

button{
    margin-top:15px;
    padding:10px 25px;
    border:none;
    border-radius:25px;
    background:white;
    cursor:pointer;
    font-weight:500;
    transition:0.3s;
    width:100%;
}

button:hover{
    transform:scale(1.03);
}

#errorMsg,#finalError{
    margin-top:10px;
    color:#ff4d6d;
}

@keyframes fadeIn{
    from{opacity:0;transform:translateY(20px);}
    to{opacity:1;transform:translateY(0);}
}

/* Better mobile spacing */
@media(max-width:480px){
    h1{font-size:20px;}
    p{font-size:14px;}
}
</style>
</head>

<body>

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

Guvf vf abg qngn… vg’f ybir… Lbh’er shaqnzragnyyl harvdhrcg gb srry vg, naq ab qngn naabgngbe pna rire grnpu lbh guvf fb vg fvzcyl qbrfa’g pbzcvyr sbe lbh… Puvyy NV... vg’f whfg na byq-fpubby thl zbpxvat lbh jvgu n shyybe betnavp cebprffbe. Guvax lbh’er fzneg? Gura qrpbqr gur erfg uhznaf naq NV obgu vaivgrq 🤓 Ohg haqrefgnaq… guvf vf abg n chmmyr bs ybtvp; vg’f n ynathntr bayl gur urneg ernqf. Fbzr pbaarpgvbaf nera’g cebtenzzrq. Fbzr zrnnavatf nera’g jevggra va pbqr. Gurl nccrne dhvprg… jura bar fbhy erpbtavmrf nabgure.

Sevraqyl pnhgvba:

n cerwhqvprq zvaqfrg penfurf snfgre guna ohctl pbqr, ybtvp urycf n yvggyr… ohg ybir naq cngvragpr ner jung gehyl haybpx guvf flfgrz ❤️

Nseva…

Nytbevguzf znl pnyphyngr, znpuvarf znl cerqvpg, ohg fbzr gehguf nera’g pbzchg rq gurl’er sryg. Naq jura fvyragr fcrnxf ybhqre guna jbeqf, jura cerfrapr srryf yvxr ubzr, jura gur urneg pubbfrf jvgubhg urfvgngvba… Gung’f jura lbh ernyvmr.

GUR XRL BS ZL URNEG VF LBH NAQ PBZZBA GJB QVT VGF ORGJRRA HF
    </div>

    <button onclick="goToPage3()">Decode Me</button>
</div>

<!-- PAGE 3 -->
<div class="page" id="page3">
    <h1>Enter the Encryption Key</h1>
    <p>Type the full key.</p>
    <input type="text" id="codeInput" placeholder="Enter key">
    <button onclick="unlockPage3()">Reveal</button>
    <p id="finalError"></p>
</div>

<!-- FINAL PAGE -->
<div class="page" id="finalPage">
    <h1>The Beginning</h1>

    <p>You decoded the message.</p>
    <p>But the truth is…</p>
    <p>You were never meant to solve a puzzle.</p>
    <p>You were always the key.</p>

    <p style="margin-top:20px;">
        Not because of logic.<br>
        Not because of coincidence.
    </p>

    <p>
        But because when something feels right,
        it doesn’t need to be explained.
    </p>

    <p style="margin-top:25px; font-weight:500;">
        Afrin…
    </p>

    <p>
        The key of my heart is you.
    </p>

    <p style="margin-top:30px; opacity:0.8;">
        And maybe… this is where we begin.
    </p>

    <p style="margin-top:40px;">
        – By Anonymous ❤
    </p>
</div>

<script>

function switchPage(from,to){
    document.getElementById(from).classList.remove("active");
    document.getElementById(to).classList.add("active");
    window.scrollTo({top:0, behavior:'smooth'});
}

function unlockPage1(){
    const name=document.getElementById("nameInput").value.trim().toLowerCase();
    if(name==="afrin"){
        switchPage("page1","page2");
    }else{
        document.getElementById("errorMsg").innerHTML=
        "Hmm… this story is waiting for someone specific 😉";
    }
}

function goToPage3(){
    switchPage("page2","page3");
}

function unlockPage3(){
    const input=document.getElementById("codeInput").value.trim().toLowerCase();
    if(input==="afrin87"){
        switchPage("page3","finalPage");
    }else{
        document.getElementById("finalError").innerHTML=
        "That’s not the full key… look deeper 😉";
    }
}

</script>

</body>
</html>
