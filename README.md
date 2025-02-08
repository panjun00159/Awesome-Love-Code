<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>reCAPTCHA v2 示例</title>

    <!-- 引入 Google reCAPTCHA JS 库 -->
    <script src="https://www.google.com/recaptcha/api.js" async defer></script>
</head>
<body>
    <h2>用户注册表单</h2>
    <form action="你的后端处理脚本" method="POST">
        <label for="username">用户名：</label>
        <input type="text" id="username" name="username" required><br><br>

        <label for="password">密码：</label>
        <input type="password" id="password" name="password" required><br><br>

        <!-- 插入 reCAPTCHA 验证码 -->
        <div class="g-recaptcha" data-sitekey="6LcgftAqAAAAAFo7pXZW-npEay_DaaPzLug3mYAn"></div>
        
        <br><br>
        <button type="submit">提交</button>
    </form>
</body>
</html>
