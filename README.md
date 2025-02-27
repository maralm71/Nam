# Nam
<!DOCTYPE html>
<html lang="fa">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>فال اسم شما</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: black;
            color: white;
            padding: 50px;
        }
        input, button {
            font-size: 18px;
            padding: 10px;
            margin: 10px;
        }
        #result {
            margin-top: 20px;
            font-size: 20px;
        }
    </style>
</head>
<body>

    <h2>✨ فال بر اساس نام شما ✨</h2>
    <p>نام خود را وارد کنید:</p>
    <input type="text" id="nameInput" placeholder="مثلاً علی">
    <button onclick="getFal()">دریافت فال</button>
    <div id="result"></div>

    <script>
        const falList = [
            "🌟 امروز برای تو روز خوبی خواهد بود، از فرصت‌ها استفاده کن!",
            "🎯 موفقیت نزدیک است، فقط کافی است که امیدت را از دست ندهی.",
            "🎁 یک سورپرایز در راه داری، آماده باش!",
            "🔮 به زودی یک تصمیم مهم خواهی گرفت که مسیر زندگی‌ات را تغییر می‌دهد.",
            "🚀 امروز زمان خوبی برای شروع یک کار جدید است، از آن نترس!",
            "📩 منتظر یک پیام خوشحال‌کننده باش، کسی به تو فکر می‌کند!",
            "💡 ایده‌ای که در ذهنت داری، به زودی به نتیجه می‌رسد.",
            "❤️ عشقی در اطراف توست که هنوز متوجه آن نشده‌ای.",
            "🍀 شانس با توست! به ندای درونت گوش بده و ریسک کن.",
            "🕰️ صبر کن، زمان به نفع تو خواهد بود!",
            "🎶 امروز موسیقی گوش بده، نشانه‌ای در آن خواهی یافت.",
            "💰 نشانه‌هایی از پیشرفت مالی در کارت دیده می‌شود.",
            "📚 امروز روز یادگیری است، دانشی که کسب می‌کنی به دردت خواهد خورد.",
            "🌊 آرامش را در طبیعت جستجو کن، انرژی مثبتی به تو بازمی‌گردد.",
            "🔥 امروز جرقه‌ای در ذهن تو زده خواهد شد که آینده را تغییر می‌دهد."
        ];

        function getFal() {
            let name = document.getElementById("nameInput").value.trim();
            if (name === "") {
                alert("لطفاً نام خود را وارد کنید!");
                return;
            }

            let luckyNumber = name.length % falList.length;
            document.getElementById("result").innerHTML = `🌟 عدد شانس شما: ${luckyNumber + 1}<br>📜 ${falList[luckyNumber]}`;
        }
    </script>

</body>
</html>
