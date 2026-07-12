<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday Suhi</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
height:100vh;
display:flex;
justify-content:center;
align-items:center;
background:linear-gradient(135deg,#ff9ecf,#ffd6e8,#fff5fa);
overflow:hidden;
}

.container{
text-align:center;
}

.gift{
font-size:120px;
cursor:pointer;
animation:bounce 1.5s infinite;
}

h2{
margin-top:20px;
color:#ff1493;
}

@keyframes bounce{
0%,100%{transform:translateY(0);}
50%{transform:translateY(-20px);}
}

#card{
display:none;
background:white;
padding:25px;
border-radius:20px;
box-shadow:0 0 20px rgba(0,0,0,.2);
width:340px;
}

button{
padding:12px 22px;
border:none;
border-radius:30px;
background:#ff1493;
color:white;
font-size:18px;
margin-top:20px;
cursor:pointer;
}
</style>
</head>

<body>

<div class="container">

<div id="gift" class="gift" onclick="openGift()">
🎁
</div>

<h2 id="text">Tap the Gift 🎁</h2>

<div id="card">

<h1>🎂 Happy Birthday 🎂</h1>

<h2>💖 Suhi 💖</h2>

<p style="margin-top:20px">
Today is all about you! 🥳
</p>

<button onclick="nextPage()">
Open Surprise ❤️
</button>

</div>

</div>

<script>

function openGift(){

document.getElementById("gift").style.display="none";
document.getElementById("text").style.display="none";
document.getElementById("card").style.display="block";

}

function nextPage(){

alert("Part 2 এ আসল Surprise শুরু হবে! 💖");

}

</script>

</body>
</html>
function nextPage(){

document.getElementById("card").innerHTML=`

<h1 style="color:#ff1493;">💖 A Special Message 💖</h1>

<p style="font-size:20px;line-height:1.8;margin-top:20px;">

🎉 Happy Birthday, <b>Suhi</b>! 🎉

<br><br>

May Allah bless you with endless happiness, good health, success and lots of beautiful memories. 🤲💕

<br><br>

Thank you for being my closest friend.

You always make life brighter with your kindness and smile. 🌸

<br><br>

May every dream of yours come true.

Keep smiling forever. 🥰

</p>

<button onclick="showFinal()">

One More Surprise 🎁

</button>

`;

startHearts();

}

function startHearts(){

setInterval(()=>{

let heart=document.createElement("div");

heart.innerHTML="💖";

heart.style.position="fixed";

heart.style.left=Math.random()*window.innerWidth+"px";

heart.style.top=window.innerHeight+"px";

heart.style.fontSize=(20+Math.random()*30)+"px";

heart.style.transition="6s linear";

document.body.appendChild(heart);

setTimeout(()=>{

heart.style.top="-100px";

heart.style.opacity="0";

},50);

setTimeout(()=>{

heart.remove();

},6000);

},300);

}

function showFinal(){

alert("🥳 Final Surprise আসছে... (Part 3)");

function showFinal(){

document.getElementById("card").innerHTML=`

<h1 style="color:#ff1493;">🎂 Happy Birthday Suhi 🎂</h1>

<div style="font-size:70px;margin:15px 0;">🎂🎈🎁</div>

<p style="font-size:20px;line-height:1.8;color:#d63384;">

💖 Dear Suhi, 💖

<br><br>

Thank you for always being such a wonderful friend.

I feel lucky to have a friend like you.

May Allah fill your life with happiness, peace, success and lots of smiles. 🤲🌸

<br><br>

Never stop dreaming.

Never stop smiling.

Stay exactly the amazing person you are.

<br><br>

✨ Happy Birthday Once Again! ✨

</p>

<h2 style="margin-top:20px;color:#ff1493;">
From Your Close Friend ❤️
</h2>

`;

startConfetti();

}

function startConfetti(){

const emoji=["🎊","🎉","💖","✨","🌸","🎈"];

setInterval(()=>{

let e=document.createElement("div");

e.innerHTML=emoji[Math.floor(Math.random()*emoji.length)];

e.style.position="fixed";

e.style.left=Math.random()*window.innerWidth+"px";

e.style.top="-50px";

e.style.fontSize=(20+Math.random()*25)+"px";

e.style.transition="6s linear";

document.body.appendChild(e);

setTimeout(()=>{

e.style.top=window.innerHeight+"px";

},50);

setTimeout(()=>{

e.remove();

},6000);

},180);

}
