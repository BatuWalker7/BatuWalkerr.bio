# BatuWalkerr.bio[batuwalker.html](https://github.com/user-attachments/files/25561033/batuwalker.html)
<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>BatuWalker Bio</title>

<style>

/* ===== GENEL ===== */
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial, sans-serif;
}

body{
height:100vh;
overflow:hidden;
color:white;
}

/* ===== ARKA PLAN ===== */
video{
position:fixed;
width:100%;
height:100%;
object-fit:cover;
z-index:-2;
}

.overlay{
position:fixed;
width:100%;
height:100%;
background:rgba(0,0,0,0.65);
z-index:-1;
}

/* ===== İÇERİK ===== */
.container{
position:absolute;
top:50%;
left:50%;
transform:translate(-50%,-50%);
text-align:center;
}

/* ===== PROFİL ===== */
.profile{
width:160px;
height:160px;
border-radius:50%;
border:4px solid white;
object-fit:cover;
transition:0.3s;
}

.profile:hover{
transform:scale(1.1);
box-shadow:0 0 20px white;
}

/* ===== BAŞLIK ===== */
h1{
margin-top:15px;
font-size:40px;
letter-spacing:2px;
}

/* ===== ALT YAZI ===== */
p{
margin-top:10px;
color:#ccc;
}

/* ===== BUTON ===== */
.btn{
display:block;
width:240px;
margin:15px auto;
padding:12px;
border-radius:30px;
background:white;
color:black;
text-decoration:none;
font-weight:bold;
transition:0.3s;
}

.btn:hover{
background:black;
color:white;
box-shadow:0 0 20px white;
}

/* ===== SAYAC ===== */
.counter{
margin-top:15px;
font-size:20px;
color:#00ffcc;
}

/* ===== SES BUTONU ===== */
.soundBtn{
position:fixed;
bottom:20px;
right:20px;
padding:12px 18px;
background:white;
color:black;
border-radius:20px;
cursor:pointer;
font-weight:bold;
z-index:999;
}

</style>
</head>
<body>

<!-- 🔥 ARKA PLAN -->
<video id="bgVideo" autoplay loop muted>
<source src="supra.mp4" type="video/mp4">
</video>

<div class="overlay"></div>

<!-- 🔥 İÇERİK -->
<div class="container">

<img src="walker.jpeg" class="profile">

<h1>BatuWalker</h1>

<p>Risk almadan kazanılmaz.</p>

<a class="btn" href="https://instagram.com/batuz067_" target="_blank">
Instagram
</a>

<a class="btn" href="https://www.tiktok.com/@baturraenee" target="_blank">
TikTok
</a>

<!-- 👀 ZİYARETÇİ -->
<div class="counter">
👀 Ziyaretçi: <span id="visitorCount">0</span>
</div>

</div>

<!-- 🔊 SES -->
<div class="soundBtn" onclick="toggleSound()">
🔊 Ses Aç
</div>

<script>

/* ===== ZİYARETÇİ SAYACI ===== */
let visits = localStorage.getItem("visits");

if(!visits){
visits = 0;
}

visits++;
localStorage.setItem("visits", visits);

document.getElementById("visitorCount").innerText = visits;


/* ===== SES KONTROL ===== */
let video = document.getElementById("bgVideo");
let btn = document.querySelector(".soundBtn");

video.muted = true;

function toggleSound(){
if(video.muted){
video.muted = false;
btn.innerHTML = "🔇 Ses Kapat";
}else{
video.muted = true;
btn.innerHTML = "🔊 Ses Aç";
}
}

</script>

</body>
</html>
