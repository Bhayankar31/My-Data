<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Personal Data Saver</title>
  <style>
    body {
      background: #f5f5f5;
      font-family: Arial, sans-serif;
    }

    .container {
      max-width: 400px;
      margin: 50px auto;
      background: white;
      padding: 30px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #333;
    }

    label {
      display: block;
      margin: 10px 0 5px;
      color: #555;
    }

    input[type="text"],
    input[type="password"] {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    button {
      width: 100%;
      background: #4CAF50;
      color: white;
      padding: 12px;
      border: none;
      border-radius: 4px;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background: #45a049;
    }

    .message {
      text-align: center;
      margin-top: 15px;
      color: green;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Personal Data Saver</h2>
    <form id="dataForm">
      <label for="name">Name:</label>
      <input type="text" id="name" required />

      <label for="address">Address:</label>
      <input type="text" id="address" required />

      <label for="debit">Debit Card Number:</label>
      <input type="text" id="debit" required />

      <label for="credit">Credit Card Number:</label>
      <input type="text" id="credit" required />

      <label for="password">Password:</label>
      <input type="password" id="password" required />

      <button type="button" onclick="saveData()">Save Data</button>

      <div class="message" id="message"></div>
    </form>
  </div>

  <script>
    function saveData() {
      const data = {
        name: document.getElementById('name').value,
        address: document.getElementById('address').value,
        debit: document.getElementById('debit').value,
        credit: document.getElementById('credit').value,
        password: document.getElementById('password').value,
      };

      // Convert to JSON and save in localStorage (browser only)
      localStorage.setItem('personalData', JSON.stringify(data));

      document.getElementById('message').innerText = 'Data saved locally in your browser!';
    }
  </script>
</body>
</html>
