# Date
Anniversary 


<!DOCTYPE html>
<html>
<head>
    <title>A Date with Me?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f7e9ec;
            text-align: center;
            flex-direction: column;
            position: relative;
            overflow: hidden;
        }
        .heart {
            position: absolute;
            font-size: 20px;
            color: #ff69b4;
            animation: float 10s ease-in-out infinite;
            pointer-events: none;
        }
        .heart:nth-child(1) { top: 10%; left: 5%; animation-duration: 9s; }
        .heart:nth-child(2) { top: 20%; left: 30%; animation-duration: 11s; }
        .heart:nth-child(3) { top: 50%; left: 15%; animation-duration: 8s; }
        .heart:nth-child(4) { top: 70%; left: 60%; animation-duration: 10s; }
        .heart:nth-child(5) { top: 85%; left: 80%; animation-duration: 12s; }
        .heart:nth-child(6) { top: 40%; left: 90%; animation-duration: 9.5s; }
        
        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }
        .container {
            background-color: #fff;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            max-width: 600px;
            position: relative;
            z-index: 1;
        }
        h1 {
            color: #ff69b4;
        }
        p {
            color: #666;
            line-height: 1.6;
        }
        .options {
            display: flex;
            justify-content: space-around;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        .option {
            background-color: #ffc0cb;
            padding: 20px;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s;
            flex: 1;
            margin: 10px;
            min-width: 150px;
            color: #333;
        }
        .option:hover {
            background-color: #ffb6c1;
        }
        #responseSection, #yesResponse {
            display: none;
            margin-top: 30px;
        }
        .response-button {
            background-color: #ff69b4;
            color: white;
            padding: 10px 20px;
            margin: 0 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .response-button:hover {
            background-color: #e65a9e;
        }
    </style>
</head>
<body>

<div class="heart">❤️</div>
<div class="heart">💖</div>
<div class="heart">❤️</div>
<div class="heart">💖</div>
<div class="heart">❤️</div>
<div class="heart">💖</div>

<div class="container">
    <div id="mainContent">
        <h1>A Date with Me?</h1>
        <p>Hey! I was wondering if you'd like to go on a date with me this <strong>Friday, September 19th</strong>. I'd love to spend the whole day with you!</p>
        <p>I have a few ideas, and I'd love for you to help me decide. Which of these sounds like a perfect day to you?</p>

        <div class="options">
            <div class="option" onclick="selectOption('A. A cozy blanket, a beautiful park, and a picnic full of snacks.')">
                <p><strong>A.</strong> A cozy blanket, a beautiful park, and a picnic full of snacks.</p>
            </div>
            <div class="option" onclick="selectOption('B. Exploring the city, grabbing coffee, and checking out what\'s new in BGC.')">
                <p><strong>B.</strong> Exploring the city, grabbing coffee, and checking out what's new in BGC.</p>
            </div>
            <div class="option" onclick="selectOption('C. Popcorn, a scary movie (like *The Conjuring*), and a good scare.')">
                <p><strong>C.</strong> Popcorn, a scary movie (like *The Conjuring*), and a good scare.</p>
            </div>
            <div class="option" onclick="selectOption('D. A comfy home date with painting sessions and good conversation.')">
                <p><strong>D.</strong> A comfy home date with painting sessions and good conversation.</p>
            </div>
        </div>
    </div>
    
    <div id="responseSection">
        <p>This is my way of officially asking you out. So, [Her Name], will you be my date?</p>
        <button class="response-button" onclick="showYesResponse()">Yes</button>
        <button id="noButton" class="response-button" onclick="changeNoToYes()">No</button>
    </div>

    <div id="yesResponse">
        <h1>Thank you for saying yes!</h1>
        <p style="font-size: 1.2em; color: #ff69b4;">I love you!</p>
        <p>I can't wait to spend the whole day with you on September 19th.</p>
    </div>
</div>

<script>
    function selectOption(optionText) {
        alert("Awesome! Let's make it a " + optionText.toLowerCase().replace('!', '.') + ' date.');
        document.getElementById('mainContent').style.display = 'none';
        document.getElementById('responseSection').style.display = 'block';
    }

    function changeNoToYes() {
        var noButton = document.getElementById('noButton');
        noButton.textContent = 'Yes';
        noButton.onclick = showYesResponse;
    }

    function showYesResponse() {
        document.getElementById('responseSection').style.display = 'none';
        document.getElementById('yesResponse').style.display = 'block';
    }
</script>

</body>
</html>
