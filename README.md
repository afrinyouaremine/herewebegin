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
    transition:background 1s ease;
    overflow:hidden;
}

/* Background Themes */
.bg1{
    background:linear-gradient(rgba(0,0,0,0.6),rgba(0,0,0,0.6)),
    url('romantic1.jpg') center/cover no-repeat;
}

.bg2{
    background:linear-gradient(rgba(0,0,0,0.6),rgba(0,0,0,0.6)),
    url('romantic2.jpg') center/cover no-repeat;
}

/* Acrylic Card */
.page{
    width:90%;
    max-width:520px;
    padding:40px;
    border-radius:25px;
    backdrop-filter:blur(25px);
    background:rgba(255,255,255,0.12);
    border:1px solid rgba(255,255,255,0.25);
    box-shadow:0 0 40px rgba(0,0,0,0.5);
    text-align:center;
    display:none;
    animation:fadeIn 1s ease forwards;
}

.active{display:block;}

h1{
    font-family:'Playfair Display',serif;
    font-size:26px;
    color:#fff;
    margin-bottom:20px;
}

p{
    color:#f1f1f1;
    line-height:1.7;
    margin-bottom:14px;
    font-size:15px;
}

input{
    width:100%;
    padding:12px;
    border-radius:30px;
    border:1px solid rgba(255,255,255,0.5);
    background:rgba(255,255,255,0.2);
    color:#fff;
    text-align:center;
    outline:none;
    margin-top:15px;
}

button{
    margin-top:18px;
    padding:12px;
    width:100%;
    border-radius:30px;
    border:none;
    background:linear-gradient(90deg,#d4af37,#ffd700);
    color:#000;
    font-weight:600;
    cursor:pointer;
    transition:0.3s;
}

button:hover{
    transform:scale(1.05);
    box-shadow:0 0 20px gold;
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

<body class="bg1">

<!-- INTRO SCREEN -->
<div class="page active" id="introPage">
    <h1>Welcome…</h1>
    <p>A gift has been prepared.</p>
    <p>But not for everyone.</p>
    <p>Only for one Queen.</p>
</div>

<!-- IDENTITY PAGE -->
<div class="page" id="identityPage">
    <h1>Claim Your Gift 👑</h1>
    <p>If you are her…</p>
    <p>Type your name to claim it.</p>
    <input type="text" id="nameInput" placeholder="Enter your name">
    <button onclick="checkIdentity()">Claim the Gift</button>
    <p id="errorMsg" class="error"></p>
</div>

<!-- MESSAGE PAGE -->
<div class="page" id="messagePage">
    <h1>Hi Afrin…</h1>
    <p>
        Okay… first rule.
        Don’t freak out.
    </p>

    <p>
        Nothing dramatic is happening.
        Just me… choosing to be bold for once.
    </p>

    <p>
        I figured if I’m going to approach a Queen,
        I shouldn’t do it casually.
    </p>

    <p>
        You have this calm way of existing
        like you don’t realize you quietly change the atmosphere.
    </p>

    <p>
        It’s impressive.
        Slightly unfair.
        But impressive.
    </p>

    <p>
        So relax.
        No pressure.
        Just intentional energy.
    </p>

    <p>
        And if you’re smiling right now…
        good.
    </p>

    <p>
        If you’re pretending not to smile…
        even better.
    </p>

    <p style="margin-top:20px;">
        – By Anonymous ❤
    </p>
</div>

<script>

/* Auto move from intro to identity after 3 seconds */
setTimeout(() => {
    switchPage("introPage","identityPage","bg1");
}, 3000);

function switchPage(from,to,bg){
    document.getElementById(from).classList.remove("active");
    document.getElementById(to).classList.add("active");
    document.body.className=bg;
}

function checkIdentity(){
    const name=document.getElementById("nameInput").value.trim().toLowerCase();

    if(name==="afrin"){
        switchPage("identityPage","messagePage","bg2");
    } else {
        document.getElementById("errorMsg").innerHTML=
        "This throne answers to only one name… and my Queen wears another.";
    }
}

</script>

</body>
</html>