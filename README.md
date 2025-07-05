<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Student Mobile Viewer</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #111;
      color: #fff;
      text-align: center;
      padding: 2rem;
    }
    input, button {
      padding: 10px;
      font-size: 16px;
      margin: 10px;
    }
    button {
      background: #00ffcc;
      border: none;
      cursor: pointer;
    }
    .result-box {
      margin-top: 20px;
      padding: 20px;
      background: #222;
      display: none;
      border: 1px solid #555;
    }
  </style>
</head>
<body>
  <h1>📱 Student Contact Viewer</h1>
  <p>Enter Student Name:</p>
  <input type="text" id="nameInput" placeholder="e.g. Tanisha">
  <button onclick="showNumber()">Show Number</button>  <div class="result-box" id="resultBox">
    <h2>Student: <span id="studentName"></span></h2>
    <p><strong>📞 Mobile Number:</strong> <span id="mobileNumber"></span></p>
  </div>  <script>
    // Student contact list
    const contacts = {
      "Tanisha": "01816344886",
      "Titi": "01704470145",
      "Marium": "01836802304",
      "Faria": "01890755262",
      "Amina": "01816271499",
      "Rida": "01862911568",
      "Nava": "01814874823",
      "Rimi": "01817082695",
      "Afla": "01821035002",
      "Joi": "0819417198",
      "Soha": "01711504436",
      "Jomo": "01811902197",
      "Asifa": "01325548872",
      "Eti": "01708111245",
      "Esrat": "01733949580",
      "Mim": "01306877994",
      "Nisa": "01889499838",
      "Kadiza": "01716074745",
      "Sabiha": "01611716679",
      "Rani": "01724600398",
      "Mehazabin": "01828150069"
    };

    function showNumber() {
      const name = document.getElementById("nameInput").value.trim();
      const number = contacts[name];
      const resultBox = document.getElementById("resultBox");

      if (number) {
        document.getElementById("studentName").innerText = name;
        document.getElementById("mobileNumber").innerText = number;
        resultBox.style.display = "block";
      } else {
        alert("❌ No contact found for this name.");
        resultBox.style.display = "none";
      }
    }
  </script></body>
</html>
