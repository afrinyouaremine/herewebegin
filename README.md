# here-we-begin
Deploying emotions to production
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Here We Begin</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500&family=Poppins:wght@300&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    height:100vh;
    background:#000;
    display:flex;
    justify-content:center;
    align-items:center;
    color:#fff;
    font-family:'Poppins',sans-serif;
    overflow:hidden;
}

/* 🌌 Star Sky */
.stars{
    position:fixed;
    width:100%;
    height:100%;
    overflow:hidden;
}

.star{
    position:absolute;
    width:2px;
    height:2px;
    background:white;
    border-radius:50%;
    animation:twinkle 3s infinite alternate;
}

@keyframes twinkle{
    from{opacity:0.2;}
    to{opacity:1;}
}

/* Password Screen */
.password-screen{
    text-align:center;
    z-index:10;
}

input{
    padding:10px;
    margin-top:15px;
    border:none;
    border-radius:5px;
    outline:none;
    text-align:center;
}

button{
    padding:8px 15px;
    margin-top:10px;
    border:none;
    border-radius:5px;
    cursor:pointer;
}

#errorMsg{
    margin-top:10px;
    color:#ff6b6b;
}

/* Main Content */
.container{
    display:none;
    text-align:center;
    max-width:600px;
    animation:fadeIn 2s ease-in forwards;
    z-index:10;
}

h1{
    font-family:'Playfair Display',serif;
    margin-bottom:20px;
}

p{
    margin:10px 0;
}

.heart{
    font-size:32px;
    margin-top:20px;
    animation:pulse 1.5s infinite;
}

@keyframes pulse{
    0%{transform:scale(1);}
    50%{transform:scale(1.3);}
    100%{transform:scale(1);}
}

@keyframes fadeIn{
    from{opacity:0;}
    to{opacity:1;}
}

@media(max-width:600px){
    h1{font-size:24px;}
    p{font-size:16px;}
}
</style>
</head>

<body>

<div class="stars" id="stars"></div>

<!-- 🔐 Password Screen -->
<div class="password-screen" id="passwordScreen">
    <h2>Before we begin...</h2>
    <p style="opacity:0.7; margin-top:10px;">
        Type the two digits we have in common.
    </p>
    <input type="password" id="passwordInput" placeholder="Two digits only">
    <br>
    <button onclick="checkPassword()">Unlock</button>
    <p id="errorMsg"></p>
</div>

<!-- ❤️ Main Content -->
<div class="container" id="mainContent">
    <h1 id="title"></h1>
    <p id="line1"></p>
    <p id="line2"></p>
    <p id="line3"></p>
    <div class="heart">❤</div>
    <p style="margin-top:20px;opacity:0.6;">– U</p>
</div>

<audio id="bgMusic" loop>
    <source src="https://cdn.pixabay.com/audio/2022/10/16/audio_5b0b5f7f7e.mp3" type="audio/mpeg">
</audio>

<script>
// 🌌 Generate Stars
for(let i=0;i<180;i++){
    let star=document.createElement("div");
    star.className="star";
    star.style.top=Math.random()*100+"%";
    star.style.left=Math.random()*100+"%";
    star.style.animationDuration=(Math.random()*3+2)+"s";
    document.getElementById("stars").appendChild(star);
}

// 🔐 Password Logic
const correctPassword="87";

function checkPassword(){
    const input=document.getElementById("passwordInput").value.trim();
    const errorMsg=document.getElementById("errorMsg");

    if(input===correctPassword){
        document.getElementById("passwordScreen").style.display="none";
        document.getElementById("mainContent").style.display="block";
        document.getElementById("bgMusic").play();
        startTyping();
    }else{
        errorMsg.innerHTML="That’s not our number 🙂";
    }
}

// ⌨️ Typewriter Effect
const titleText="If you're reading this...";
const lines=[
    "Then my courage finally showed up.",
    "Some feelings are too real to stay silent.",
    "You are one of them."
];

function typeWriter(element,text,speed,callback){
    let i=0;
    function typing(){
        if(i<text.length){
            element.innerHTML+=text.charAt(i);
            i++;
            setTimeout(typing,speed);
        }else if(callback){
            callback();
        }
    }
    typing();
}

function startTyping(){
    typeWriter(document.getElementById("title"),titleText,50,()=>{
        typeWriter(document.getElementById("line1"),lines[0],40,()=>{
            typeWriter(document.getElementById("line2"),lines[1],40,()=>{
                typeWriter(document.getElementById("line3"),lines[2],40);
            });
        });
    });
}
</script>

</body>
</html>
