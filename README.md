# Calculadora-de-IMC-em-Java-Script-
Uma calculadora simples de Índice de Massa Corporal (IMC) em uma página da web.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>IMC Calculator</title>
</head>
<body>
    <h1>IMC Calculator</h1>
    <label for="weight">Weight (kg):</label>
    <input type="number" id="weight">
    <br>
    <label for="height">Height (m):</label>
    <input type="number" id="height">
    <br>
    <button onclick="calculateBMI()">Calculate</button>
    <p id="result"></p>

    <script>
        function calculateBMI() {
            const weight = parseFloat(document.getElementById('weight').value);
            const height = parseFloat(document.getElementById('height').value);
            const bmi = weight / (height * height);
            document.getElementById('result').innerText = `Your BMI is ${bmi.toFixed(2)}`;
        }
    </script>
</body>
</html>
