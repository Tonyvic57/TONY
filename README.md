<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Ariana 💖</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to right, #ffdde1, #ee9ca7);
            text-align: center;
            color: #a11d33;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            overflow: hidden;
            padding: 10px;
        }

        h1 {
            font-size: 1.2em;
            max-width: 90%;
        }

        .btn {
            padding: 8px 12px;
            font-size: 0.9em;
            margin: 5px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
            width: 70%;
            max-width: 180px;
        }

        #btnSi {
            background-color: #ff5e78;
            color: white;
        }

        #btnNo {
            background-color: #333;
            color: white;
        }

        #mensaje {
            font-size: 0.9em;
            display: none;
            margin-top: 10px;
            max-width: 90%;
            padding: 10px;
            border-radius: 10px;
            background: rgba(255, 255, 255, 0.9);
            line-height: 1.4;
        }

        #imagen {
            width: 60%;
            max-width: 200px;
            height: auto;
            margin-top: 10px;
            display: none;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <h1>Ariana, ¿quieres ser mi San Valentín? 💖</h1>
    <button id="btnSi" class="btn" onclick="aceptar()">Sí 💕</button>
    <button id="btnNo" class="btn" onclick="cambiarTextoNo()">No 😢</button>
    
    <p id="mensaje"></p>
    <img id="imagen" src="" alt="Respuesta">

    <script>
        let contadorNo = 0;
        const mensajesNo = [
            "¿Estás segura? 😥",
            "Piensa bien... 🥺",
            "No me hagas esto 💔",
            "Duele un poquito... 😢",
            "Por favor... 💖",
            "Te quiero demasiado como para aceptar un no 😭"
        ];

        function aceptar() {
            document.getElementById("imagen").src = "GATO.gif";
            document.getElementById("imagen").style.display = "block";
            document.getElementById("mensaje").style.display = "block";
            document.getElementById("mensaje").innerHTML = 
                "Ariana, si pudiera escribir en el cielo lo que significas para mí, no habría estrellas suficientes para plasmarlo. " +
                "<br><br> Eres mi refugio y mi aventura, mi calma y mi tormenta perfecta. " +
                "Cuando estoy contigo, el mundo deja de girar tan rápido, y todo se siente justo como debería ser. " +
                "<br><br> Eres el lugar donde quiero estar, hoy y siempre. No sé qué nos tenga preparado el destino, pero sí sé que no quiero vivir un solo día sin ti. " +
                "Hoy 14 de febrero quiero que el tiempo se detenga en un abrazo tuyo, en un suspiro compartido, en la certeza de que cada instante a tu lado es un regalo. " +
                "<br><br> Te quiero más de lo que las palabras pueden expresar, y aún así, cada día encuentro una nueva forma de adorarte más. ❤️✨";  
            document.getElementById("btnSi").style.display = "none";
            document.getElementById("btnNo").style.display = "none";
        }

        function cambiarTextoNo() {
            if (contadorNo < mensajesNo.length) {
                document.getElementById("btnNo").innerText = mensajesNo[contadorNo];
                contadorNo++;
            } else {
                document.getElementById("imagen").src = "triste.gif";
                document.getElementById("imagen").style.display = "block";
                document.getElementById("mensaje").style.display = "block";
                document.getElementById("mensaje").innerHTML = 
                    "Oh... 😔 parece que dijiste que no. " +
                    "<br><br> Tal vez algún día, en otro momento, me des un 'Sí'. 💔";
                document.getElementById("btnNo").style.display = "none";
                document.getElementById("btnSi").style.display = "none";
            }
        }
    </script>
</body>
</html>
