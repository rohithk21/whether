<!DOCTYPE html>
<html>
<head>
    <title>Temperature Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .converter {
            max-width: 300px;
            margin: 0 auto;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="converter">
        <h1>Temperature Converter</h1>
        <label for="celsius">Celsius:</label>
        <input type="number" id="celsius" placeholder="Enter Celsius" oninput="convertTemperature()">
        <br><br>
        <label for="fahrenheit">Fahrenheit:</label>
        <span id="fahrenheitValue"></span>
        <br><br>
        <label for="kelvin">Kelvin:</label>
        <span id="kelvinValue"></span>
    </div>

    <script>
        function convertTemperature() {
            const celsiusInput = document.getElementById("celsius").value;
            const fahrenheit = (celsiusInput * 9/5) + 32;
            const kelvin = parseFloat(celsiusInput) + 273.15;

            document.getElementById("fahrenheitValue").textContent = fahrenheit.toFixed(2) + " °F";
            document.getElementById("kelvinValue").textContent = kelvin.toFixed(2) + " K";
        }
    </script>
</body>
</html>
