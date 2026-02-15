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

/* Acrylic Card */
.page{
    width:90%;
    max-width:520px;
    padding:40px;
    border-radius:25px;
    backdrop-filter:blur(20px);
    background:rgba(255,255,255,0.08);
    border:1px solid rgba(255,255,255,0.2);
    box-shadow:0 0 40px rgba(255,0,0,0.2);
    text-align:center;
    display:none;
    animation:fadeIn 1.5s ease forwards;
}

.active{display:block;}

h1{
    font-family:'Playfair Display',serif;
    color:#fff;
    margin-bottom:20px;
}

p{
    color:#ddd;
    line-height:1.6;
    margin-bottom:12px;
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

/* Heart */
.heart{
    width:120px;
    height:120px;
    background:red;
    position:relative;
    transform:rotate(-45deg);
    animation:pulse 1.2s infinite;
}

.heart:before,
.heart:after{
    content:"";
    width:120px;
    height:120px;
    background:red;
    border-radius:50%;
    position:absolute;
}

.heart:before{ top:-60px; left:0; }
.heart:after{ left:60px; top:0; }

@keyframes pulse{
    0%{transform:rotate(-45deg) scale(1);}
    50%{transform:rotate(-45deg) scale(1.15);}
    100%{transform:rotate(-45deg) scale(1);}
}

/* Explosion */
@keyframes explode{
    0%{opacity:1; transform:scale(1);}
    70%{transform:scale(3); opacity:1;}
    100%{opacity:0; transform:scale(4);}
}

/* Fade */
@keyframes fadeIn{
    from{opacity:0; transform:translateY(20px);}
    to{opacity:1; transform:translateY(0);}
}

/* Screen shake */
@keyframes shake{
    0%{transform:translateX(0);}
    25%{transform:translateX(-10px);}
    50%{transform:translateX(10px);}
    75%{transform:translateX(-5px);}
    100%{transform:translateX(0);}
}
</style>
</head>

<body>

<!-- INTRO -->
<div id="intro" style="position:absolute;">
    <div class="heart" id="heart"></div>
</div>

<!-- IDENTITY PAGE -->
<div class="page" id="identityPage">
    <h1>Claim Your Gift 👑</h1>
    <p>If you are her… type your name.</p>
    <input type="text" id="nameInput" placeholder="Enter your name">
    <button onclick="checkIdentity()">Claim</button>
    <p id="errorMsg" style="color:#ff4d6d;"></p>
</div>

<!-- MESSAGE PAGE -->
<div class="page" id="messagePage">
    <h1>Hi Afrin…</h1>
    <p>Okay… don’t freak out.</p>
    <p>Nothing dramatic is happening.</p>
    <p>I just decided to be bold for once.</p>
    <p>You have this calm way of existing that shifts the room quietly.</p>
    <p>It’s impressive. Slightly unfair. But impressive.</p>
    <p>If you’re smiling right now… good.</p>
    <p>If you’re pretending not to smile… even better.</p>
    <p style="margin-top:20px;">– By Anonymous ❤</p>
</div>

<audio id="bgMusic" loop>
    <source src="violin.mp3" type="audio/mpeg">
</audio>

<script>

/* Explosion Sequence */
setTimeout(() => {
    document.getElementById("heart").style.animation="explode 1.5s forwards";
    document.body.style.animation="shake 0.5s";
    document.getElementById("bgMusic").play();
}, 2500);

setTimeout(() => {
    document.getElementById("intro").style.display="none";
    document.getElementById("identityPage").classList.add("active");
}, 4500);

function checkIdentity(){
    const name=document.getElementById("nameInput").value.trim().toLowerCase();
    if(name==="afrin"){
        document.getElementById("identityPage").classList.remove("active");
        document.getElementById("messagePage").classList.add("active");
    }else{
        document.getElementById("errorMsg").innerHTML=
        "This throne answers to only one name… and my Queen wears another.";
    }
}

</script>

</body>
</html>