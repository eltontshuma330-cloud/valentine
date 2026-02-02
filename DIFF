<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Question for Elsie ❤️</title>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Nunito:wght@400;700&display=swap');

    body {
        margin: 0;
        padding: 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 99%, #fecfef 100%);
        font-family: 'Nunito', sans-serif;
        overflow: hidden; /* Prevents scrollbars during the game */
    }

    /* Screen 1: The Proposal */
    #proposal-screen {
        text-align: center;
        z-index: 10;
        padding: 20px;
    }

    h1 {
        color: #d63384;
        font-family: 'Dancing Script', cursive;
        font-size: 3.5rem;
        margin-bottom: 30px;
        text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
    }

    .btn-container {
        position: relative;
        height: 100px; /* Space for buttons */
        display: flex;
        justify-content: center;
        gap: 20px;
    }

    button {
        font-size: 1.2rem;
        padding: 12px 30px;
        border: none;
        border-radius: 50px;
        cursor: pointer;
        font-weight: bold;
        transition: transform 0.2s;
        box-shadow: 0 4px 15px rgba(0,0,0,0.2);
    }

    #yesBtn {
        background-color: #ff4757;
        color: white;
    }

    #yesBtn:hover {
        transform: scale(1.1);
        background-color: #ff6b81;
    }

    #noBtn {
        background-color: white;
        color: #ff4757;
        position: absolute; /* Allows it to move freely */
    }

    /* Screen 2: The Letter */
    #letter-screen {
        display: none;
        position: relative;
        width: 100%;
        height: 100vh;
        justify-content: center;
        align-items: center;
        padding: 20px;
        box-sizing: border-box;
        overflow-y: auto; /* Allow scrolling if letter is long */
    }

    .paper {
        background-color: #fff;
        width: 100%;
        max-width: 500px;
        padding: 40px;
        border-radius: 10px;
        box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        position: relative;
        animation: fadeInUp 1s ease forwards;
        text-align: left;
        line-height: 1.6;
        color: #444;
        margin: auto;
    }

    .paper h2 {
        font-family: 'Dancing Script', cursive;
        color: #d63384;
        font-size: 2.5rem;
        margin-top: 0;
        text-align: center;
    }

    .signature {
        font-family: 'Dancing Script', cursive;
        font-size: 1.8rem;
        margin-top: 30px;
        text-align: right;
        color: #d63384;
    }

    /* Animations */
    @keyframes fadeInUp {
        from { opacity: 0; transform: translateY(20px); }
        to { opacity: 1; transform: translateY(0); }
    }

    /* Confetti */
    .confetti {
        position: absolute;
        width: 10px;
        height: 10px;
        background-color: #f00;
        animation: fall linear forwards;
    }

    @keyframes fall {
        to { transform: translateY(100vh) rotate(720deg); }
    }
</style>
</head>
<body>

    <div id="proposal-screen">
        <h1>Elsie, will you be my Valentine? 🌹</h1>
        <div class="btn-container">
            <button id="yesBtn" onclick="sheSaidYes()">YES!</button>
            <button id="noBtn" onmouseover="moveButton()" onclick="moveButton()">No</button>
        </div>
    </div>

    <div id="letter-screen">
        <div class="paper">
            <h2>You said YES! ❤️</h2>
            <p><strong>My Dearest Elsie,</strong></p>
            
            <p>I’ve been thinking a lot lately about how lucky I am. People always talk about the "firsts" in a relationship, but I’ve been really looking forward to this particular first: our first Valentine’s Day together.</p>

            <p>I know today is just a date on a calendar, but getting to spend it with you makes it feel genuinely significant to me. You have brought so much light, laughter, and warmth into my life. Even the quiet moments with you feel better than the most exciting moments with anyone else.</p>

            <p>I want to celebrate you—not just today, but every day. I want to be the reason you smile when you check your phone, and the person who supports you when things get heavy.</p>

            <p>Thank you for making me the happiest man alive.</p>

            <div class="signature">
                With all my love,<br>
                Elton Tshuma
            </div>
        </div>
    </div>

    <script>
        // Make the "No" button run away
        function moveButton() {
            const btn = document.getElementById('noBtn');
            const container = document.getElementById('proposal-screen');
            
            // Get window dimensions
            const maxWidth = window.innerWidth - 100; // Buffer for button width
            const maxHeight = window.innerHeight - 50; // Buffer for button height

            // Calculate random position
            const newX = Math.random() * (maxWidth - 20) + 10;
            const newY = Math.random() * (maxHeight - 20) + 10;

            // Apply new position fixed to screen
            btn.style.position = 'fixed';
            btn.style.left = newX + 'px';
            btn.style.top = newY + 'px';
        }

        // Transition to the letter
        function sheSaidYes() {
            document.getElementById('proposal-screen').style.display = 'none';
            const letterScreen = document.getElementById('letter-screen');
            letterScreen.style.display = 'flex';
            document.body.style.overflow = 'auto'; // Allow scrolling for the letter
            
            createConfetti();
        }

        // Simple Confetti Effect
        function createConfetti() {
            const colors = ['#ff4757', '#2ed573', '#1e90ff', '#ffa502', '#d63384'];
            for (let i = 0; i < 50; i++) {
                const confetti = document.createElement('div');
                confetti.classList.add('confetti');
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.animationDuration = (Math.random() * 2 + 3) + 's';
                document.body.appendChild(confetti);
            }
        }
    </script>
</body>
</html>
