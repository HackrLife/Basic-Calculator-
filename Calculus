<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Basic Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .calculator {
            background-color: #333;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .display {
            background-color: #fff;
            border-radius: 5px;
            padding: 10px;
            margin-bottom: 10px;
            text-align: right;
            font-size: 24px;
        }
        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }
        button {
            background-color: #4CAF50;
            border: none;
            color: white;
            padding: 15px;
            text-align: center;
            text-decoration: none;
            font-size: 18px;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #45a049;
        }
        button.operator {
            background-color: #ff9800;
        }
        button.operator:hover {
            background-color: #e68a00;
        }
        button.clear {
            background-color: #f44336;
        }
        button.clear:hover {
            background-color: #da190b;
        }
        button.equals {
            background-color: #2196F3;
        }
        button.equals:hover {
            background-color: #0b7dda;
        }
    </style>
</head>
<body>
    <div class="calculator">
        <div class="display" id="display">0</div>
        <div class="buttons">
            <button onclick="clearDisplay()">C</button>
            <button onclick="appendToDisplay('7')">7</button>
            <button onclick="appendToDisplay('8')">8</button>
            <button onclick="appendToDisplay('9')">9</button>
            <button class="operator" onclick="appendToDisplay('+')">+</button>
            <button onclick="appendToDisplay('4')">4</button>
            <button onclick="appendToDisplay('5')">5</button>
            <button onclick="appendToDisplay('6')">6</button>
            <button class="operator" onclick="appendToDisplay('-')">-</button>
            <button onclick="appendToDisplay('1')">1</button>
            <button onclick="appendToDisplay('2')">2</button>
            <button onclick="appendToDisplay('3')">3</button>
            <button class="operator" onclick="appendToDisplay('*')">*</button>
            <button onclick="appendToDisplay('0')">0</button>
            <button onclick="appendToDisplay('.')">.</button>
            <button class="equals" onclick="calculate()">=</button>
            <button class="operator" onclick="appendToDisplay('/')">/</button>
        </div>
    </div>

    <script>
        let display = document.getElementById('display');
        let currentValue = '0';

        function updateDisplay() {
            display.textContent = currentValue;
        }

        function appendToDisplay(value) {
            if (currentValue === '0' && value !== '.') {
                currentValue = value;
            } else {
                currentValue += value;
            }
            updateDisplay();
        }

        function clearDisplay() {
            currentValue = '0';
            updateDisplay();
        }

        function calculate() {
            try {
                currentValue = eval(currentValue).toString();
                updateDisplay();
            } catch (error) {
                currentValue = 'Error';
                updateDisplay();
            }
        }
    </script>
</body>
</html>
