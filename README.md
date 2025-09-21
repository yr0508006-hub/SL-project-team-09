<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Patient Details</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(120deg, #3a8dde, #6dd5ed);
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .container {
      background: rgba(0, 0, 0, 0.6);
      padding: 30px;
      border-radius: 15px;
      width: 400px;
    }
    h2 {
      text-align: center;
      margin-bottom: 20px;
    }
    label {
      display: block;
      margin-top: 10px;
    }
    input, textarea, button {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border: none;
      border-radius: 8px;
    }
    button {
      margin-top: 20px;
      background: #4CAF50;
      color: white;
      cursor: pointer;
      font-weight: bold;
    }
    button:hover {
      background: #45a049;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Patient Details</h2>
    <form id="patientForm" action="dosage_calculator.html">
      <label>Name:</label>
      <input type="text" id="name" required>

      <label>Age:</label>
      <input type="number" id="age" required>

      <label>Height (cm):</label>
      <input type="number" id="height" required>

      <label>Weight (kg):</label>
      <input type="number" id="weight" required>

      <label>Sugar Level (mg/dL):</label>
      <input type="number" id="sugar" required>

      <label>Other Conditions:</label>
      <textarea id="conditions" rows="3"></textarea>

      <button type="submit">Go to Calculator</button>
    </form>
  </div>

  <script>
    // Save data to localStorage to use on next page
    document.getElementById("patientForm").addEventListener("submit", function() {
      localStorage.setItem("name", document.getElementById("name").value);
      localStorage.setItem("age", document.getElementById("age").value);
      localStorage.setItem("height", document.getElementById("height").value);
      localStorage.setItem("weight", document.getElementById("weight").value);
      localStorage.setItem("sugar", document.getElementById("sugar").value);
      localStorage.setItem("conditions", document.getElementById("conditions").value);
    });
  </script>
</body>
</html>
