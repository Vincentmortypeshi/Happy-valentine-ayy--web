<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine for Ayy</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: url('https://source.unsplash.com/1600x900/?hearts,pink') no-repeat center center/cover;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: 'Poppins', sans-serif;
            text-align: center;
        }
        .message {
            background: rgba(255, 182, 193, 0.95);
            padding: 30px 50px;
            border-radius: 20px;
            box-shadow: 0 0 15px rgba(255, 0, 76, 0.3);
            font-size: 2.5rem;
            color: #ff007f;
            font-weight: bold;
            animation: glow 1.5s infinite alternate;
        }
        @keyframes glow {
            0% { box-shadow: 0 0 15px rgba(255, 0, 76, 0.3); }
            100% { box-shadow: 0 0 25px rgba(255, 0, 76, 0.6); }
        }
        .hearts {
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }
        .heart {
            position: absolute;
            bottom: 0;
            width: 20px;
            height: 20px;
            background: red;
            clip-path: polygon(50% 0%, 100% 35%, 80% 100%, 50% 80%, 20% 100%, 0% 35%);
            animation: floatUp 4s linear infinite;
        }
        @keyframes floatUp {
            0% { transform: translateY(0) scale(1); opacity: 1; }
            100% { transform: translateY(-100vh) scale(1.5); opacity: 0; }
        }
    </style>
</head>
<body>
    <div class="hearts"></div>
    <div class="message">Happy Valentine's Day, Ayy! 💖<br>
    Kalau cinta itu ujian, maka bersamamu adalah jawaban yang selalu benar.💖<br>
    Kamu adalah cahaya dalam hariku dan cinta dalam hidupku. 💕</div>
    <script>
        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 3 + 2) + 's';
            document.querySelector('.hearts').appendChild(heart);
            setTimeout(() => heart.remove(), 4000);
        }
        setInterval(createHeart, 300);
    </script>
</body>
</html>
