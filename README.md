<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>2-Key Authentication</title>
  <style>
    /* Dark Mode Background and Text */
    body {
      background-color: #1b1b1b;
      color: #e0e0e0;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    /* Container for the authentication boxes */
    .auth-container {
      text-align: center;
      padding: 2rem;
      border-radius: 15px;
      background-color: #333;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
      width: 300px;
    }

    h1 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
    }

    /* Input box styling */
    input[type="text"] {
      width: 90%;
      padding: 10px;
      border-radius: 50px;
      border: none;
      margin-bottom: 1rem;
      background-color: #222;
      color: #fff;
    }

    /* Circle button styling */
    button {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      border: none;
      background-color: #6200ea;
      color: white;
      font-size: 1.2rem;
      cursor: pointer;
      margin-top: 10px;
      transition: background-color 0.3s ease;
    }

    button:hover {
      background-color: #3700b3;
    }

    /* Hide error text by default */
    .error {
      color: red;
      display: none;
      font-size: 0.9rem;
    }
  </style>
</head>
<body>
  <!-- First Authentication Page -->
  <div class="auth-container" id="auth1">
    <h1>Enter First Key</h1>
    <input type="text" id="firstKey" placeholder="Enter Key">
    <button onclick="checkFirstKey()">✔</button>
    <p class="error" id="error1">Incorrect key. Try again.</p>
  </div>

  <!-- Second Authentication Page -->
  <div class="auth-container" id="auth2" style="display: none;">
    <h1>Enter Admin Key</h1>
    <input type="text" id="secondKey" placeholder="Enter Admin Key">
    <button onclick="checkSecondKey()">✔</button>
    <p class="error" id="error2">Incorrect admin key. Try again.</p>
  </div>

  <script>
    // First authentication key: "AmasisReborn"
    function checkFirstKey() {
      const firstKeyInput = document.getElementById('firstKey').value;
      if (firstKeyInput === 'AmasisReborn') {
        document.getElementById('auth1').style.display = 'none';
        document.getElementById('auth2').style.display = 'block';
      } else {
        document.getElementById('error1').style.display = 'block';
      }
    }

    // Second authentication key: "gEX7jN64iUmrDq9pvHSWwCz1cPOFKyTlAo53LMRZ0hQVtBdIkf2sb8YJaeGxuXn"
    function checkSecondKey() {
      const secondKeyInput = document.getElementById('secondKey').value;
      if (secondKeyInput === 'gEX7jN64iUmrDq9pvHSWwCz1cPOFKyTlAo53LMRZ0hQVtBdIkf2sb8YJaeGxuXn') {
        // Redirect to the external page upon success
        window.location.href = "https://loot-link.com/s?417e78f8";
      } else {
        document.getElementById('error2').style.display = 'block';
      }
    }
  </script>
</body>
</html>
