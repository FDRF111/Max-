<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Макс</title>
    
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="Макс">
    <link rel="apple-touch-icon" href="https://cdn-icons-png.flaticon.com/512/1041/1041916.png">

    <style>
        :root {
            --main-bg: #f0f0f2;
            --accent: #007AFF;
        }
        body {
            margin: 0;
            padding: 0;
            font-family: -apple-system, system-ui, sans-serif;
            background-color: var(--main-bg);
            height: 100vh;
            display: flex;
            flex-direction: column;
        }
        .header {
            background: rgba(255, 255, 255, 0.8);
            backdrop-filter: blur(10px);
            padding: 50px 20px 15px;
            text-align: center;
            font-weight: 600;
            border-bottom: 0.5px solid #ccc;
            position: sticky;
            top: 0;
        }
        .chat {
            flex: 1;
            overflow-y: auto;
            padding: 20px;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .msg {
            max-width: 75%;
            padding: 10px 14px;
            border-radius: 18px;
            font-size: 16px;
            background: white;
            align-self: flex-start;
            box-shadow: 0 1px 2px rgba(0,0,0,0.1);
        }
        .footer {
            background: white;
            padding: 10px 15px 35px; /* Отступ под нижнюю полоску iPhone */
            display: flex;
            gap: 10px;
            align-items: center;
            border-top: 0.5px solid #ccc;
        }
        input {
            flex: 1;
            border: 1px solid #ddd;
            padding: 10px 15px;
            border-radius: 20px;
            font-size: 16px;
            outline: none;
            background: #f9f9f9;
        }
        .send {
            color: var(--accent);
            font-weight: 600;
            font-size: 16px;
        }
    </style>
</head>
<body>

<div class="header">Макс</div>
<div class="chat" id="chat">
    <div class="msg">ошибка</div>
</div>

<form class="footer" onsubmit="event.preventDefault(); document.getElementById('inp').value='';">
    <input type="text" id="inp" placeholder="Cообщение" autocomplete="off">
    <div class="send" onclick="document.getElementById('inp').value='';">Отпр.</div>
</form>

</body>
</html>

