<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Sneha ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:'Poppins',sans-serif;
}

body{
height:100vh;
overflow:hidden;
background:linear-gradient(-45deg,#ff4d6d,#ff758f,#8e44ad,#4a00e0);
background-size:400% 400%;
animation:bgMove 12s ease infinite;
display:flex;
justify-content:center;
align-items:center;
position:relative;
}

@keyframes bgMove{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

.card{
width:90%;
max-width:420px;
padding:30px;
border-radius:25px;
background:rgba(255,255,255,0.12);
backdrop-filter:blur(15px);
text-align:center;
color:white;
box-shadow:0 0 30px rgba(255,255,255,0.2);
z-index:5;
animation:floatCard 3s ease-in-out infinite;
}

@keyframes floatCard{
0%,100%{transform:translateY(0);}
50%{transform:translateY(-8px);}
}

h1{
font-size:2rem;
margin-bottom:10px;
}

.subtitle{
font-size:1rem;
opacity:0.9;
margin-bottom:25px;
}

button{
border:none;
padding:14px 28px;
border-radius:50px;
background:white;
color:#ff4d6d;
font-weight:700;
font-size:1rem;
cursor:pointer;
transition:0.3s;
}

button:hover{
transform:scale(1.08);
}

.popup{
position:fixed;
top:50%;
left:50%;
transform:translate(-50%,-50%) scale(0);
width:90%;
max-width:500px;
background:white;
padding:25px;
border-radius:25px;
box-shadow:0 0 40px rgba(0,0,0,0.3);
transition:.4s;
z-index:20;
}

.popup.show{
transform:translate(-50%,-50%) scale(1);
}

.popup h2{
color:#ff4d6d;
margin-bottom:15px;
text-align:center;
}

.popup p{
color:#444;
line-height:1.7;
font-size:0.95rem;
white-space:pre-line;
}

.close{
margin-top:20px;
width:100%;
background:#ff4d6d;
color:white;
}

.float{
position:absolute;
bottom:-50px;
animation:rise linear infinite;
pointer-events:none;
}

@keyframes rise{
0%{
transform:translateY(0) rotate(0deg);
opacity:0;
}
20%{
opacity:1;
}
100%{
transform:translateY(-120vh) rotate(360deg);
opacity:0;
}
}
</style>
</head>
<body>

<div class="card">
<h1>❤️ For Sneha ❤️</h1>
<p class="subtitle">
Happy Best Friends Day to my favorite person ✨
</p>

<button onclick="openLetter()">
Open My Letter 💌
</button>
</div>

<div class="popup" id="letter">
<h2>To Sneha ❤️</h2>

<p>
From all our random conversations to the memories we've made together,
you've become one of the most important people in my life.

You make ordinary days feel special, and I'm grateful for every laugh,
every moment, and every memory we share.

No matter what the future brings, you'll always have a special place in my heart.

Thank you for being my best friend, my favorite person,
and someone I care about so much.

I love you alott my bestie friendd 🥺❤️

— Baibhab 🫂✨
</p>

<button class="close" onclick="closeLetter()">
Close ❤️
</button>
</div>

<script>
function openLetter(){
document.getElementById("letter").classList.add("show");
}

function closeLetter(){
document.getElementById("letter").classList.remove("show");
}

const symbols=["❤️","💖","💕","💗","✨","⭐"];

for(let i=0;i<60;i++){
let item=document.createElement("div");
item.className="float";
item.innerHTML=symbols[Math.floor(Math.random()*symbols.length)];

item.style.left=Math.random()*100+"vw";
item.style.fontSize=(18+Math.random()*25)+"px";
item.style.animationDuration=(6+Math.random()*10)+"s";
item.style.animationDelay=Math.random()*5+"s";

document.body.appendChild(item);
}
</script>

</body>
</html>
