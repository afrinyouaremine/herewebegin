<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mission 2</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    background: linear-gradient(135deg, #ff1a1a, #b30000);
    font-family:'Segoe UI', Arial, sans-serif;
    text-align:center;
    padding:20px;
}

.main-text{
    color:white;
    font-size:2.2rem;
    font-weight:600;
    line-height:1.6;
    animation: fadeIn 2s ease-in-out;
}

.loading-text{
    color:black;
    font-size:1.4rem;
    margin-top:30px;
    font-weight:bold;
    letter-spacing:2px;
    animation: pulse 1.5s infinite;
}

@keyframes pulse {
    0% { opacity:1; }
    50% { opacity:0.6; }
    100% { opacity:1; }
}

@keyframes fadeIn {
    from { opacity:0; transform:translateY(20px); }
    to { opacity:1; transform:translateY(0); }
}
</style>
</head>

<body>

<div class="main-text">
    Don't rush yourself calm down... take your time.... <br>
    Me kaha jayega tume choodke..
</div>

<div class="loading-text">
    MISSION-2 LOADING... <br>
    Imotions Deploying to Production
</div>

</body>
</html>