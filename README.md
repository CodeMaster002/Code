# Code
Для школы 
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Дом</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #87CEEB;
            margin: 0;
            font-family: Arial, sans-serif;
        }

        .house {
            position: relative;
            width: 300px;
        }

        /* Основание дома */
        .base {
            width: 250px;
            height: 200px;
            background-color: #CD853F;
            margin: 0 auto;
            position: relative;
            border-radius: 5px;
        }

        /* Крыша */
        .roof {
            width: 0;
            height: 0;
            border-left: 150px solid transparent;
            border-right: 150px solid transparent;
            border-bottom: 100px solid #8B4513;
            margin: 0 auto;
        }

        /* Окно */
        .window {
            width: 60px;
            height: 60px;
            background-color: #ADD8E6;
            border-radius: 50%;
            position: absolute;
            top: 50px;
            left: 95px;
            border: 3px solid #000;
        }

        /* Перекладины окна */
        .window::before,
        .window::after {
            content: '';
            position: absolute;
            background-color: #000;
        }

        .window::before {
            width: 60px;
            height: 3px;
            top: 50%;
            left: 0;
            transform: translateY(-50%);
        }

        .window::after {
            width: 3px;
            height: 60px;
            left: 50%;
            top: 0;
            transform: translateX(-50%);
        }

        /* Дымоход */
        .chimney {
            width: 30px;
            height: 60px;
            background-color: #A0522D;
            position: absolute;
            top: -40px;
            right: 50px;
        }

        /* Дверь */
        .door {
            width: 50px;
            height: 90px;
            background-color: #8B4513;
            position: absolute;
            bottom: 0;
            left: 30px;
            border-top-left-radius: 5px;
            border-top-right-radius: 5px;
        }

        /* Ручка двери */
        .door::after {
            content: '';
            width: 8px;
            height: 8px;
            background-color: #FFD700;
            border-radius: 50%;
            position: absolute;
            top: 50%;
            right: 5px;
        }

        /* Наличник */
        .door-frame {
            width: 60px;
            height: 100px;
            background-color: #D2B48C;
            position: absolute;
            bottom: 0;
            left: 25px;
            z-index: -1;
            border-top-left-radius: 5px;
            border-top-right-radius: 5px;
        }

        /* Трава перед домом */
        .grass {
            width: 300px;
            height: 20px;
            background-color: #2E8B57;
            margin: 0 auto;
            border-radius: 0 0 10px 10px;
        }

        /* Солнце */
        .sun {
            width: 80px;
            height: 80px;
            background-color: #FFD700;
            border-radius: 50%;
            position: absolute;
            top: 30px;
            right: 30px;
            box-shadow: 0 0 40px #FFD700;
        }
    </style>
</head>
<body>
    <div class="house">
        <div class="sun"></div>
        <div class="roof"></div>
        <div class="chimney"></div>
        <div class="base">
            <div class="window"></div>
            <div class="door-frame"></div>
            <div class="door"></div>
        </div>
        <div class="grass"></div>
    </div>
</body>
</html>
