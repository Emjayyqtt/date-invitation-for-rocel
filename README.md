<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Rocel 💖</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial Rounded MT Bold', 'Arial', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #ff9a9e, #fad0c4, #fbc2eb);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            position: relative;
        }
        
        .container {
            background-color: rgba(255, 255, 255, 0.92);
            border-radius: 25px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            padding: 40px;
            width: 90%;
            max-width: 500px;
            text-align: center;
            z-index: 10;
            position: relative;
            animation: fadeIn 1s ease-out;
        }
        
        h1 {
            color: #ff6b6b;
            margin-bottom: 20px;
            font-size: 2.8rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        p {
            color: #555;
            margin-bottom: 25px;
            font-size: 1.3rem;
            line-height: 1.6;
        }
        
        .buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        button {
            padding: 16px 32px;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        #yes-btn {
            background: linear-gradient(to right, #ff6b6b, #ff8e8e);
            color: white;
            flex: 1;
            min-width: 120px;
        }
        
        #no-btn {
            background: linear-gradient(to right, #cccccc, #aaaaaa);
            color: white;
            flex: 1;
            min-width: 120px;
            position: relative;
        }
        
        button:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
        }
        
        button:active {
            transform: translateY(0);
        }
        
        .confirmation {
            display: none;
            animation: fadeIn 1s ease-out;
        }
        
        .confirmation h2 {
            color: #ff6b6b;
            margin-bottom: 20px;
            font-size: 2.2rem;
        }
        
        .date-details {
            background: linear-gradient(to right, #f8f5ff, #fff);
            border-radius: 20px;
            padding: 25px;
            margin: 25px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .date-details p {
            margin: 12px 0;
            font-size: 1.2rem;
        }
        
        .heart {
            position: absolute;
            font-size: 20px;
            color: #ff6b6b;
            opacity: 0.7;
            z-index: 1;
            pointer-events: none;
        }
        
        .music-control {
            position: absolute;
            top: 20px;
            right: 20px;
            background: rgba(255, 255, 255, 0.9);
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            z-index: 100;
        }
        
        .music-control i {
            color: #ff6b6b;
            font-size: 22px;
        }
        
        .sad-message {
            display: none;
            color: #ff6b6b;
            font-size: 1.4rem;
            margin-top: 20px;
            animation: pulse 1.5s infinite;
        }
        
        .instructions {
            position: absolute;
            top: 20px;
            left: 20px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            z-index: 100;
            width: 300px;
            display: none;
        }
        
        .instructions h3 {
            color: #ff6b6b;
            margin-bottom: 10px;
        }
        
        .instructions ol {
            text-align: left;
            padding-left: 20px;
        }
        
        .instructions li {
            margin-bottom: 8px;
            font-size: 0.9rem;
        }
        
        .help-btn {
            position: absolute;
            top: 20px;
            left: 20px;
            background: rgba(255, 255, 255, 0.9);
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            z-index: 100;
        }
        
        .help-btn i {
            color: #ff6b6b;
            font-size: 22px;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        @keyframes float {
            0% { transform: translateY(0) rotate(0deg); opacity: 0.7; }
            50% { transform: translateY(-25px) rotate(10deg); opacity: 0.9; }
            100% { transform: translateY(0) rotate(0deg); opacity: 0.7; }
        }
        
        @keyframes sparkle {
            0% { transform: scale(0.8); opacity: 0; }
            50% { transform: scale(1.2); opacity: 1; }
            100% { transform: scale(0.8); opacity: 0; }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        @keyframes shake {
            0% { transform: translateX(0); }
            25% { transform: translateX(-10px); }
            50% { transform: translateX(10px); }
            75% { transform: translateX(-10px); }
            100% { transform: translateX(0); }
        }
        
        @media (max-width: 600px) {
            .container {
                padding: 25px;
                width: 95%;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            p {
                font-size: 1.1rem;
            }
            
            button {
                padding: 14px 28px;
                font-size: 1.1rem;
            }
            
            .buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .instructions {
                width: 80%;
                left: 10%;
                top: 70px;
            }
        }
    </style>
</head>
<body>
    <!-- Help Button -->
    <div class="help-btn" id="help-btn">
        <i class="fas fa-question"></i>
    </div>
    
    <!-- Instructions -->
    <div class="instructions" id="instructions">
        <h3>How to Share This Invitation</h3>
        <ol>
            <li>Save this file (Ctrl+S or File → Save)</li>
            <li>Upload to Netlify Drop: <a href="https://app.netlify.com/drop" target="_blank">https://app.netlify.com/drop</a></li>
            <li>Drag and drop the HTML file</li>
            <li>Copy the provided link and send it to Rocel</li>
        </ol>
        <p>Alternative: Use GitHub Pages, Vercel, or any free hosting service.</p>
    </div>
    
    <!-- Music Control -->
    <div class="music-control" id="music-control">
        <i class="fas fa-volume-mute"></i>
    </div>
    
    <!-- Main Content -->
    <div class="container">
        <div class="invitation">
            <h1>Hi loveeeee 💖</h1>
            <p>Gusto ra nako i celebrate atong ika 4th monthsary bisag wala na ta haha. I was wondering...</p>
            <p>Would you like to go on a date with me?</p>
            
            <div class="buttons">
                <button id="yes-btn">Yes</button>
                <button id="no-btn">No</button>
            </div>
            
            <div class="sad-message" id="sad-message">
                You don't love me na ba? 😢
            </div>
        </div>
        
        <div class="confirmation">
            <h2>Yay! 💕</h2>
            <p>I'm so excited to spend time with you!</p>
            
            <div class="date-details">
                <p><i class="far fa-calendar-alt"></i> <strong>Date:</strong> Thursday, August 28th</p>
                <p><i class="far fa-clock"></i> <strong>Time:</strong> 7:00 PM</p>
                <p><i class="fas fa-map-marker-alt"></i> <strong>Place:</strong> Beracah. (pwede pud kung asa ka ganahan hehe)</p>
            </div>
            
            <p>Thankyou Ex HAHAHA Can't wait to see you! 😊</p>
        </div>
    </div>
    
    <!-- Audio Element -->
    <audio id="bg-music" loop>
        <source src="https://cdn.pixabay.com/download/audio/2022/01/20/audio_dc6cffc5c5.mp3?filename=soft-inspiring-background-amp-piano-118532.mp3" type="audio/mpeg">
    </audio>
    
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const invitation = document.querySelector('.invitation');
            const confirmation = document.querySelector('.confirmation');
            const yesBtn = document.getElementById('yes-btn');
            const noBtn = document.getElementById('no-btn');
            const sadMessage = document.getElementById('sad-message');
            const musicControl = document.getElementById('music-control');
            const helpBtn = document.getElementById('help-btn');
            const instructions = document.getElementById('instructions');
            const bgMusic = document.getElementById('bg-music');
            const body = document.body;
            let musicPlaying = false;
            let noCount = 0;
            
            // Create floating hearts
            function createHearts() {
                for (let i = 0; i < 25; i++) {
                    const heart = document.createElement('div');
                    heart.innerHTML = '❤';
                    heart.classList.add('heart');
                    
                    // Random position and size
                    const size = Math.random() * 25 + 15;
                    const left = Math.random() * 100;
                    const top = Math.random() * 100;
                    
                    heart.style.fontSize = `${size}px`;
                    heart.style.left = `${left}%`;
                    heart.style.top = `${top}%`;
                    
                    // Random animation
                    const duration = Math.random() * 5 + 5;
                    const delay = Math.random() * 5;
                    heart.style.animation = `float ${duration}s ease-in-out ${delay}s infinite`;
                    
                    body.appendChild(heart);
                }
            }
            
            // Create sparkles
            function createSparkles() {
                for (let i = 0; i < 15; i++) {
                    const sparkle = document.createElement('div');
                    sparkle.innerHTML = '✨';
                    sparkle.classList.add('heart');
                    
                    // Random position and size
                    const size = Math.random() * 20 + 10;
                    const left = Math.random() * 100;
                    const top = Math.random() * 100;
                    
                    sparkle.style.fontSize = `${size}px`;
                    sparkle.style.left = `${left}%`;
                    sparkle.style.top = `${top}%`;
                    
                    // Random animation
                    const duration = Math.random() * 3 + 2;
                    const delay = Math.random() * 3;
                    sparkle.style.animation = `sparkle ${duration}s ease-in-out ${delay}s infinite`;
                    
                    body.appendChild(sparkle);
                }
            }
            
            // Button click handlers
            yesBtn.addEventListener('click', showConfirmation);
            
            noBtn.addEventListener('click', function() {
                noCount++;
                
                if (noCount === 1) {
                    sadMessage.style.display = 'block';
                    noBtn.style.animation = 'shake 0.5s ease';
                    setTimeout(() => {
                        noBtn.style.animation = '';
                    }, 500);
                } else if (noCount === 2) {
                    sadMessage.textContent = "hala ngano gud mag NO ka??";
                    noBtn.style.animation = 'shake 0.5s ease';
                    setTimeout(() => {
                        noBtn.style.animation = '';
                    }, 500);
                } else if (noCount === 3) {
                    sadMessage.textContent = "Pretty please? 🥺";
                    noBtn.style.animation = 'shake 0.5s ease';
                    setTimeout(() => {
                        noBtn.style.animation = '';
                    }, 500);
                } else if (noCount === 4) {
                    sadMessage.textContent = "pangging ba!!!🥺";
                    noBtn.style.animation = 'shake 0.5s ease';
                    setTimeout(() => {
                        noBtn.style.animation = '';
                    }, 500);
                } else {
                    sadMessage.textContent = "Okay, I'll stop... just kidding! 😜";
                    noBtn.style.animation = 'shake 0.5s ease';
                    setTimeout(() => {
                        noBtn.style.animation = '';
                    }, 500);
                    
                    // After many no's, make the yes button more appealing
                    yesBtn.style.transform = 'scale(1.1)';
                    yesBtn.style.boxShadow = '0 8px 25px rgba(255, 107, 107, 0.4)';
                }
            });
            
            function showConfirmation() {
                invitation.style.display = 'none';
                confirmation.style.display = 'block';
                
                // Create more hearts when she says yes
                for (let i = 0; i < 15; i++) {
                    const heart = document.createElement('div');
                    heart.innerHTML = '❤';
                    heart.classList.add('heart');
                    
                    const size = Math.random() * 30 + 20;
                    const left = Math.random() * 100;
                    const top = Math.random() * 100;
                    
                    heart.style.fontSize = `${size}px`;
                    heart.style.left = `${left}%`;
                    heart.style.top = `${top}%`;
                    
                    const duration = Math.random() * 4 + 3;
                    heart.style.animation = `float ${duration}s ease-in-out infinite`;
                    
                    body.appendChild(heart);
                }
            }
            
            // Music control
            musicControl.addEventListener('click', function() {
                if (musicPlaying) {
                    bgMusic.pause();
                    musicControl.innerHTML = '<i class="fas fa-volume-mute"></i>';
                } else {
                    bgMusic.play().catch(e => {
                        console.log("Audio play failed: ", e);
                        musicControl.style.display = 'none';
                    });
                    musicControl.innerHTML = '<i class="fas fa-volume-up"></i>';
                }
                musicPlaying = !musicPlaying;
            });
            
            // Help button
            helpBtn.addEventListener('click', function() {
                instructions.style.display = instructions.style.display === 'block' ? 'none' : 'block';
            });
            
            // Initialize animations
            createHearts();
            createSparkles();
        });
    </script>
</body>
</html>
