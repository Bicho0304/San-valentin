# San-valentin
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carta para Ti</title>
    <style>
        body {
            background-color: #ffcccc;
            text-align: center;
            font-family: 'Arial', sans-serif;
        }
        .container {
            margin-top: 50px;
            opacity: 0;
            transform: scale(0.8);
            animation: fadeIn 2s forwards ease-in-out;
        }
        @keyframes fadeIn {
            0% { opacity: 0; transform: scale(0.8); }
            100% { opacity: 1; transform: scale(1); }
        }
        .hidden {
            opacity: 0;
        }
        .message {
            font-size: 24px;
            color: #b30000;
            margin-top: 20px;
            transition: opacity 2s;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Para la persona más especial</h1>
        <button onclick="showMessage()">Haz clic para ver la carta</button>
        <p id="msg1" class="message hidden">Desde que entraste en mi vida, todo es más hermoso.</p>
        <p id="msg2" class="message hidden">Cada día a tu lado es un regalo que valoro infinitamente.</p>
        <p id="msg3" class="message hidden">Te amo con todo mi corazón. ¡Feliz San Valentín!</p>
    </div>

    <script>
        function showMessage() {
            let messages = document.querySelectorAll('.message');
            messages.forEach((msg, index) => {
                setTimeout(() => {
                    msg.style.opacity = "1";
                }, index * 2000);
            });
        }
    </script>
</body>
</html>
