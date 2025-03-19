<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>You Have Been Pwned</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: black;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            overflow: hidden;
            font-family: Arial, sans-serif;
        }

        h1 {
            color: red;
            font-size: 50px;
            font-weight: bold;
            text-shadow: 0 0 20px red;
            text-align: center;
            margin-top: 20px;
        }

        #hacker-name {
            color: white;
            text-shadow: 0 0 20px white;
        }

        .discord-link {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: #7289DA;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
            animation: pulse 2s infinite;
            box-shadow: 0 0 10px rgba(114, 137, 218, 0.5);
        }

        @keyframes pulse {
            0% {
                transform: translateX(-50%) scale(1);
                box-shadow: 0 0 10px rgba(114, 137, 218, 0.5);
            }
            50% {
                transform: translateX(-50%) scale(1.05);
                box-shadow: 0 0 20px rgba(114, 137, 218, 0.8);
            }
            100% {
                transform: translateX(-50%) scale(1);
                box-shadow: 0 0 10px rgba(114, 137, 218, 0.5);
            }
        }

        /* خلفية متحركة */
        .background-gif {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }

        .background-gif img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    </style>
</head>
<body>

    <div class="background-gif">
        <img src="https://i.top4top.io/p_3365rfndr1.gif" alt="Background GIF">
    </div>

    <h1>
        YOU HAVE BEEN PWNED BY <span id="hacker-name">[جهيمان]</span>
    </h1>

    <a href="https://discord.gg/zbnh" class="discord-link" target="_blank">dis zbnh</a>

    <script>
        // قائمة الأسماء اللي بتظهر بالتناوب
        const hackerNames = ["جهيمان", "بلا حدود", "M2", "FA7", "B2"];
        let currentIndex = 0;

        function changeHackerName() {
            const nameElement = document.getElementById("hacker-name");
            nameElement.textContent = `[${hackerNames[currentIndex]}]`;

            // تغيير اللون بشكل عشوائي لمظهر مخيف
            const colors = ["red", "white", "#ff0000", "#ff4d4d"];
            const randomColor = colors[Math.floor(Math.random() * colors.length)];
            nameElement.style.color = randomColor;
            nameElement.style.textShadow = `0 0 20px ${randomColor}`;

            currentIndex = (currentIndex + 1) % hackerNames.length; // التنقل بين الأسماء
        }

        // تغيير الاسم كل ثانية
        setInterval(changeHackerName, 1000);
    </script>

    <!-- صوت تحذيري مرعب -->
    <audio autoplay loop>
        <source src="https://www.myinstants.com/media/sounds/error.mp3" type="audio/mpeg">
    </audio>

</body>
</html>
