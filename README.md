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
*{margin:0;padding:0;box-sizing:border-box;}

body{
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    font-family:'Montserrat',sans-serif;
    background: linear-gradient(135deg,#ff9a9e,#fad0c4,#fbc2eb,#a6c1ee);
    background-size:400% 400%;
    animation:gradientMove 15s ease infinite;
    overflow:hidden;
}

@keyframes gradientMove{
    0%{background-position:0% 50%;}
    50%{background-position:100% 50%;}
    100%{background-position:0% 50%;}
}

.page{
    backdrop-filter:blur(25px);
    background:rgba(255,255,255,0.25);
    padding:40px;
    border-radius:25px;
    width:90%;
    max-width:420px;
    text-align:center;
    box-shadow:0 20px 40px rgba(0,0,0,0.25);
    display:none;
    animation:fadeIn 1.2s ease forwards;
}

.active{display:block;}

h1{
    font-family:'Playfair Display',serif;
    font-size:26px;
    margin-bottom:15px;
    color:#fff;
}

p{color:#fff;opacity:0.95;margin-bottom:12px;}

input{
    padding:12px;
    width:80%;
    border:none;
    border-radius:12px;
    text-align:center;
    outline:none;
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
}

button:hover{transform:scale(1.05);}

#errorMsg{margin-top:10px;color:#ff4d6d;}

@keyframes fadeIn{
    from{opacity:0;transform:translateY(20px);}
    to{opacity:1;transform:translateY(0);}
}
</style>
</head>

<body>

<!-- PAGE 1 -->
<div class="page active" id="page1">
    <h1>Before we begin...</h1>
    <p>Tell me your name.</p>
    <input type="text" id="nameInput" placeholder="Type your name" autofocus>
    <br>
    <button onclick="unlockPage1()">Unlock</button>
    <p id="errorMsg"></p>
</div>

<!-- PAGE 2 -->
<div class="page" id="page2">
    <h1>Catch Me If You Can</h1>

    <p>
        Some words are not written to be read immediately.
    </p>

    <p>
        Some feelings hide between letters.
    </p>

    <p>
        And sometimes… you have to decode the heart.
    </p>

    <!-- You will replace this with your ROT13 message later -->
    <p style="margin-top:15px; font-style:italic;">
        Gurer vf n frperg zrffntr urer...
    </p>

    <button onclick="goToPage3()">Decode Me</button>
</div>

<!-- PAGE 3 -->
<div class="page" id="page3">
    <h1>Final Key</h1>
    <p>Enter the decoded message.</p>
    <input type="text" id="codeInput" placeholder="Type the decoded text">
    <br>
    <button onclick="unlockPage3()">Reveal</button>
    <p id="finalError" style="color:#ff4d6d;"></p>
</div>

<!-- FINAL MESSAGE -->
<div class="page" id="finalPage">
    <h1>The Beginning</h1>
    <p id="finalMessage"></p>
    <p style="margin-top:15px;">– U ❤</p>
</div>

<script>

// PAGE 1 LOGIC
function unlockPage1(){
    const name=document.getElementById("nameInput").value.trim().toLowerCase();
    const error=document.getElementById("errorMsg");

    if(name==="afrin"){
        switchPage("page1","page2");
    }else{
        error.innerHTML="Hmm… this story is waiting for someone specific 😉";
    }
}

// PAGE SWITCH FUNCTION
function switchPage(from,to){
    document.getElementById(from).classList.remove("active");
    document.getElementById(to).classList.add("active");
}

// PAGE 2 BUTTON
function goToPage3(){
    switchPage("page2","page3");
}

// PAGE 3 UNLOCK (ROT13 RESULT CHECK)
function unlockPage3(){
    const input=document.getElementById("codeInput").value.trim().toLowerCase();
    const error=document.getElementById("finalError");

    // Example decoded message of:
    // "Gurer vf n frperg zrffntr urer"
    // ROT13 → "There is a secret message here"

    if(input==="there is a secret message here"){
        switchPage("page3","finalPage");
        document.getElementById("finalMessage").innerHTML=
            "You found it. And maybe… you just found me too.";
    }else{
        error.innerHTML="Not quite… look closer between the letters 😉";
    }
}

</script>

</body>
</html>
