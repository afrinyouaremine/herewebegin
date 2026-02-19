<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mission 2</title>

<style>
:root{
    --primary:#ff2e63;
    --dark:#0f0f0f;
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
    background: radial-gradient(circle at top, #2a0005, #000000 70%);
    font-family:'Segoe UI', sans-serif;
    text-align:center;
    padding:25px;
    color:var(--soft);
}

/* Elegant Card */
.container{
    max-width:500px;
    width:100%;
    padding:40px 30px;
    border-radius:20px;
    background: rgba(255,255,255,0.05);
    backdrop-filter: blur(18px);
    border:1px solid rgba(255,255,255,0.08);
    box-shadow:0 0 40px rgba(255,46,99,0.25);
    animation: fadeIn 1.5s ease forwards;
}

/* Main Text */
.main-text{
    font-size:1.5rem;
    line-height:1.8;
    font-weight:500;
    letter-spacing:0.5px;
}

/* Highlight Urdu Line */
.urdu{
    display:block;
    margin-top:20px;
    font-size:1.6rem;
    font-weight:600;
    background: linear-gradient(90deg, #ff2e63, #ff8a00);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

/* Smooth Fade */
@keyframes fadeIn{
    from{opacity:0; transform:translateY(25px);}
    to{opacity:1; transform:translateY(0);}
}

/* Mobile Optimization */
@media (max-width:480px){
    .main-text{ font-size:1.3rem; }
    .urdu{ font-size:1.4rem; }
}
</style>
</head>

<body>

<div class="container">
    <div class="main-text">
        Don’t rush yourself… calm down. Take your time.
        <span class="urdu">
            Main kahaan jaaunga tumhe chhod ke…?
        </span>
    </div>
</div>

</body>
</html>