<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Here We Begin</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600&family=Poppins:wght@300;400&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;}

body{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:'Poppins',sans-serif;
    background:#000;
    overflow:hidden;
}

/* Floating glowing hearts */
.heart-particle{
    position:absolute;
    width:15px;
    height:15px;
    background:red;
    transform:rotate(-45deg);
    animation:floatUp linear infinite;
    filter:drop-shadow(0 0 8px red);
    opacity:0.8;
}

.heart-particle:before,
.heart-particle:after{
    content:"";
    position:absolute;
    width:15px;
    height:15px;
    background:red;
    border-radius:50%;
}

.heart-particle:before{ top:-7px; left:0; }
.heart-particle:after{ left:7px; top:0; }

@keyframes floatUp{
    0%{
        transform:translateY(100vh) rotate(-45deg) scale(0.5);
        opacity:0;
    }
    20%{opacity:1;}
    100%{
        transform:translateY(-10vh) rotate(-45deg) scale(1);
        opacity:0;
    }
}

/* Acrylic Card */
.page{
    width:90%;
    max-width:520px;
    padding:40px;
    border-radius:25px;
    backdrop-filter:blur(25px);
    background:rgba(255,255,255,0.08);
    border:1px solid rgba(255,0,0,0.3);
    box-shadow:0 0 40px rgba(255,0,0,0.3);
    text-align:center;
    display:none;
    animation:fadeIn 1.2s ease forwards;
    z-index:10;
}

.active{display:block;}

h1{
    font-family:'Playfair Display',serif;
    color:#fff;
    margin-bottom:20px;
}

p{
    color:#ddd;
    line-height:1.7;
    margin-bottom:14px;
}

input{
    width:100%;
    padding:12px;
    border-radius:30px;
    border:1px solid rgba(255,255,255,0.4);
    background:rgba(255,255,255,0.1);
    color:#fff;
    text-align:center;
    margin-top:15px;
}

button{
    margin-top:18px;
    padding:12px;
    width:100%;
    border-radius:30px;
    border:none;
    background:linear-gradient(90deg,#ff0000,#b30000);
    color:#fff;
    font-weight:600;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    transform:scale(1.05);
    box-shadow:0 0 20px red;
}

.error{
    color:#ff4d6d;
    margin-top:12px;
}

@keyframes fadeIn{
    from{opacity:0;transform:translateY(20px);}
    to{opacity:1;transform:translateY(0);}
}
</style>
</head>

<body>

<!-- IDENTITY PAGE -->
<div class="page active" id="identityPage">
    <h1>Claim Your Gift 👑</h1>
    <p>If you are her… type your name.</p>
    <input type="text" id="nameInput" placeholder="Enter your name">
    <button onclick="checkIdentity()">Claim</button>
    <p id="errorMsg" class="error"></p>
</div>

<!-- MESSAGE PAGE -->
<div class="page" id="messagePage">
    <h1>Hi Afrin…</h1>
    <p>Okay… don’t freak out.</p>
    <p>Nothing dramatic is happening.</p>
    <p>I just decided to be bold for once.</p>
    <p>You have this calm way of existing that quietly shifts the atmosphere.</p>
    <p>It’s impressive. Slightly unfair. But impressive.</p>
    <p>If you’re smiling right now… good.</p>
    <p>If you’re pretending not to smile… even better.</p>
    <p style="margin-top:20px;">– By Anonymous ❤</p>
</div>

<audio id="bgMusic" loop>
    <source src="violin.mp3" type="audio/mpeg">
</audio>

<script>

/* Generate floating hearts */
for(let i=0; i<60; i++){
    let heart=document.createElement("div");
    heart.className="heart-particle";
    heart.style.left=Math.random()*100+"%";
    heart.style.animationDuration=(6 + Math.random()*6)+"s";
    heart.style.animationDelay=Math.random()*5+"s";
    heart.style.width=(10 + Math.random()*12)+"px";
    heart.style.height=heart.style.width;
    document.body.appendChild(heart);
}

function checkIdentity(){
    const name=document.getElementById("nameInput").value.trim().toLowerCase();

    if(name==="afrin"){
        document.getElementById("identityPage").classList.remove("active");
        document.getElementById("messagePage").classList.add("active");
        document.getElementById("bgMusic").play();
    } else {
        document.getElementById("errorMsg").innerHTML=
        "This throne answers to only one name… and my Queen wears another.";
    }
}

</script>

</body>
</html>