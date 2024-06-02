<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¿Nos hacemos novios?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
        }
        .container {
            text-align: center;
        }
        .button {
            padding: 10px 20px;
            margin: 10px;
            font-size: 16px;
            cursor: pointer;
        }
        #no-button {
            font-size: 16px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>¿Nos hacemos novios?</h1>
        <button class="button" id="si-button">Sí</button>
        <button class="button" id="no-button">No</button>
        <p id="message"></p>
    </div>

    <script>
        const noButton = document.getElementById("no-button");
        const siButton = document.getElementById("si-button");
        const message = document.getElementById("message");

        // El botón "Sí" no hace nada
        siButton.addEventListener("click", () => {
            message.textContent = "";
        });

        noButton.addEventListener("click", () => {
            message.textContent = "Bueno, después te pregunto otra vez.";
            const currentSize = parseInt(window.getComputedStyle(noButton).fontSize);
            noButton.style.fontSize = (currentSize + 2) + "px";
        });
    </script>
</body>
</html>
