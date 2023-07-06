<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <link rel="stylesheet" href="styles.css"> <!-- Create this CSS file later -->
    <style>
        /* Your existing styles for the login page */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
        }
        
        .login-container {
            text-align: center;
            background-color: #fff;
            border: 1px solid #ddd;
            padding: 30px;
            border-radius: 5px;
        }
        
        h1 {
            margin-bottom: 20px;
        }
        
        .form-group {
            margin-bottom: 15px;
        }
        
        label {
            display: block;
            font-weight: bold;
        }
        
        input {
            width: 100%;
            padding: 8px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        
        button {
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h1>Login Page</h1>
        <form id="login-form">
            <div class="form-group">
                <label for="username">Username</label>
                <input type="text" id="username" name="username" required>
            </div>
            <div class="form-group">
                <label for="password">Password</label>
                <input type="password" id="password" name="password" required>
            </div>
            <button type="submit">Login</button>
        </form>
    </div>

    <script>
        const form = document.getElementById('login-form');

        form.addEventListener('submit', (event) => {
            event.preventDefault(); // Prevent form submission

            // Fetch the entered username and password
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;

            // Validate the login credentials
            if (username === 'DONARD' && password === 'PASS') {
                // Redirect the user to the landing page
                window.location.href = 'landing_page.html';
            }
            else {
                // Show an error message for invalid credentials (you can enhance this with a proper UI)
                alert('Invalid username or password. Please try again later.');
            }
        }
    );
        
    </script>
</body>
</html>
