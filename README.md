<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>For My Love ❤️</title>

<style>
body {
    margin: 0;
    overflow: hidden;
    background: linear-gradient(to bottom, #ff9a9e, #fad0c4);
    font-family: Arial, sans-serif;
    text-align: center;
    color: white;
}

h1 {
    margin-top: 100px;
    font-size: 50px;
}

button {
    padding: 15px 30px;
    font-size: 18px;
    border-radius: 30px;
    border: none;
    cursor: pointer;
    margin: 10px;
    transition: 0.3s;
}

#yes {
    background-color: white;
    color: #ff4b8b;
}

#no {
    background-color: #ff4b8b;
    color: white;
    position: absolute;
}

.heart {
    position: fixed;
    top: -10px;
    font-size: 20px;
    animation: fall linear forwards;
}

@keyframes fall {
    to {
        transform: translateY(100vh);
    }
}
</style>
</head>

<body>

<h1>Do You Love Me? 💖</h1>

<button id="yes" onclick="love()">YES 😍</button>
<button id="no" onmouseover="moveButton()">NO 😜</button>

<script>
function love() {
    document.body.innerHTML = `
        <h1 style="margin-top:200px;">I LOVE YOU 💘</h1>
        <h2>You are my favorite human ever ✨</h2>
    `;
}

function moveButton() {
    let button = document.getElementById("no");
    let x = Math.random() * window.innerWidth;
    let y = Math.random() * window.innerHeight;
    button.style.left = x + "px";
    button.style.top = y + "px";
}

function createHeart() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = Math.random() * 3 + 2 + "s";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 5000);
}

setInterval(createHeart, 300);
</script>

</body>
</html>
