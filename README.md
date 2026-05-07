Copilot said: Certainly! Below is the code for a
Certainly! Below is the code for a simple web-based calculator using HTML, CSS, and JavaScript.
It supports basic arithmetic operations: addition, subtraction, multiplication, and division.

You can copy this, save it as calculator.html, and open it in your browser.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Simple Calculator</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f4f4f4; padding: 40px; }
    #calculator {
      background: #fff;
      padding: 20px 30px 30px 30px;
      border-radius: 10px;
      box-shadow: 0 5px 15px #999;
      max-width: 320px;
      margin: auto;
    }
    #display {
      width: 100%;
      font-size: 2em;
      margin-bottom: 14px;
      height: 48px;
      text-align: right;
      padding-right: 10px;
      border: 1px solid #aaa;
      border-radius: 5px;
      box-sizing: border-box;
      background: #eee;
    }
    .row {
      display: flex;
      margin-bottom: 10px;
    }
    button {
      flex: 1;
      font-size: 1.3em;
      margin: 2px;
      padding: 16px 0;
      border: none;
      background: #007bff;
      color: #fff;
      border-radius: 5px;
      cursor: pointer;
      transition: background 0.2s;
    }
    button:active { background: #0056b3; }
    .operator { background: #28a745; }
    .operator:active { background: #1e7e34; }
    .clear { background: #dc3545; }
    .clear:active { background: #a71d2a; }
    .equal { background: #ffc107; color: #333; }
    .equal:active { background: #b38f00; }
  </style>
</head>
<body>
  <div id="calculator">
    <input type="text" id="display" disabled>
    <div class="row">
      <button onclick="append('7')">7</button>
      <button onclick="append('8')">8</button>
      <button onclick="append('9')">9</button>
      <button class="operator" onclick="append('/')">&divide;</button>
    </div>
    <div class="row">
      <button onclick="append('4')">4</button>
      <button onclick="append('5')">5</button>
      <button onclick="append('6')">6</button>
      <button class="operator" onclick="append('*')">&times;</button>
    </div>
    <div class="row">
      <button onclick="append('1')">1</button>
      <button onclick="append('2')">2</button>
      <button onclick="append('3')">3</button>
      <button class="operator" onclick="append('-')">-</button>
    </div>
    <div class="row">
      <button onclick="append('0')">0</button>
      <button onclick="append('.')">.</button>
      <button class="equal" onclick="calculate()">=</button>
      <button class="operator" onclick="append('+')">+</button>
    </div>
    <div class="row">
      <button class="clear" style="flex:2" onclick="clearDisplay()">C</button>
      <button class="clear" style="flex:2" onclick="backspace()">&larr;</button>
    </div>
  </div>
  <script>
    function append(character) {
      const display = document.getElementById('display');
      display.value += character;
    }
    function clearDisplay() {
      document.getElementById('display').value = '';
    }
    function backspace() {
      const display = document.getElementById('display');
      display.value = display.value.slice(0, -1);
    }
    function calculate() {
      const display = document.getElementById('display');
      try {
        display.value = eval(display.value);
      } catch {
        display.value = 'Error';
      }
    }
  </script>
</body>
</html>this is to count alphabet
