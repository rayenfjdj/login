<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>تسجيل دخول مزيف</title>
<style>
  body {
    font-family: Arial, sans-serif;
    background: #f0f0f0;
    display: flex;
    height: 100vh;
    justify-content: center;
    align-items: center;
  }
  .login-container {
    background: white;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
    width: 300px;
  }
  h2 {
    margin-bottom: 20px;
    text-align: center;
  }
  input[type="text"], input[type="password"] {
    width: 100%;
    padding: 10px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  button {
    width: 100%;
    padding: 10px;
    background: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  button:hover {
    background: #0056b3;
  }
  .message {
    margin-top: 15px;
    text-align: center;
    color: red;
  }
</style>
</head>
<body>
<div class="login-container">
  <h2>تسجيل الدخول</h2>
  <input id="username" type="text" placeholder="اسم المستخدم" />
  <input id="password" type="password" placeholder="كلمة المرور" />
  <button onclick="login()">دخول</button>
  <div class="message" id="message"></div>
</div>

<script>
  function login() {
    const user = document.getElementById('username').value;
    const pass = document.getElementById('password').value;
    const message = document.getElementById('message');

    // هنا تحقق بسيط وهمي فقط
    if(user === 'admin' && pass === '1234') {
      message.style.color = 'green';
      message.textContent = 'تم تسجيل الدخول بنجاح!';
    } else {
      message.style.color = 'red';
      message.textContent = 'اسم المستخدم أو كلمة المرور غير صحيحة';
    }
  }
</script>
</body>
</html>
