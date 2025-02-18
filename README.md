<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الأفضل بالشقة</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            direction: rtl;
        }
        .container {
            margin-top: 50px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            margin: 5px;
            cursor: pointer;
        }
        #message {
            font-size: 20px;
            color: red;
            margin-top: 20px;
            font-weight: bold;
        }
        #image-container {
            margin-top: 20px;
            display: none;
        }
        img {
            width: 200px;
            height: auto;
            border-radius: 10px;
        }
        audio {
            margin-top: 20px;
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>من الأفضل بالشقة؟</h1>
        <button onclick="checkChoice('3badi')">3badi</button>
        <button onclick="checkChoice('f9ool')">f9ool</button>
        <button onclick="checkChoice('mohand')">mohand</button>
        <button onclick="checkChoice('s3ood')">s3ood</button>

        <p id="message"></p>
        <div id="image-container">
            <img src="https://i.postimg.cc/hvQP2Yr2/IMG-0854.jpg" alt="صورة 3badi">
        </div>
        
        <!-- أغنية عم المجال كلو -->
        <audio id="song" controls>
            <source src="https://drive.google.com/uc?export=download&id=1UEhAcrnxSuqmYcCQOojon8aG-tMUl9xi" type="audio/mp3">
            متصفحك لا يدعم عنصر الصوت.
        </audio>
    </div>

    <script>
        function checkChoice(name) {
            var song = document.getElementById("song");
            if (name === '3badi') {
                document.getElementById("message").innerText = "أحسنت الاختيار!";
                document.getElementById("image-container").style.display = "block";
                song.style.display = "block"; // إظهار مشغل الصوت
                song.play(); // تشغيل الأغنية تلقائيًا
            } else {
                document.getElementById("message").innerText = "ارجع اختار عمك!";
                document.getElementById("image-container").style.display = "none";
                song.pause(); // إيقاف الأغنية عند الاختيار الخاطئ
                song.currentTime = 0; // إعادة تشغيل الأغنية من البداية عند الاختيار الصحيح لاحقًا
            }
        }
    </script>
</body>
</html>
