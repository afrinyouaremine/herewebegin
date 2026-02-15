<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Access Restricted</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500&family=Poppins:wght@300;400&display=swap');

body{
    margin:0;
    padding:0;
    background:radial-gradient(circle at center,#0a0a0a,#000000);
    overflow:hidden;
    font-family:'Poppins',sans-serif;
    color:#f5f5f5;
}

/* Floating Hearts */
.heart{
    position:absolute;
    color:#ff1744;
    animation:float 8s linear infinite;
    opacity:0.5;
    text-shadow:0 0 8px #ff1744;
}

@keyframes float{
    0%{transform:translateY(100vh) scale(0.5);}
    100%{transform:translateY(-10vh) scale(1.2);}
}

/* Center Glass Box */
.glass{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    background:rgba(255,255,255,0.05);
    backdrop-filter:blur(12px);
    padding:40px;
    border-radius:20px;
    text-align:center;
    width:90%;
    max-width:650px;
    box-shadow:0 0 25px rgba(255,23,68,0.25);
}

/* Titles */
h1{
    font-family:'Playfair Display',serif;
    color:#ff3d5a;
    letter-spacing:1px;
}

h2{
    color:#ff8fa3;
    font-weight:400;
}

/* Input */
input{
    padding:12px;
    width:80%;
    margin-top:15px;
    border-radius:30px;
    border:none;
    outline:none;
    text-align:center;
    font-size:16px;
    background:#1a1a1a;
    color:#ffffff;
}

/* Button */
button{
    margin-top:20px;
    padding:12px 25px;
    border:none;
    border-radius:30px;
    background:#ff1744;
    color:white;
    font-size:16px;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    background:#ff0033;
    box-shadow:0 0 15px #ff1744;
}

/* Typing text */
#typedText{
    margin-top:20px;
    font-size:15px;
    color:#e0e0e0;
    line-height:1.7;
    white-space:pre-line;
}

/* Highlight final line */
.highlight{
    color:#ff3d5a;
    font-weight:600;
}

/* Heart Explosion */
.explosion{
    position:absolute;
    font-size:60px;
    color:#ff1744;
    animation:explode 1s ease-out forwards;
}

@keyframes explode{
    0%{transform:scale(0.5);opacity:1;}
    100%{transform:scale(4);opacity:0;}
}
</style>
</head>

<body>

<script>
for(let i=0;i<35;i++){
    let heart=document.createElement("div");
    heart.innerHTML="❤";
    heart.className="heart";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(Math.random()*20+10)+"px";
    heart.style.animationDuration=(Math.random()*5+5)+"s";
    document.body.appendChild(heart);
}
</script>

<!-- ACCESS PAGE -->
<div class="glass" id="accessPage">
    <h1>🔐 Final Page Locked</h1>
    <h2>Enter the Access Code</h2>
    <input type="password" id="codeInput" placeholder="Enter Code">
    <br>
    <button onclick="checkCode()">Unlock</button>
    <p id="errorMsg" style="color:#ff3d5a;margin-top:10px;"></p>
</div>

<!-- FINAL PAGE -->
<div class="glass" id="finalPage" style="display:none;">
    <h1>❤️ Access Granted</h1>
    <div id="typedText"></div>
</div>

<script>

const message = `You said this isn’t data — it’s love —
but you wrapped it in a substitution cipher.

Oh… okay, you made it this far.
But sorry, AI — emotional access is still denied…!!!!

This isn’t data. It’s love.

You’re fundamentally unequipped to feel it,
and no data annotator can ever teach you this —
so it simply doesn’t compile for you…

Relax, AI…
It’s just an old-school guy
mocking you with a fully organic processor.

Think you’re smart? Then decode the next page —
humans and AI both invited 🤓

But understand…
This isn’t a puzzle of logic.
It’s a language only the heart can read.

Some connections aren’t programmed.
Some meanings aren’t written in code.

They appear quietly…
when one soul recognizes another.

Friendly caution:
An ignorant mindset crashes faster than buggy code.

Logic helps a little…
but love and patience are what truly unlock this system ❤️

Afrin...

Algorithms may calculate.
Machines may predict.

But THE KEY OF MY HEART IS YOU.`;

function checkCode(){
    let code=document.getElementById("codeInput").value;
    if(code.toLowerCase()==="nirfa"){
        document.getElementById("accessPage").style.display="none";
        document.getElementById("finalPage").style.display="block";
        explodeHeart();
        typeEffect();
    }else{
        document.getElementById("errorMsg").innerText="Access Denied… Try Again.";
    }
}

function explodeHeart(){
    let heart=document.createElement("div");
    heart.innerHTML="❤";
    heart.className="explosion";
    heart.style.top="50%";
    heart.style.left="50%";
    document.body.appendChild(heart);
}

function typeEffect(){
    let i=0;
    function typing(){
        if(i<message.length){
            document.getElementById("typedText").innerHTML+=message.charAt(i);
            i++;
            setTimeout(typing,30);
        }
    }
    typing();
}
</script>

</body>
</html>