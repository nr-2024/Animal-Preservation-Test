<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animal Preservation - Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .login-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }
        h1 {
            margin-bottom: 20px;
            color: #333;
        }
        .input-group {
            margin-bottom: 15px;
        }
        .input-group label {
            display: block;
            text-align: left;
            margin-bottom: 5px;
            color: #555;
        }
        .input-group input {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .btn {
            background-color: #4CAF50;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            width: 100%;
            cursor: pointer;
        }
        .btn:hover {
            background-color: #45a049;
        }
        .message {
            margin-top: 20px;
            color: #777;
        }
    </style>
</head>
<body>

    <div class="login-container">
        <h1>Animal Preservation</h1>
        <form id="login-form">
            <div class="input-group">
                <label for="username">Username</label>
                <input type="text" id="username" name="username" required>
            </div>
            <div class="input-group">
                <label for="password">Password</label>
                <input type="password" id="password" name="password" required>
            </div>
            <button type="submit" class="btn">Login</button>
        </form>
        <div class="message">
            <p>Don't have an account? <a href="/register">Sign up</a></p>
        </div>
    </div>

    <script>
        document.getElementById("login-form").addEventListener("submit", function(event) {
            event.preventDefault(); // Prevent the form from submitting immediately

            // Get the input values
            const username = document.getElementById("username").value;
            const password = document.getElementById("password").value;

            // Simple validation (this should be replaced with a real backend authentication check)
            if (username === "admin" && password === "password") {
                // Redirect to the dashboard or another page upon successful login
                window.location.href = "/dashboard";  // Change this URL to the page you want to navigate to
            } else {
                alert("Invalid login credentials. Please try again.");
            }
        });
    </script>

</body>
</html>
