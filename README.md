<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Payment & Receipt Tracker - Login</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
        }

        body {
            background: #f2f4f7;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .login-box {
            background: white;
            width: 350px;
            padding: 35px;
            border-radius: 12px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.12);
        }

        h1 {
            text-align: center;
            margin-bottom: 8px;
            color: #222;
        }

        .subtitle {
            text-align: center;
            color: #777;
            margin-bottom: 25px;
            font-size: 14px;
        }

        label {
            display: block;
            margin-bottom: 6px;
            color: #333;
            font-weight: bold;
        }

        input {
            width: 100%;
            padding: 12px;
            margin-bottom: 18px;
            border: 1px solid #ccc;
            border-radius: 7px;
            font-size: 15px;
        }

        input:focus {
            outline: none;
            border-color: #4a6cf7;
        }

        button {
            width: 100%;
            padding: 12px;
            background: #4a6cf7;
            color: white;
            border: none;
            border-radius: 7px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background: #3451c7;
        }

        #message {
            text-align: center;
            margin-top: 15px;
            color: red;
            font-size: 14px;
        }
    </style>
</head>

<body>

    <div class="login-box">

        <h1>Welcome</h1>
        <p class="subtitle">Payment & Receipt Tracker</p>

        <form id="loginForm">

            <label>Username</label>
            <input type="text" id="username" placeholder="Enter username" required>

            <label>Password</label>
            <input type="password" id="password" placeholder="Enter password" required>

            <button type="submit">Login</button>

            <p id="message"></p>

        </form>

    </div>

    <script>
        document.getElementById("loginForm").addEventListener("submit", function(event) {

            event.preventDefault();

            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;

            // Demo login details
            if (username === "admin" && password === "1234") {
                alert("Login successful!");
                window.location.href = "dashboard.html";
            } else {
                document.getElementById("message").textContent =
                    "Invalid username or password";
            }

        });
    </script>

</body>
</html>
