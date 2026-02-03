<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Be My Valentine ❤️</title>
    <style>
        body {
            font-family: 'Comic Sans MS', cursive;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .box {
            background: white;
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            width: 350px;
            height: 350px;
            position: relative;
            box-shadow: 0 10px 25px rgba(0,0,0,0.2);
        }

        h1 {
            color: #e60073;
        }

        button {
            padding: 10px 20px;
            font-size: 18px;
            border-radius: 10px;
            border: none;
            cursor: pointer;
        }

        #yesBtn {
            background: #ff4d88;
            color: white;
        }

        #noBtn {
            background: #cccccc;
            color: black;
            position: absolute;
        }

        .buttons {
            margin-top: 40px;
        }

        img {
            width: 250px;
            margin-top: 20px;
            border-radius: 15px;
        }
    </style>
</head>
<body>

<div class="box" id="box">
    <h1>Priyanka- Will you be my Valentine? 💖</h1>

    <div class="buttons">
        <button id="yesBtn" onclick="sayYes()">YES 💘</button>
        <button id="noBtn" onmouseover="moveNo()">NO 😜</button>
    </div>

    <div id="result"></div>
</div>

<script>
    const noBtn = document.getElementById("noBtn");
    const box = document.getElementById("box");

    function moveNo() {
        const boxRect = box.getBoundingClientRect();

        const maxX = boxRect.width - noBtn.offsetWidth;
        const maxY = boxRect.height - noBtn.offsetHeight;

        const randomX = Math.floor(Math.random() * maxX);
        const randomY = Math.floor(Math.random() * maxY);

        noBtn.style.left = randomX + "px";
        noBtn.style.top = randomY + "px";
    }

    function sayYes() {
        document.getElementById("box").innerHTML = `
            <h1>YAYYYYY!!! 😍💖</h1>
            <p>I knew you'd say YES 😘</p>
            <img src="https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExd3R1bTRrbnI4cmR2c3J2bWl0bXc0cDRvZ2l4czZqbW8zYTRnZ3JqYiZlcD12MV9naWZzX3NlYXJjaCZjdD1n/MDJ9IbxxvDUQM/giphy.gif">
        `;
    }
</script>

</body>
</html>

