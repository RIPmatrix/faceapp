<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>تسجيل الدخول</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Arial', sans-serif;
      background-color: #f0f2f5;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .login-container {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100%;
    }

    .login-box {
      background-color: #ffffff;
      padding: 40px;
      width: 350px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      text-align: center;
    }

    h2 {
      color: #333;
      margin-bottom: 20px;
      font-size: 24px;
    }

    .textbox {
      margin-bottom: 20px;
      position: relative;
    }

    .textbox input {
      width: 100%;
      padding: 12px;
      border: 2px solid #ddd;
      border-radius: 5px;
      outline: none;
      font-size: 16px;
      transition: all 0.3s ease;
    }

    .textbox input:focus {
      border-color: #007bff;
    }

    .textbox input::placeholder {
      color: #aaa;
    }

    .btn {
      width: 100%;
      padding: 12px;
      background-color: #007bff;
      border: none;
      border-radius: 5px;
      color: white;
      font-size: 16px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    .btn:hover {
      background-color: #0056b3;
    }

    .signup-link {
      margin-top: 15px;
    }

    .signup-link a {
      color: #007bff;
      text-decoration: none;
      font-weight: bold;
    }

    .signup-link a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <div class="login-container">
    <div class="login-box">
      <h2>تسجيل الدخول</h2>
      <form id="loginForm">
        <div class="textbox">
          <input type="text" placeholder="اسم المستخدم" id="username" required>
        </div>
        <div class="textbox">
          <input type="password" placeholder="كلمة المرور" id="password" required>
        </div>
        <button type="submit" class="btn">تسجيل الدخول</button>
      </form>
      <p class="signup-link">لا تملك حسابًا؟ <a href="#">إنشاء حساب</a></p>
    </div>
  </div>

  <script>
    document.getElementById("loginForm").addEventListener("submit", function(event) {
      event.preventDefault();

      let username = document.getElementById("username").value;
      let password = document.getElementById("password").value;

      // هنا يمكنك إضافة التحقق من اسم المستخدم وكلمة المرور
      if (username === "" || password === "") {
        alert("يرجى ملء جميع الحقول.");
      } else {
        // على سبيل المثال: التحقق بنجاح
        alert(`مرحبًا، ${username}! تم تسجيل الدخول بنجاح.`);
      }
    });
  </script>
</body>
</html>
