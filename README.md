<!DOCTYPE html>
<html>
<head>
    <title>Birthday Confession</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f8ff;
            margin-top: 20px;
        }
        #noButton {
            position: absolute;
        }
        .image-container {
            text-align: center;
            margin-bottom: 20px;
        }
        img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
        }
        button {
            padding: 15px 25px;
            font-size: 18px;
            margin: 10px;
            border: none;
            background-color: #4CAF50;
            color: white;
            border-radius: 10px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
    <script>
        function moveButton() {
            // Randomly change the position of the "No" button when hovered over
            var button = document.getElementById("noButton");
            var x = Math.floor(Math.random() * window.innerWidth);
            var y = Math.floor(Math.random() * window.innerHeight);
            button.style.left = x + "px";
            button.style.top = y + "px";
        }

        function confess() {
            alert("Yay! I knew you'd say yes! Happy Birthday to my Angel!");
            // Change the main content to a birthday message and show more pictures
            document.getElementById("mainContent").innerHTML = `
                <h1>Happy Birthday to My Angel!</h1>
                <div class="image-container">
                    <img src="https://example.com/balloons.jpg" alt="Balloons">
                    <img src="https://example.com/cake.jpg" alt="Cake">
                    <img src="https://example.com/party.jpg" alt="Party">
                </div>
                <p>You're the light of my life, and I hope your birthday is as amazing as you are!</p>
            `;
        }
    </script>
</head>
<body>

    <div id="mainContent">
        <h1>Will you go out with me?</h1>
        
        <button onclick="confess()">Yes</button>
        
        <button id="noButton" onmouseover="moveButton()">No</button>
    </div>

</body>
</html>
