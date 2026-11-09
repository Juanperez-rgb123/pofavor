# porfavor
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apoyo</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            background-color: #f4f4f4;
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .container {
            text-align: center;
            background: white;
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            max-width: 400px;
            width: 90%;
        }

        .emoji {
            font-size: 50px;
            margin-bottom: 15px;
        }

        h1 {
            font-size: 20px;
            color: #333;
            margin-bottom: 25px;
            line-height: 1.4;
        }

        .btn {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 12px 30px;
            font-size: 16px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: bold;
        }

        #video-screen {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: black;
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    </style>
</head>
<body>

    <div class="container" id="main-card">
        <div class="emoji">❤️‍🩹</div>
        <h1>¿Podrías rezar por esta persona por favor?</h1>
        <button class="btn" id="accept-btn">Aceptar</button>
    </div>

    <div id="video-screen">
        <video id="scare-video" src="https://www.youtube.com/embed/UZw7y0-txpI" controls></video>
    </div>

    <script>
        const btn = document.getElementById('accept-btn');
        const mainCard = document.getElementById('main-card');
        const videoScreen = document.getElementById('video-screen');
        const video = document.getElementById('scare-video');

        btn.addEventListener('click', () => {
            mainCard.style.display = 'none';
            videoScreen.style.display = 'flex';
            video.play().catch(error => {
                console.log("Reproducción automática:", error);
            });
        });
    </script>
</body>
</html>
