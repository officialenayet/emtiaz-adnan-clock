<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Emtiyaz Adnan - Age Clock</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #f9f9f9;
      color: #222;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      text-align: center;
      margin: 0;
    }
    h1 {
      font-size: 2.5rem;
      color: #4b8df8;
      margin-bottom: 0.5rem;
    }
    .age {
      font-size: 1.5rem;
      font-weight: 500;
      color: #333;
    }
    .time {
      margin-top: 0.5rem;
      font-size: 1.25rem;
      color: #777;
    }
  </style>
</head>
<body>
  <h1>Emtiyaz Adnan</h1>
  <div class="age" id="ageText">Loading...</div>
  <div class="time" id="liveTime">--</div>

  <script>
    const birthDate = new Date("2025-06-20T00:00:00");

    function updateAge() {
      const now = new Date();
      let diff = now - birthDate;

      const years = now.getFullYear() - birthDate.getFullYear();
      const months = now.getMonth() - birthDate.getMonth() + (now.getDate() < birthDate.getDate() ? -1 : 0);
      const days = Math.floor((now - new Date(now.getFullYear(), now.getMonth(), birthDate.getDate())) / (1000 * 60 * 60 * 24));

      let total = now - birthDate;
      const tDays = Math.floor(total / (1000 * 60 * 60 * 24));
      total -= tDays * (1000 * 60 * 60 * 24);
      const hours = Math.floor(total / (1000 * 60 * 60));
      total -= hours * (1000 * 60 * 60);
      const minutes = Math.floor(total / (1000 * 60));
      total -= minutes * (1000 * 60);
      const seconds = Math.floor(total / 1000);

      document.getElementById("ageText").textContent =
        `${tDays + 1} days (${years}y ${months >= 0 ? months : months + 12}m ${days}d)`;

      document.getElementById("liveTime").textContent =
        `${hours} hours, ${minutes} minutes, ${seconds} seconds`;
    }

    updateAge();
    setInterval(updateAge, 1000);
  </script>
</body>
</html>
