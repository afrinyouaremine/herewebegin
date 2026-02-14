# here-we-begin
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
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:'Montserrat', sans-serif;
    background: linear-gradient(135deg, #ff9a9e, #fad0c4, #fbc2eb, #a6c1ee);
    background-size: 400% 400%;
    animation: gradientMove 15s ease infinite;
    overflow:hidden;
}

/* Animated gradient */
@keyframes gradientMove {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

/* Glass card */
.card{
    backdrop-filter: blur(20px);
    background: rgba(255,255,255,0.25);
    padding:40px;
    border-radius:20px;
    width:90%;
    max-width:420px;
    text-align:center;
    box-shadow:0 15px 35px rgba(0,0,0,0.2);
    animation: fadeIn 1.5s ease forwards;
}

h1{
    font-family:'Playfair Display', serif;
    font-size:28px;
    margin-bottom:15px;
    color:#fff;
}

p{
    color:#fff;
    opacity:0.9;
    margin-bottom:15px;
}

input{
    padding:10px;
    width:80%;
    border:none;
    border-radius:10px;
    text-align:center;
    outline:none;
}

button{
    margin-top:15px;
    padding:8px 20px;
    border:none;
    border-radius:20px;
    background:white;
    cursor:pointer;
    font-weight:500;
}

#errorMsg{
    margin-top:10px;
    color:#ff4d6d;
}

.hidden{
    display:none;
}

@keyframes fadeIn{
    from{opacity:0; transform:translateY(20px);}
    to{opacity:1; transform:translateY(0);}
}

/* Floating hearts */
.heart{
    position:absolute;
    font-size:18px;
    color:white;
    opacity:0.3;
    animation: floatUp 6s linear infinite;
}

@keyframes floatUp{
    from{transform:translateY(100vh);}
    to{transform:translateY(-10vh);}
}
</style>
</head>

<body>

<!-- Floating Hearts -->
<script>
for(let i=0;i<20;i++){
    let heart=document.createElement("div");
    heart.className="heart";
    heart.innerHTML="❤";
    heart.style.left=Math.random()*100+"%";
    heart.style.animationDuration=(Math.random()*5+5)+"s";
    document.body.appendChild(heart);
}
</script>

<!-- Unlock Card -->
<div class="card" id="unlockCard">
    <h1>Before we begin...</h1>
    <p>Tell me your name.</p>
    <input type="text" id="nameInput" placeholder="Type your name">
    <br>
    <button onclick="checkName()">Unlock</button>
    <p id="errorMsg"></p>
</div>

<!-- Love Message Card -->
<div class="card hidden" id="loveCard">
    <h1>Here We Begin</h1>
    <p>If you're reading this,</p>
    <p>then my courage finally won.</p>
    <p>You matter to me more than I can explain.</p>
    <p style="margin-top:20px;">– U ❤</p>
</div>

<script>
function checkName(){
    const input=document.getElementById("nameInput").value.trim().toLowerCase();
    const errorMsg=document.getElementById("errorMsg");

    if(input==="afrin"){
        document.getElementById("unlockCard").classList.add("hidden");
        document.getElementById("loveCard").classList.remove("hidden");
    }else{
        errorMsg.innerHTML="Hmm… this page seems to know exactly who it's waiting for 😉";
    }
}
</script>

</body>
</html>
