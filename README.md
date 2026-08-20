# For-my-BABY
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday My Love! ❤️</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', cursive, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 99%, #feada6 100%);
            color: #4a4a4a;
            min-height: 100vh;
            overflow-x: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        /* Floating Hearts Background */
        .heart-bg {
            position: fixed;
            top: -10vh;
            font-size: 1.5rem;
            animation: fall linear infinite;
            z-index: 1;
            opacity: 0.7;
        }

        @keyframes fall {
            to {
                transform: translateY(110vh) rotate(360deg);
            }
        }

        /* Container Alignment */
        .container {
            width: 90%;
            max-width: 800px;
            margin: 40px auto;
            text-align: center;
            z-index: 2;
        }

        /* Hero Header */
        h1 {
            font-size: 2.8rem;
            color: #d63384;
            text-shadow: 2px 2px 8px rgba(255, 255, 255, 0.8);
            margin-bottom: 10px;
            animation: pulse 2s infinite ease-in-out;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.03); }
        }

        .subtitle {
            font-size: 1.2rem;
            color: #6c757d;
            margin-bottom: 30px;
        }

        /* Photo Gallery Frame */
        .photo-card {
            background: #ffffff;
            padding: 15px;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(214, 51, 132, 0.2);
            margin: 25px auto;
            max-width: 450px;
            transform: rotate(-2deg);
            transition: all 0.3s ease;
        }

        .photo-card:hover {
            transform: rotate(0deg) scale(1.02);
        }

        .photo-card img {
            width: 100%;
            height: 350px;
            object-fit: cover;
            border-radius: 15px;
        }

        .photo-caption {
            margin-top: 12px;
            font-weight: 600;
            color: #d63384;
            font-size: 1.1rem;
        }

        /* Relationship Timer Box */
        .timer-box {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(5px);
            border-radius: 15px;
            padding: 20px;
            margin: 30px 0;
            box-shadow: 0 4px 15px rgba(0,0,0,0.05);
        }

        .timer-box h2 {
            color: #c2185b;
            font-size: 1.4rem;
            margin-bottom: 15px;
        }

        .timer-display {
            display: flex;
            justify-content: center;
            gap: 15px;
        }

        .time-segment {
            background: #ffe6e8;
            padding: 10px 15px;
            border-radius: 10px;
            min-width: 70px;
        }

        .time-number {
            font-size: 1.5rem;
            font-weight: bold;
            color: #d63384;
        }

        .time-label {
            font-size: 0.75rem;
            color: #757575;
            text-transform: uppercase;
        }

        /* Interactive Surprise Note */
        .interactive-section {
            margin: 40px 0;
        }

        .btn-surprise {
            background: linear-gradient(45deg, #ff4081, #d63384);
            color: #fff;
            border: none;
            padding: 15px 35px;
            font-size: 1.1rem;
            border-radius: 30px;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(214, 51, 132, 0.4);
            transition: transform 0.2s;
        }

        .btn-surprise:hover {
            transform: translateY(-3deg);
        }

        .letter {
            display: none;
            background: #fff9fa;
            border: 2px dashed #ff80ab;
            border-radius: 15px;
            padding: 25px;
            margin-top: 25px;
            text-align: left;
            line-height: 1.8;
            color: #444;
            animation: fadeIn 1s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Happy Birthday, My Love! 🎂✨</h1>
        <p class="subtitle">To the most special person in my world</p>

        <!-- Main Photo Frame -->
        <div class="photo-card">
            <!-- Replace 'photo.jpg' with your image file path -->
            <img src="pic.jpg" alt="Our Special Moment" id="mainPhoto">
            <div class="photo-caption">Making every moment magical with you ❤️</div>
        </div>

        <!-- Relationship Counter -->
        <div class="timer-box">
            <h2>Counting Every Precious Moment Together</h2>
            <div class="timer-display">
                <div class="time-segment">
                    <div class="time-number" id="days">00</div>
                    <div class="time-label">Days</div>
                </div>
                <div class="time-segment">
                    <div class="time-number" id="hours">00</div>
                    <div class="time-label">Hours</div>
                </div>
                <div class="time-segment">
                    <div class="time-number" id="minutes">00</div>
                    <div class="time-label">Mins</div>
                </div>
                <div class="time-segment">
                    <div class="time-number" id="seconds">00</div>
                    <div class="time-label">Secs</div>
                </div>
            </div>
        </div>

        <!-- Hidden Love Letter Section -->
        <div class="interactive-section">
            <button class="btn-surprise" onclick="toggleLetter()">Click for Your Birthday Message 💌</button>
            <div class="Happy birthday! A very dear person living in the nerve cells of the brain." id="loveLetter">
                <p>My Dearest,</p><br>
                <p>Happy Birthday! Having you in my life brings so much warmth, laughter, and happiness every single day. Thank you for being your incredible self and for making every memory so unforgettable.</p><br>
                <p>May your special day be filled with as much joy and beauty as you bring into my life. Here's to celebrating you today and creating many more wonderful moments together.</p><br>
                <p>Forever & Always,<br><strong>Yours ❤️</strong></p>
            </div>
        </div>
    </div>

    <script>
        // 1. Floating Hearts Animation
        function createHearts() {
            const symbols = ['❤️', '💖', '✨', '🌸', '💕'];
            const heart = document.createElement('div');
            heart.classList.add('heart-bg');
            heart.innerText = symbols[Math.floor(Math.random() * symbols.length)];
            heart.style.left = Math.random() * 100 + "vw";
            heart.style.animationDuration = Math.random() * 3 + 3 + "s";
            heart.style.fontSize = Math.random() * 15 + 15 + "px";
            document.body.appendChild(heart);

            setTimeout(() => {
                heart.remove();
            }, 6000);
        }
        setInterval(createHearts, 300);

        // 2. Relationship Timer Counter
        // Set your relationship start date here (Year, Month Index [0-11], Day)
        const startDate = new Date(2021, 0, 12); 

        function updateTimer() {
            const now = new Date();
            const diff = now - startDate;

            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
            const minutes = Math.floor((diff / 1000 / 60) % 60);
            const seconds = Math.floor((diff / 1000) % 60);

            document.getElementById('days').innerText = days;
            document.getElementById('hours').innerText = hours < 10 ? '0' + hours : hours;
            document.getElementById('minutes').innerText = minutes < 10 ? '0' + minutes : minutes;
            document.getElementById('seconds').innerText = seconds < 10 ? '0' + seconds : seconds;
        }
        setInterval(updateTimer, 1000);
        updateTimer();

        // 3. Toggle Letter Display
        function toggleLetter() {
            const letter = document.getElementById('loveLetter');
            if (letter.style.display === "block") {
                letter.style.display = "none";
            } else {
                letter.style.display = "block";
            }
        }
    </script>
</body>
</html>
