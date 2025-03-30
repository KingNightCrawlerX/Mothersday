<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Happy Mother's Day!</title>
    <style>
        body {
            background-color: #ffebf0;
            text-align: center;
            font-family: Arial, sans-serif;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            overflow: hidden;
        }
        
        .card {
            width: 300px;
            height: 200px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 22px;
            color: #e91e63;
            font-weight: bold;
            cursor: pointer;
            position: relative;
            transition: transform 0.6s ease-in-out;
        }

        .card:hover {
            transform: scale(1.05);
        }

        .card-content {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: opacity 0.4s ease-in-out;
        }

        .hidden-content {
            position: absolute;
            width: 350px;
            height: 450px;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            opacity: 0;
            transform: scale(0.5);
            transition: opacity 0.6s ease-in-out, transform 0.6s ease-in-out;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        h1 {
            color: #e91e63;
        }

        .message {
            font-size: 18px;
            color: #333;
            text-align: center;
        }

        .heart {
            font-size: 50px;
            color: #e91e63;
            animation: heartbeat 1.5s infinite;
        }

        @keyframes heartbeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.3); }
            100% { transform: scale(1); }
        }

        .footer {
            font-size: 14px;
            color: #777;
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <!-- Clickable Card -->
    <div class="card" onclick="openCard()">
        <div class="card-content">💌 Click to Open</div>
    </div>

    <!-- Hidden Message (Appears When Clicked) -->
    <div class="hidden-content" id="messageBox">
        <h1>Happy Mother's Day! 💐</h1>
        <p class="message">Dear Mummy,</p>
        <p class="message">
            Thank you for everything you have done for me over the past year. <br>
            You are the best mother a son could ask for—patient, kind, and supportive. <br>
            You make the world a better place just by being in it. <br>
            Wishing you a beautiful day filled with joy!
        </p>
        <div class="heart">❤️</div>
        <p class="footer">Lots and lots of love,<br>William</p>
    </div>

    <script>
        function openCard() {
            document.querySelector(".card").style.display = "none";
            let messageBox = document.getElementById("messageBox");
            messageBox.style.opacity = "1";
            messageBox.style.transform = "scale(1)";
        }
    </script>

</body>
</html>
