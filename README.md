<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will you be my Valentine?</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #fce4ec;
            font-family: 'Arial', sans-serif;
            overflow: hidden;
            text-align: center;
        }
        .container {
            background: white;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            padding: 10px 25px;
            font-size: 18px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin: 0 10px;
            transition: 0.3s;
        }
        #yesBtn { background-color: #e91e63; color: white; }
        #noBtn { background-color: #90a4ae; color: white; position: absolute; }
    </style>
</head>
<body>

    <div class="container">
        <h1 id="question">Will you be my Valentine? ❤️</h1>
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">Yes</button>
            <button id="noBtn" onmouseover="moveButton()">No</button>
        </div>
    </div>

    <script>
        function moveButton() {
            const x = Math.random() * (window.innerWidth - 100);
            const y = Math.random() * (window.innerHeight - 50);
            const noBtn = document.getElementById('noBtn');
            noBtn.style.left = x + 'px';
            noBtn.style.top = y + 'px';
        }

        function celebrate() {
            document.getElementById('question').innerHTML = "YAY! 🥳✨";
            document.querySelector('.buttons').style.display = 'none';
        }
    </script>

</body>
</html>
