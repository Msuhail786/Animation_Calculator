<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Animated Calculator</title>
  <style>
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      background: linear-gradient(135deg, #667eea, #764ba2);
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      animation: fadeIn 1.5s ease-in;
    }
    .calculator {
      background: #fff;
      border-radius: 20px;
      padding: 20px;
      box-shadow: 0 15px 25px rgba(0,0,0,0.3);
      transition: transform 0.3s ease;
      animation: slideUp 1s ease-out;
    }
    .calculator:hover {
      transform: scale(1.03);
    }
    .display {
      width: 100%;
      height: 60px;
      background: #222;
      color: #0f0;
      font-size: 2rem;
      border-radius: 10px;
      margin-bottom: 15px;
      text-align: right;
      padding: 10px;
      box-sizing: border-box;
      overflow-x: auto;
    }
    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 10px;
    }
    button {
      font-size: 1.5rem;
      padding: 20px;
      border: none;
      border-radius: 10px;
      background: #f0f0f0;
      cursor: pointer;
      transition: background 0.3s, transform 0.1s;
    }
    button:active {
      transform: scale(0.95);
    }
    button:hover {
      background: #ddd;
    }
    .equal {
      background: #667eea;
      color: white;
    }
    .operator {
      background: #764ba2;
      color: white;
    }
    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }
    @keyframes slideUp {
      from {
        transform: translateY(50px);
        opacity: 0;
      }
      to {
        transform: translateY(0);
        opacity: 1;
      }
    }
  </style>
</head>
<body>
<div class="calculator">
  <div class="display" id="display">0</div>
  <div class="buttons">
    <button onclick="clearDisplay()">C</button>
    <button onclick="append('/')">/</button>
    <button onclick="append('*')">*</button>
    <button onclick="backspace()">←</button>
    <button onclick="append('7')">7</button>
    <button onclick="append('8')">8</button>
    <button onclick="append('9')">9</button>
    <button class="operator" onclick="append('-')">-</button>
    <button onclick="append('4')">4</button>
    <button onclick="append('5')">5</button>
    <button onclick="append('6')">6</button>
    <button class="operator" onclick="append('+')">+</button>
    <button onclick="append('1')">1</button>
    <button onclick="append('2')">2</button>
    <button onclick="append('3')">3</button>
    <button class="equal" onclick="calculate()">=</button>
    <button onclick="append('0')">0</button>
    <button onclick="append('.')">.</button>
  </div>
</div>
<script>
  const display = document.getElementById('display');
  function append(value) {
    if (display.textContent === '0') {
      display.textContent = value;
    } else {
      display.textContent += value;
    }
  }
  function clearDisplay() {
    display.textContent = '0';
  }
  function backspace() {
    display.textContent = display.textContent.slice(0, -1) || '0';
  }
  function calculate() {
    try {
      display.textContent = eval(display.textContent);
    } catch {
      display.textContent = 'Error';
    }
  }
</script>

</body>
</html>
