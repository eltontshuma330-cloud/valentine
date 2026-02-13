
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Courtney ❤️ Mandipa</title>

<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Nunito:wght@400;700&display=swap" rel="stylesheet">

<style>

body {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    font-family: 'Nunito', sans-serif;
    overflow: hidden;
}

/* Screen 1 */
#proposal-screen {
    text-align: center;
}

h1 {
    color: #4da6ff;
    font-family: 'Dancing Script', cursive;
    font-size: 3rem;
    margin-bottom: 30px;
}

.btn-container {
    position: relative;
    height: 100px;
}

button {
    font-size: 1.2rem;
    padding: 12px 30px;
    border: none;
    border-radius: 50px;
    cursor: pointer;
    font-weight: bold;
    transition: 0.2s;
    box-shadow: 0 5px 15px rgba(0,0,0,0.3);
}

#yesBtn {
    background-color: #1e90ff;
    color: white;
}

#yesBtn:hover {
    transform: scale(1.1);
    background-color: #4da6ff;
}

#noBtn {
    background-color: white;
    color: #1e90ff;
    position: absolute;
    left: 150px;
}

/* Screen 2 */
#letter-screen {
    display: none;
    width: 100%;
    height: 100vh;
    justify-content: center;
    align-items: center;
    padding: 20px;
    box-sizing: border-box;
}

.paper {
    background-color: white;
    max-width: 500px;
    padding: 40px;
    border-radius: 15px;
    box-shadow: 0 15px 40px rgba(0,0,0,0.4);
    border-left: 6px solid #1e90ff;
    animation: fadeInUp 1s ease forwards;
    line-height: 1.6;
    color: #333;
}

.paper h2 {
    font-family: 'Dancing Script', cursive;
    color: #1e90ff;
    text-align: center;
    font-size: 2.3rem;
}

.signature {
    font-family: 'Dancing Script', cursive;
    font-size: 1.8rem;
    margin-top: 30px;
    text-align: right;
    color: #1e90ff;
}

/* Animations */
@keyframes fadeInUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

/* Confetti */
.confetti {
    position: absolute;
    width: 8px;
    height: 8px;
    background-color: #1e90ff;
    animation: fall linear forwards;
}

@keyframes fall {
    to { transform: translateY(100vh) rotate(720deg); }
}

</style>
</head>

<body>

<!-- Screen 1 -->
<div id="proposal-screen">
    <h1>Mandipa 💙 Will You Open This?</h1>
    <div class="btn-container">
        <button id="yesBtn">Yes 💙</button>
        <button id="noBtn">No</button>
    </div>
</div>

<!-- Screen 2 -->
<div id="letter-screen">
    <div class="paper">
        <h2>To My Mandipa 💙</h2>

        <p>
            From the very beginning, you have been my calm in the chaos 
            and my strength when I needed it most.
        </p>

        <p>
            You have this quiet confidence, this way of loving and 
            protecting that makes me feel safe in ways I never expected.
        </p>

        <p>
            I love the way you think. I love the way you speak.
            I love the way you carry yourself like a man who knows who he is.
            And most of all, I love how you love me.
        </p>

        <p>
            No matter where life takes us, I want you to always remember 
            that you are deeply appreciated and deeply loved.
        </p>

        <div class="signature">
            Forever yours,<br>
            Courtney 💙
        </div>
    </div>
</div>

<script>

const yesBtn = document.getElementById("yesBtn");
const noBtn = document.getElementById("noBtn");
const proposalScreen = document.getElementById("proposal-screen");
const letterScreen = document.getElementById("letter-screen");

/* Make No button run away */
noBtn.addEventListener("mouseover", () => {
    const x = Math.random() * (window.innerWidth - 100);
    const y = Math.random() * (window.innerHeight - 50);
    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
});

/* Show letter */
yesBtn.addEventListener("click", () => {
    proposalScreen.style.display = "none";
    letterScreen.style.display = "flex";
    createConfetti();
});

/* Confetti effect */
function createConfetti() {
    for (let i = 0; i < 100; i++) {
        let confetti = document.createElement("div");
        confetti.classList.add("confetti");
        confetti.style.left = Math.random() * window.innerWidth + "px";
        confetti.style.animationDuration = (Math.random() * 3 + 2) + "s";
        document.body.appendChild(confetti);

        setTimeout(() => {
            confetti.remove();
        }, 5000);
    }
}

</script>

</body>
</html>
