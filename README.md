<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>موقع دردشة - شبيه Omegle</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(to right, #dfe9f3, #ffffff);
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            text-align: center;
            background-color: #fff;
            padding: 30px 50px;
            border-radius: 15px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
            transition: transform 0.3s ease;
        }
        .container:hover {
            transform: translateY(-5px);
        }
        h1 {
            margin-bottom: 15px;
            color: #222;
        }
        p {
            color: #555;
            font-size: 18px;
            margin-bottom: 25px;
        }
        button {
            background-color: #007bff;
            color: white;
            border: none;
            padding: 12px 25px;
            margin: 10px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s, transform 0.2s;
        }
        button:hover {
            background-color: #0056b3;
            transform: scale(1.05);
        }
        .footer {
            margin-top: 20px;
            font-size: 14px;
            color: #888;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 id="welcomeText">مرحبًا بك في موقع الدردشة!</h1>
        <p>اختر نوع الدردشة التي تفضلها:</p>
        <button onclick="startChat('text')">دردشة نصية</button>
        <button onclick="startChat('video')">دردشة فيديو</button>
        <div class="footer">© 2025 دردش بحرية - جميع الحقوق محفوظة</div>
    </div>

    <script>
        function startChat(type) {
            if (type === 'text') {
                alert('🚀 جاري بدء دردشة نصية...');
                // مثال: window.location.href = "text-chat.html";
            } else if (type === 'video') {
                alert('🎥 جاري بدء دردشة فيديو...');
                // مثال: window.location.href = "video-chat.html";
            }
        }

        // تغيير نص الترحيب تلقائيًا كل بضع ثوانٍ
        const messages = [
            "مرحبًا بك في موقع الدردشة!",
            "تواصل مع أشخاص جدد الآن!",
            "تجربة دردشة ممتعة وآمنة!"
        ];
        let index = 0;
        setInterval(() => {
            document.getElementById('welcomeText').textContent = messages[index];
            index = (index + 1) % messages.length;
        }, 4000);
    </script>
</body>
</html>
