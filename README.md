<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Access Locked</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500&family=Poppins:wght@300;400&display=swap');

*{
    box-sizing:border-box;
}

body{
    margin:0;
    padding:0;
    font-family:'Poppins',sans-serif;
    background:linear-gradient(135deg,#0f0f0f,#000000);
    color:#f2f2f2;
    overflow:hidden;
}

/* Floating Hearts */
.heart{
    position:absolute;
    color:#ff9aa2;
    opacity:0.4;
    animation:float 12s linear infinite;
}

@keyframes float{
    from{transform:translateY(100vh) scale(0.6);}
    to{transform:translateY(-10vh) scale(1);}
}

/* Glass Card */
.glass{
    position:absolute;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    width:90%;
    max-width:650px;
    padding:40px;
    background:rgba(255,255,255,0.05);
    backdrop-filter:blur(15px);
    border-radius:20px;
    text-align:center;
    box-shadow:0 0 20px rgba(255,154,162,0.2);
}

/* Headings */
h1{
    font-family:'Playfair Display',serif;
    color:#ffb3c1;
    margin-bottom:10px;
}

h2{
    color:#ffd6de;
    font-weight:400;
}

/* Input */
input{
    width:80%;
    padding:12px;
    margin-top:15px;
    border-radius:25px;
    border:none;
    outline:none;
    text-align:center;
    background:#1a1a1a;
    color:#ffffff;
}

/* Button */
button{
    margin-top:20px;
    padding:12px 25px;
    border-radius:25px;
    border:none;
    background:#ffb3c1;
    color:#000;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    background:#ffd6de;
}

/* Message text */
#typedText{
    margin-top:20px;
    font-size:15px;
    line-height:1.7;
    white-space:pre-line;
    color:#f5f5f5;
}

/* Heart Explosion */
.explosion{
    position:absolute;
    font-size:70px;
    color:#ffb3c1;
    animation:explode 1s ease-out forwards;
}

@keyframes explode{
    0%{transform:scale(0.5);opacity:1;}
    100%{transform:scale(3);opacity:0;}
}
</style>
</head>

<body>

<!-- ACCESS PAGE (VISIBLE FIRST) -->
<div class="glass" id="accessPage">
    <h1>🔐 Final Page Locked</h1>
    <h2>Enter the Access Code</h2>
    <input type="password" id="codeInput" placeholder="Enter Code">
    <br>
    <button onclick="checkCode()">Unlock</button>
    <p id="errorMsg" style="margin-top:10px;color:#ffb3c1;"></p>
</div>

<!-- FINAL PAGE (HIDDEN BY DEFAULT) -->
<div class="glass" id="finalPage" style="display:none;">
    <h1>❤️ Access Granted</h1>
    <div id="typedText"></div>
</div>

<script>

/* Ensure correct initial state */
document.getElementById("finalPage").style.display = "none";

/* Floating Hearts */
for(let i=0;i<30;i++){
    let heart=document.createElement("div");
    heart.innerHTML="❤";
    heart.className="heart";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(Math.random()*18+12)+"px";
    heart.style.animationDuration=(Math.random()*8+6)+"s";
    document.body.appendChild(heart);
}

/* Message */
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

/* Unlock Logic */
function checkCode(){
    let code=document.getElementById("codeInput").value.trim();

    if(code.toLowerCase()==="nirfa"){
        document.getElementById("accessPage").style.display="none";
        document.getElementById("finalPage").style.display="block";
        explodeHeart();
        typeEffect();
    }else{
        document.getElementById("errorMsg").innerText="Access Denied… Try Again.";
    }
}

/* Explosion */
function explodeHeart(){
    let heart=document.createElement("div");
    heart.innerHTML="❤";
    heart.className="explosion";
    heart.style.top="50%";
    heart.style.left="50%";
    document.body.appendChild(heart);
}

/* Typing Effect */
function typeEffect(){
    let i=0;
    function typing(){
        if(i<message.length){
            document.getElementById("typedText").innerHTML+=message.charAt(i);
            i++;
            setTimeout(typing,25);
        }
    }
    typing();
}

</script>

</body>
</html>