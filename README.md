<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Counter App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        .container {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        button {
            padding: 10px 20px;
            margin: 5px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
        }
        .increase { background: green; color: white; }
        .decrease { background: red; color: white; }
        .reset { background: gray; color: white; }
        #counter {
            font-size: 24px;
            margin: 20px 0;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Counter App</h2>
        <p id="counter">0</p>
        <button class="increase" onclick="increaseCounter()">Increase</button>
        <button class="decrease" onclick="decreaseCounter()">Decrease</button>
        <button class="reset" onclick="resetCounter()">Reset</button>
    </div><script>
    let count = 0;
    function updateCounter() {
        document.getElementById('counter').innerText = count;
    }
    function increaseCounter() {
        count++;
        updateCounter();
    }
    function decreaseCounter() {
        count--;
        updateCounter();
    }
    function resetCounter() {
        count = 0;
        updateCounter();
    }
</script>

</body>
</html>
