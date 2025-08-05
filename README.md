<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Project Management App</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: Arial, sans-serif;
      display: flex;
      height: 100vh;
      background-color: #f5f5f5;
    }

    /* Sidebar */
    .sidebar {
      width: 240px;
      background-color: #6e4cac;
      color: white;
      padding: 20px;
    }

    .sidebar h2 {
      font-size: 18px;
      margin-bottom: 20px;
    }

    .sidebar .section {
      margin-bottom: 20px;
    }

    .sidebar .section-title {
      font-weight: bold;
      margin-bottom: 5px;
    }

    .sidebar ul {
      list-style: none;
      padding-left: 10px;
    }

    .sidebar li {
      margin-bottom: 10px;
      cursor: pointer;
    }

    /* Main Content */
    .main {
      flex-grow: 1;
      padding: 20px;
      background-color: white;
      overflow-y: auto;
    }

    .top-bar {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 10px;
    }

    .calendar {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 10px;
      margin-top: 20px;
    }

    .day {
      height: 100px;
      background-color: #e9e9e9;
      border: 1px solid #ccc;
      text-align: right;
      padding: 5px;
      font-size: 14px;
    }

    .controls {
      margin-bottom: 10px;
    }

    .controls button {
      margin-right: 10px;
      padding: 6px 12px;
    }
  </style>
</head>
<body>

  <div class="sidebar">
    <h2>Suprith Gaonkar</h2>
    <div class="section">
      <div class="section-title">Channels</div>
      <ul>
        <li># general</li>
      </ul>
    </div>
    <div class="section">
      <div class="section-title">Projects</div>
      <ul>
        <li>VM Ware</li>
        <li>DC Migration</li>
      </ul>
    </div>
  </div>

  <div class="main">
    <div class="top-bar">Suprith Gaonkar / VM Ware</div>

    <div class="controls">
      <button onclick="generateCalendar()">Generate Calendar</button>
    </div>

    <div class="calendar" id="calendar"></div>
  </div>

  <script>
    function generateCalendar() {
      const calendar = document.getElementById("calendar");
      calendar.innerHTML = "";
      const startDate = 24;
      let day = startDate;
      for (let i = 0; i < 14; i++) {
        const div = document.createElement("div");
        div.className = "day";
        div.innerText = day;
        day++;
        if (day > 31) day = 1;
        calendar.appendChild(div);
      }
    }

    // Auto-generate on load
    window.onload = generateCalendar;
  </script>

</body>
</html>

