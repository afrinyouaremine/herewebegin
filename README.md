<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mission 2</title>

<style>
:root{
    --primary:#ff2e63;
    --accent:#ff8a00;
    --soft:#f5f5f5;
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background: radial-gradient(circle at top, #2a0005, #000000 75%);
    font-family:'Segoe UI', sans-serif;
    padding:20px;
    color:var(--soft);
}

.container{
    width:100%;
    max-width:520px;
    padding:35px 25px;
    border-radius:20px;
    background: rgba(255,255,255,0.05);
    backdrop-filter: blur(18px);
    border:1px solid rgba(255,255,255,0.08);
    box-shadow:0 0 40px rgba(255,46,99,0.25);
    animation: fadeIn 1.2s ease forwards;
}

/* Romantic Text */
.main-text{
    font-size:1.4rem;
    line-height:1.8;
    text-align:center;
}

.urdu{
    display:block;
    margin-top:15px;
    font-size:1.6rem;
    font-weight:600;
    background: linear-gradient(90deg, var(--primary), var(--accent));
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

/* Divider */
.divider{
    height:1px;
    background: rgba(255,255,255,0.1);
    margin:25px 0;
}

/* Input Section */
h2{
    font-size:1rem;
    font-weight:500;
    margin-bottom:12px;
    text-align:center;
    color:#ccc;
}

textarea{
    width:100%;
    min-height:90px;
    padding:12px;
    border-radius:12px;
    border:1px solid rgba(255,255,255,0.1);
    background: rgba(255,255,255,0.08);
    color:white;
    resize:none;
    font-size:0.95rem;
    outline:none;
    margin-bottom:12px;
}

.buttons{
    display:flex;
    gap:10px;
}

button{
    flex:1;
    padding:10px;
    border-radius:30px;
    border:none;
    cursor:pointer;
    font-weight:600;
    transition:0.3s ease;
}

.save{
    background: linear-gradient(90deg, var(--primary), var(--accent));
    color:white;
}

.edit{
    background:#222;
    color:white;
}

button:hover{
    transform:scale(1.05);
}

.saved-box{
    margin-top:15px;
    padding:12px;
    border-radius:12px;
    background: rgba(255,255,255,0.07);
    border:1px solid rgba(255,255,255,0.1);
    min-height:50px;
    font-size:0.9rem;
    color:#ddd;
    white-space:pre-wrap;
}

/* Animation */
@keyframes fadeIn{
    from{opacity:0; transform:translateY(20px);}
    to{opacity:1; transform:translateY(0);}
}

@media(max-width:480px){
    .main-text{font-size:1.2rem;}
    .urdu{font-size:1.3rem;}
}
</style>
</head>

<body>

<div class="container">

    <div class="main-text">
        Don’t rush yourself… calm down. Take your time.
        <span class="urdu">
            Main kahaan jaane wala hu tumhe chhod ke…
 yahi hu tere inthzaar main..
        </span>
    </div>

    <div class="divider"></div>

    <h2>If you want to say or ask something, you can type it here...</h2>

    <textarea id="messageInput" placeholder="Type your message..."></textarea>

    <div class="buttons">
        <button class="save" onclick="saveMessage()">Save</button>
        <button class="edit" onclick="editMessage()">Edit</button>
    </div>

    <div class="saved-box" id="savedMessage"></div>

</div>

<script>
const input = document.getElementById("messageInput");
const savedBox = document.getElementById("savedMessage");

window.onload = function(){
    const saved = localStorage.getItem("missionMessage");
    if(saved){
        savedBox.innerText = saved;
        input.value = saved;
        input.disabled = true;
    }
};

function saveMessage(){
    const message = input.value.trim();
    if(message !== ""){
        localStorage.setItem("missionMessage", message);
        savedBox.innerText = message;
        input.disabled = true;
    }
}

function editMessage(){
    input.disabled = false;
    input.focus();
}
</script>

</body>
</html>