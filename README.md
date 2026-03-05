<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Mom!</title>
    <style>
        body { text-align: center; font-family: 'Comic Sans MS', cursive; background: #fff0f5; overflow-x: hidden; }
        .container { margin-top: 50px; }
        #cake { font-size: 100px; cursor: pointer; transition: transform 0.3s; display: inline-block; }
        #cake:hover { transform: scale(1.1); }
        .hidden { display: none; }
        .photo-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; padding: 20px; }
        .photo-grid img { width: 100%; border-radius: 15px; border: 5px solid white; box-shadow: 0 4px 8px rgba(0,0,0,0.1); }
        h1 { color: #ff69b4; }
        #message { font-size: 24px; color: #d02090; margin-top: 20px; }
    </style>
</head>
<body>

    <div class="container">
        <h1 id="title">Click the cake to cut it, Mom!</h1>
        <div id="cake" onclick="cutCake()">🎂</div>
        
        <div id="celebration" class="hidden">
            <h1>🍰 YUM! Happy Birthday!</h1>
            <p id="message">You're the best mom in the world!</p>
            
            <audio id="bdayMusic" controls autoplay loop style="margin-bottom: 20px;">
                <source src="your-music-file.mp3" type="audio/mpeg">
                Your browser does not support the audio element.
            </audio>

            <div class="photo-grid">
                <img src="photo1.jpg" alt="Mom and Me 1">
                <img src="photo2.jpg" alt="Mom and Me 2">
                <img src="photo3.jpg" alt="Mom and Me 3">
            </div>
        </div>
    </div>

    <script>
        function cutCake() {
            document.getElementById('cake').style.display = 'none';
            document.getElementById('title').style.display = 'none';
            document.getElementById('celebration').classList.remove('hidden');
            document.getElementById('bdayMusic').play();
            // Optional: Alert or Confetti logic here
            alert("Slice cut! Time for memories ❤️");
        }
    </script>
</body>
</html>
