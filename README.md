

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Ansa!</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Montserrat:wght@400;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            transition: all 0.5s ease;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: #ffebee;
            color: #d81b60;
            overflow-x: hidden;
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .page {
            width: 90%;
            max-width: 800px;
            padding: 30px;
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(216, 27, 96, 0.2);
            text-align: center;
            margin: 20px auto;
            position: relative;
            display: none;
            animation: fadeIn 1s ease;
        }
        
        .active-page {
            display: block;
        }
        
        h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 3rem;
            margin-bottom: 20px;
            color: #d81b60;
        }
        
        p {
            font-size: 1.2rem;
            line-height: 1.6;
            margin-bottom: 20px;
        }
        
        .btn {
            background-color: #d81b60;
            color: white;
            border: none;
            padding: 12px 30px;
            font-size: 1.1rem;
            border-radius: 50px;
            cursor: pointer;
            margin-top: 20px;
            font-weight: 600;
            box-shadow: 0 5px 15px rgba(216, 27, 96, 0.4);
        }
        
        .btn:hover {
            background-color: #c2185b;
            transform: translateY(-3px);
        }
        
        .game-container {
            margin: 30px 0;
        }
        
        .game-question {
            font-size: 1.5rem;
            margin-bottom: 20px;
        }
        
        .game-options {
            display: flex;
            justify-content: center;
            gap: 20px;
        }
        
        .game-btn {
            padding: 10px 25px;
            border-radius: 50px;
            font-size: 1.1rem;
            cursor: pointer;
        }
        
        #yes-btn {
            background-color: #4caf50;
            color: white;
            border: none;
        }
        
        #no-btn {
            background-color: #f44336;
            color: white;
            border: none;
            position: relative;
        }
        
        .heart {
            position: absolute;
            font-size: 2rem;
            opacity: 0;
            animation: heartFloat 3s linear forwards;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes heartFloat {
            0% { transform: translateY(0) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-100px) rotate(20deg); opacity: 0; }
        }
        
        .hearts-container {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            overflow: hidden;
        }
        
        .birthday-image {
            width: 100%;
            max-width: 400px;
            height: auto;
            border-radius: 10px;
            margin: 20px auto;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .love-list {
            text-align: left;
            max-width: 600px;
            margin: 0 auto 30px;
        }
        
        .love-list li {
            margin-bottom: 10px;
            list-style-type: none;
            padding-left: 20px;
            position: relative;
        }
        
        .love-list li::before {
            content: "♥";
            color: #d81b60;
            position: absolute;
            left: 0;
        }
        
        .handwritten {
            font-family: 'Dancing Script', cursive;
            font-size: 1.5rem;
            margin: 20px 0;
        }
    </style>
</head>
<body>
    <div class="hearts-container" id="hearts"></div>
    
    <!-- Page 1: Welcome -->
    <div class="page active-page" id="page1">
        <h1>For Someone Special</h1>
        <p>Dear Ansa,</p>
        <p>Before you proceed, I want you to know that this is something made just for you, with all my love and affection.</p>
        <p><em>Take a deep breath and get ready for a little surprise...</em></p>
        <button class="btn" onclick="nextPage()">NEXT</button>
    </div>
    
    <!-- Page 2: Game -->
    <div class="page" id="page2">
        <h1>A Simple Question</h1>
        <div class="game-container">
            <div class="game-question">Do you love Husnain?</div>
            <div class="game-options">
                <button class="game-btn" id="yes-btn">YES</button>
                <button class="game-btn" id="no-btn">NO</button>
            </div>
        </div>
    </div>
    
    <!-- Page 3: Birthday Wishes -->
    <div class="page" id="page3">
        <h1>Happy Birthday Ansa!</h1>
        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/d0d8f0ba-9957-46d3-a8de-72e5d4eef580.png" alt="Birthday celebration with balloons, cake and gifts in pink theme" class="birthday-image">
        <p>Wishing you the most wonderful birthday filled with joy, laughter, and all the happiness you deserve!</p>
        <p>May this year bring you success in all your endeavors and shower you with love and prosperity.</p>
        <button class="btn" onclick="nextPage()">NEXT</button>
    </div>
    
    <!-- Page 4: Prayers -->
    <div class="page" id="page4">
        <h1>Blessings for You</h1>
        <p>May Allah shower His countless blessings upon you today and always.</p>
        <p>May He protect you from all harm and guide you to the right path in life.</p>
        <p>May your dreams come true and may you find happiness in every moment.</p>
        <div class="handwritten">With heartfelt prayers, Husnain</div>
        <button class="btn" onclick="nextPage()">NEXT</button>
    </div>
    
    <!-- Page 5: Love Declaration -->
    <div class="page" id="page5">
        <h1>My Feelings for You</h1>
        <p>Ansa, I want you to know how much you mean to me:</p>
        <div class="love-list">
            <li>Your smile brightens my darkest days</li>
            <li>Your voice is the most beautiful sound to me</li>
            <li>Just thinking about you makes my heart skip a beat</li>
            <li>I can't imagine my life without you in it</li>
            <li>You're the reason I believe in true love</li>
        </div>
        <p class="handwritten">Forever yours, Husnain</p>
        <button class="btn" onclick="nextPage()">NEXT</button>
    </div>
    
    <!-- Page 6: Thank You -->
    <div class="page" id="page6">
        <h1>Thank You</h1>
        <p>Thank you for being you, Ansa.</p>
        <p>Thank you for coming into my life and making it so much more beautiful.</p>
        <p>This simple website can't contain all my feelings, but I hope it makes you smile on your special day.</p>
        <p class="handwritten">With all my love...</p>
        <button class="btn" onclick="restart()">START AGAIN</button>
    </div>

    <script>
        let currentPage = 1;
        const totalPages = 6;
        
        // Initialize game button behavior
        document.addEventListener('DOMContentLoaded', function() {
            const noBtn = document.getElementById('no-btn');
            const yesBtn = document.getElementById('yes-btn');
            
            noBtn.addEventListener('mouseover', function() {
                moveNoButton();
            });
            
            noBtn.addEventListener('click', function() {
                createHearts();
                moveNoButton();
            });
            
            yesBtn.addEventListener('click', function() {
                nextPage();
            });
        });
        
        function nextPage() {
            document.getElementById(`page${currentPage}`).classList.remove('active-page');
            current
