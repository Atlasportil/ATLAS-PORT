# ATLAS-PORT
<!DOCTYPE html>
<html>
<head>
    <title>Shipping Cost Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f7f7f7;
            padding: 20px;
        }
        .container {
            background-color: #ffffff;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            max-width: 500px;
            margin: auto;
        }
        img {
            max-width: 100px;
            margin-bottom: 20px;
        }
        input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        button {
            background-color: #ff0000;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #e00000;
        }
        #cost {
            font-size: 20px;
            margin-top: 20px;
        }
    </style>
    <script type="text/javascript">
        function calculateCost() {
            var length = document.getElementById('length').value;
            var width = document.getElementById('width').value;
            var height = document.getElementById('height').value;
            var volume = length * width * height;
            var cost = volume * 1250;

            // Format the cost with commas
            var formattedCost = new Intl.NumberFormat().format(cost);

            document.getElementById('cost').innerText = 'Cost: ₪ ' + formattedCost;
        }
    </script>
</head>
<body>
    <div class="container">
        <img src="A0F88220-1BB8-4E65-8AFE-0204BB44FBC9.jpeg" alt="Company Logo">
        <h1>Shipping Cost Calculator</h1>
        <label for="length">Length (meters):</label>
        <input type="number" id="length"><br><br>
        <label for="width">Width (meters):</label>
        <input type="number" id="width"><br><br>
        <label for="height">Height (meters):</label>
        <input type="number" id="height"><br><br>
        <button onclick="calculateCost()">احسب</button>
        <p id="cost">Cost: ₪</p>
    </div>
</body>
</html>
