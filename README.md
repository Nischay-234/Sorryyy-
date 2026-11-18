
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sorry Vedu ❤️</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg,#ffb6c1,#ff69b4);
  font-family: Arial, sans-serif;
  padding: 20px;
  overflow-x: hidden;
}

.card {
  background: white;
  padding: 30px 22px;
  border-radius: 25px;
  text-align: center;
  max-width: 400px;
  width: 100%;
  box-shadow: 0 10px 35px #0003;
  z-index: 2;
}

h1 {
  color: #ff1493;
}

h2 {
  color: #ff1493;
  font-size: 21px;
}

p {
  color: #555;
  line-height: 1.7;
}

.heart {
  font-size: 55px;
}

button {
  display: block;
  width: 100%;
  border: none;
  padding: 14px;
  margin: 12px 0;
  border-radius: 25px;
  background: #ff69b4;
  color: white;
  font-size: 16px;
  cursor: pointer;
  transition: 0.2s;
}

button:hover {
  background: #ff1493;
  transform: scale(1.03);
}

#final {
  display: none;
  color: #ff1493;
  font-weight: bold;
}

#quiz {
  display: none;
}

.floating {
  position: fixed;
  bottom: -30px;
  animation: float 7s linear forwards;
  pointer-events: none;
}

@keyframes float {
  to {
    transform: translateY(-110vh) rotate(360deg);
    opacity: 0;
  }
}
</style>
</head>

<body>

<div class="card">

<div class="heart">❤️🥺❤️</div>

<div id="intro">
<h1>Vedu Please Forgive Me 💗</h1>

<p>
My sweetest Vedu ❤️<br><br>

Mujhe maaf kar do please 🥺<br>
Mujhse galti ho gayi. Time par message
nahi kiya, I am really sorry.<br><br>

Mera intention tumhe hurt karna nahi tha.
Tum mere liye bahut special ho.<br><br>

Please ek chhoti si quiz khelo ❤️
</p>

<button onclick="startQuiz()">Start Quiz 💌</button>
</div>

<div id="quiz">
<h2 id="question"></h2>
<div id="options"></div>
<p id="feedback"></p>
</div>

<div id="final">
<div class="heart">💗💗💗</div>

<h1>Thank You Vedu! 🥹</h1>

<p>
Mujhe maaf kar diya na? ❤️<br><br>

Ab mujhse naraz nahi ho na? 🥺<br>
Please ab maan jao na!<br><br>

Abse time par message karunga.<br>
Tumhe kabhi aisa feel nahi hone dunga.<br><br>

I AM REALLY SORRY VEDU ❤️<br>
I LOVE YOU SO MUCH! 💕<br><br>

Forever yours,<br>
<b>Nischay ❤️</b>
</p>
</div>

</div>

<script>

const questions = [

{
q: "Q1. Vedu, mujhe maaf kar dogi? 🥺",
a: [
"Haan maaf kiya ❤️",
"Thoda aur sorry bolo 😜",
"Abhi sochungi 🥺"
]
},

{
q: "Q2. Ab mujhse naraz nahi ho na? 💗",
a: [
"Nahi, ab naraz nahi hoon ❤️",
"Thodi si naraz hoon 😒",
"Ek hug chahiye 🫂"
]
},

{
q: "Q3. Please maan jao na? 🥹",
a: [
"Achha baba maan gayi ❤️",
"Abse time par message karna!",
"Bahut saara pyaar chahiye 💕"
]
},

{
q: "Q4. Last question! Mujhse pyaar karti ho na? ❤️",
a: [
"Bahut saara pyaar ❤️",
"Of course! 🥹",
"Always and forever 💗"
]
}

];

let current = 0;

function startQuiz() {
document.getElementById("intro").style.display = "none";
document.getElementById("quiz").style.display = "block";
showQuestion();
}

function showQuestion() {
let q = questions[current];

document.getElementById("question").innerText = q.q;

let box = document.getElementById("options");
box.innerHTML = "";

q.a.forEach(answer => {

let btn = document.createElement("button");

btn.innerText = answer;

btn.onclick = () => nextQuestion();

box.appendChild(btn);

});
}

function nextQuestion() {

current++;

if (current < questions.length) {

showQuestion();

} else {

document.getElementById("quiz").style.display = "none";

document.getElementById("final").style.display = "block";

}

}

function createHeart() {

const heart = document.createElement("div");

heart.className = "floating";

heart.innerText = "❤️";

heart.style.left = Math.random() * 100 + "vw";

heart.style.fontSize = (18 + Math.random() * 20) + "px";

heart.style.animationDuration = (4 + Math.random() * 4) + "s";

document.body.appendChild(heart);

setTimeout(() => heart.remove(), 8000);

}

setInterval(createHeart, 500);

</script>

</body>
</html>
