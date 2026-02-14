
<!DOCTYPE html>
<html>
<head>
<title>For My Hinzz 🤎</title>
<style>
body {
    margin: 0;
    font-family: Arial, sans-serif;
    text-align: center;
    background: linear-gradient(to bottom, #5c3a21, #a67b5b);
    color: white;
    overflow-x: hidden;
}

.container {
    padding: 40px 20px;
}

h1 { font-size: 36px; }

p {
    font-size: 18px;
    max-width: 600px;
    margin: auto;
    line-height: 1.6;
}

button {
    margin-top: 20px;
    padding: 12px 25px;
    font-size: 16px;
    border: none;
    border-radius: 25px;
    background-color: #3e2723;
    color: white;
    cursor: pointer;
}

button:hover { background-color: #2e1b15; }

img {
    width: 150px;
    border-radius: 15px;
    margin: 10px;
    box-shadow: 0 0 10px rgba(0,0,0,0.5);
}

video {
    width: 300px;
    margin-top: 20px;
    border-radius: 15px;
    box-shadow: 0 0 15px rgba(0,0,0,0.5);
}

#countdown {
    font-size: 20px;
    margin-top: 15px;
}

.heart {
    position: fixed;
    font-size: 22px;
    animation: floatUp 6s linear infinite;
}

@keyframes floatUp {
    0% { transform: translateY(100vh); opacity: 1; }
    100% { transform: translateY(-10vh); opacity: 0; }
}
</style>
</head>

<body>

<!-- Background Music -->
<iframe id="music" width="0" height="0"
src=""
frameborder="0"
allow="autoplay">
</iframe>

<div class="container">

<h1>For My Beautiful Hinzz 🤎</h1>

<!-- Replace these with DIRECT image links -->
<div>
  <img src="YOUR_IMAGE_LINK_1.jpg">
  <img src="YOUR_IMAGE_LINK_2.jpg">
  <img src="YOUR_IMAGE_LINK_3.jpg">
</div>

<!-- Upload video to same folder & use filename -->
<video controls>
  <source src="video.mp4" type="video/mp4">
</video>

<p>
From the day you came into my life, everything became beautiful.  
Your smile is my peace, your voice is my favorite song.  
I don’t need the whole world… I just need you Hinzz 🤎
</p>

<div id="countdown"></div>

<button onclick="startMusic()">Tap for Surprise 🎵</button><br>
<button onclick="proposal()">Will You Be Mine Forever? 💍</button>

</div>

<script>

// Start Maruvaarthai song
function startMusic() {
    document.getElementById("music").src =
    "https://www.youtube.com/embed/8Z3k8yXgR4M?autoplay=1&loop=1&playlist=8Z3k8yXgR4M";
}

// Proposal animation
function proposal() {
    document.body.style.background =
    "linear-gradient(to bottom, #3e1f13, #8b5e3c)";
    
    document.querySelector(".container").innerHTML = `
        <h1 style="font-size:40px;">Hinzz Said YES 🤎💍</h1>
        <p style="font-size:20px;">
        You are my today and all of my tomorrows.  
        Forever starts now with you 🤎✨
        </p>
    `;

    startHearts();
}

// Floating hearts
function startHearts() {
    setInterval(() => {
        let heart = document.createElement("div");
        heart.className = "heart";
        heart.innerHTML = "🤎";
        heart.style.left = Math.random() * 100 + "vw";
        document.body.appendChild(heart);
        setTimeout(() => { heart.remove(); }, 6000);
    }, 300);
}

// Countdown
var countDownDate = new Date("Feb 14, 2026 00:00:00").getTime();

var x = setInterval(function() {
    var now = new Date().getTime();
    var distance = countDownDate - now;

    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = Math.floor((distance / (1000 * 60 * 60)) % 24);
    var minutes = Math.floor((distance / 1000 / 60) % 60);
    var seconds = Math.floor((distance / 1000) % 60);

    document.getElementById("countdown").innerHTML =
    "Valentine’s Day Countdown: " +
    days + "d " + hours + "h " +
    minutes + "m " + seconds + "s ";

    if (distance < 0) {
        clearInterval(x);
        document.getElementById("countdown").innerHTML =
        "Happy Valentine’s Day My Hinzz 🤎";
    }
}, 1000);

</script>

</body>
</html>
