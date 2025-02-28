<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <title>زر مفاجئ!</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            background-color: #ffe6f2;
            font-family: Arial, sans-serif;
        }

        .container {
            text-align: center;
            position: relative;
            width: 500px;
            height: 300px;
        }

        #question {
            font-size: 24px;
            color: #cc0066;
            margin-bottom: 20px;
        }

        button {
            padding: 15px 30px;
            font-size: 18px;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 25px;
            transition: 0.3s;
        }

        #yesBtn {
            background-color: #66cc66;
            color: white;
        }

        #noBtn {
            background-color: #ff6666;
            color: white;
            position: absolute;
        }

        #heartLoader {
            display: none;
            width: 200px; /* حجم أكبر للـ GIF */
            margin: 20px auto;
        }

        #resultContainer {
            display: none;
            font-size: 28px;
            color: #cc0066;
        }
    </style>
</head>
<body>
    <div class="container">
        <div id="question">هل توافق على هذه المفاجأة؟ 🎁</div>
        <div class="questionContainer">
            <button id="yesBtn">نعم</button>
            <button id="noBtn">لا</button>
        </div>
        <img id="heartLoader" src="https://media4.giphy.com/media/iB6I46FbLRqsLliGpI/giphy.gif" alt="تحميل">
        <div id="resultContainer">مبروك! المفاجأة في طريقها إليك 💝</div>
    </div>

    <script>
        const noBtn = document.getElementById('noBtn');
        const yesBtn = document.getElementById('yesBtn');
        const heartLoader = document.getElementById('heartLoader');
        const resultContainer = document.getElementById('resultContainer');
        const questionContainer = document.querySelector('.questionContainer');

        // حركة الزر "لا" العشوائية
        noBtn.addEventListener("mouseover", () => {
            const newX = Math.random() * (questionContainer.offsetWidth - noBtn.offsetWidth);
            const newY = Math.random() * (questionContainer.offsetHeight - noBtn.offsetHeight);
            
            noBtn.style.left = `${newX}px`;
            noBtn.style.top = `${newY}px`;
        });

        // تأثير الزر "نعم"
        yesBtn.addEventListener("click", () => {
            heartLoader.style.display = "block"; // إظهار الـ GIF
            const timeoutId = setTimeout(() => {
                heartLoader.style.display = "none";
                resultContainer.style.display = "block"; // إظهار الرسالة النهائية
            }, 3000);
        });
    </script>
</body>
</html>
