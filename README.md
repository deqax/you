<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Happy Valentine's Day</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffe6e6;
            color: #d63384;
            overflow: hidden;
            margin: 0;
            padding: 0;
        }
        h1 {
            font-size: 2.5em;
            margin-top: 30px;
        }
        .heart {
            font-size: 4em;
            animation: heartbeat 1s infinite;
        }
        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }
        .message {
            font-size: 1.5em;
            margin: 20px;
            padding: 0 15px;
        }
        .button {
            display: inline-block;
            margin-top: 20px;
            padding: 12px 24px;
            background-color: #ff4d79;
            color: white;
            text-decoration: none;
            border-radius: 10px;
            font-size: 1.5em;
            cursor: pointer;
            border: none;
        }
        .hidden {
            display: none;
        }
        .emoji {
            position: absolute;
            font-size: 1.5em;
            animation: floatUp 2s ease-out forwards, fadeOut 2s ease-out forwards;
            opacity: 1;
        }
        @keyframes floatUp {
            from { transform: translateY(0); }
            to { transform: translateY(-100px); }
        }
        @keyframes fadeOut {
            from { opacity: 1; }
            to { opacity: 0; }
        }
        #surprise {
            padding: 20px;
        }
        #surprise img {
            width: 80%;
            max-width: 280px;
            border-radius: 10px;
        }
    </style>
    <script>
        function showSurprise() {
            document.getElementById('surprise').classList.remove('hidden');
            createEmojis();
        }
        
        function createEmojis() {
            const emojis = ['❤️', '💖', '💘', '💕', '💓', '😍'];
            for (let i = 0; i < 20; i++) {
                let emoji = document.createElement('div');
                emoji.classList.add('emoji');
                emoji.innerText = emojis[Math.floor(Math.random() * emojis.length)];
                emoji.style.left = Math.random() * 90 + 'vw';
                emoji.style.top = Math.random() * 80 + 10 + 'vh';
                emoji.style.position = 'absolute';
                emoji.style.transform = 'scale(1)';
                document.body.appendChild(emoji);
                setTimeout(() => { emoji.remove(); }, 2000);
            }
        }
    </script>
</head>
<body>
    <h1>Happy Valentine's Day ❤️</h1>
    <div class="heart">❤️</div>
    <p class="message">จดหมายสำหรับเบ้บคนน่ารัก💕</p>
    <button class="button" onclick="showSurprise()">กดตรงนี้เลยจร้</button>
    <div id="surprise" class="hidden">
        <h2>💖 I love you 💖</h2>
        <p>ขอบคุณที่เข้ามาเป็นสิ่งที่ดีให้เค้าในชีวิตนะอ้วน อยู่ด้วยกันกับเค้าไปนานๆนะ 🌹</p>
        <img src="https://i.pinimg.com/originals/dc/dd/45/dcdd45bc02f89241babe4ab61ce69f01.gif" alt="Love Image">
    </div>
</body>
</html>
