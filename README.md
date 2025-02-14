<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hola, Daniela. ¿Te gustaría salir conmigo?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f8ff;
        }
        .container {
            margin-top: 50px;
        }
        h1 {
            color: #ff1493;
        }
        .emoji {
            font-size: 50px;
        }
        .heart-img {
            width: 100px;
            height: 100px;
            margin: 20px 0;
        }
        .message {
            font-size: 24px;
            color: #333;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            padding: 15px 30px;
            font-size: 20px;
            background-color: #ff1493;
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            margin: 10px;
        }
        .move {
            animation: moveOption 1s infinite alternate;
        }
        @keyframes moveOption {
            0% { transform: translateX(0); }
            50% { transform: translateX(300px); }
            100% { transform: translateX(0); }
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Hola, Daniela. ¿Te gustaría salir conmigo? <span class="emoji">😍</span></h1>
    <!-- Imagen de Dudu y Bubu ahora primero -->
    <img id="duduBubu" src="https://ih1.redbubble.net/image.3760740289.3463/st,small,507x507-pad,600x600,f8f8f8.jpg" alt="Dudu y Bubu" style="width: 150px; height: 150px;">
    <p class="message">Me la debes</p>

    <div class="buttons">
        <button id="yesButton">Sí</button>
        <button id="noButton">No</button>
    </div>

    <div id="response" style="display:none;">
        <p id="yesResponse" style="font-size: 24px; color: green;"></p>
        <!-- Imagen de corazón ahora después del mensaje -->
        <img src="https://i.pinimg.com/736x/8d/43/25/8d4325b615597600ff8e406641a3831d.jpg" alt="Corazón" class="heart-img">
    </div>
</div>

<script>
    document.getElementById("yesButton").onclick = function() {
        document.getElementById("response").style.display = "block";
        document.getElementById("yesResponse").innerText = "Hehehe, lo sabía.";
    }

    document.getElementById("noButton").onclick = function() {
        var button = document.getElementById("noButton");
        button.classList.add("move");
    }
</script>

</body>
</html>
