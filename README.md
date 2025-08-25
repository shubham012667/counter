<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Live Character Counter</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 40px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    h2 {
      margin-bottom: 20px;
    }
    textarea {
      width: 400px;
      height: 120px;
      padding: 10px;
      font-size: 16px;
      border: 2px solid #ccc;
      border-radius: 8px;
      resize: none;
      outline: none;
      transition: border-color 0.3s;
    }
    textarea:focus {
      border-color: #4a90e2;
    }
    .counter {
      margin-top: 10px;
      font-size: 16px;
      font-weight: bold;
      color: #333;
    }
  </style>
</head>
<body>

  <h2>Live Character Counter</h2>
  <textarea id="textInput" placeholder="Type something..."></textarea>
  <div class="counter">Characters: <span id="charCount">0</span></div>

  <script>
    const textarea = document.getElementById("textInput");
    const charCount = document.getElementById("charCount");

    textarea.addEventListener("input", () => {
      charCount.textContent = textarea.value.length;
    });
  </script>

</body>
</html>
