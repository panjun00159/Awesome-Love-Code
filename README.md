<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub Cookie Consent</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        #cookieConsent {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background-color: #2d2d2d;
            color: white;
            padding: 10px;
            text-align: center;
            font-size: 14px;
            z-index: 9999;
        }
        #cookieConsent button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 5px 15px;
            font-size: 14px;
            cursor: pointer;
        }
        #cookieConsent button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>

    <!-- Your page content goes here -->

    <!-- Cookie Consent Popup -->
    <div id="cookieConsent">
        <p>我们使用 cookies 来提高您的体验。继续使用即表示您同意我们的 cookie 政策。</p>
        <button onclick="acceptCookies()">接受</button>
    </div>

    <script>
        // 检查是否已接受 cookies
        function checkCookies() {
            if (localStorage.getItem("cookiesAccepted")) {
                document.getElementById("cookieConsent").style.display = "none";
            }
        }

        // 设置 cookies 为已接受
        function acceptCookies() {
            localStorage.setItem("cookiesAccepted", "true");
            document.getElementById("cookieConsent").style.display = "none";
        }

        // 页面加载时检查 cookies 状态
        window.onload = checkCookies;
    </script>

</body>
</html>
