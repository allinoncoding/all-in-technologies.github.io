<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>All In Technologies - Coming Soon</title>
<!-- Google Fonts for a modern, clean look -->
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet" />
<style>
  /* Reset and base styles */
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: 'Montserrat', sans-serif;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: #fff;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    align-items: center;
    justify-content: center;
    padding: 20px;
    text-align: center;
  }

  /* Logo styling */
  .logo-container {
    margin-bottom: 30px;
  }
  .logo-container img {
    max-width: 300px;
    width: 100%;
    height: auto;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    cursor: pointer;
  }
  /* Enlarge on hover for interactivity */
  .logo-container img:hover {
    transform: scale(1.1);
    box-shadow: 0 10px 30px rgba(0,0,0,0.3);
  }

  /* Mission statement styling */
  .mission {
    font-size: 1.5em;
    margin-bottom: 40px;
    padding: 0 20px;
    max-width: 800px;
    line-height: 1.4;
  }

  /* "Coming Soon" with pulsing animation */
  .coming-soon {
    font-size: 3em;
    font-weight: 700;
    letter-spacing: 2px;
    margin-bottom: 20px;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.6; }
  }

  /* Countdown timer styling */
  .countdown {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-bottom: 40px;
    font-size: 2em;
    font-weight: 700;
  }
  .time-box {
    background: rgba(255,255,255,0.1);
    padding: 15px 20px;
    border-radius: 8px;
    min-width: 80px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .time-number {
    font-size: 2em;
    margin-bottom: 5px;
  }

  /* Footer / subscribe placeholder */
  .footer {
    margin-top: 40px;
    font-size: 1em;
    opacity: 0.8;
  }

  /* Responsive adjustments */
  @media(max-width: 600px) {
    .logo-container img {
      max-width: 200px;
    }
    .mission {
      font-size: 1.2em;
    }
    .coming-soon {
      font-size: 2em;
    }
    .countdown {
      flex-direction: column;
      gap: 10px;
    }
  }
</style>
</head>
<body>

<!-- Logo Image -->
<div class="logo-container">
  <img src="IMG_8671.jpg" alt="All In Technologies Logo" />
</div>

<!-- Mission Statement -->
<div class="mission">
  Utilizing AI to Revolutionize Ad Effectiveness Measurement
</div>

<!-- Countdown Timer -->
<div class="countdown" id="countdown">
  <div class="time-box">
    <div class="time-number" id="days">00</div>
    <div>Days</div>
  </div>
  <div class="time-box">
    <div class="time-number" id="hours">00</div>
    <div>Hours</div>
  </div>
  <div class="time-box">
    <div class="time-number" id="minutes">00</div>
    <div>Minutes</div>
  </div>
  <div class="time-box">
    <div class="time-number" id="seconds">00</div>
    <div>Seconds</div>
  </div>
</div>

<!-- Coming Soon Message with animation -->
<div class="coming-soon">
  Coming Soon
</div>

<!-- Optional footer or subscription call-to-action -->
<div class="footer">
  Stay tuned for updates and exclusive insights!
</div>

<!-- Scripts for countdown -->
<script>
  // Set your launch date here (e.g., 30 days from now)
  const launchDate = new Date().getTime() + (30 * 24 * 60 * 60 * 1000); // 30 days from now

  const countdown = document.getElementById('countdown');

  const daysSpan = document.getElementById('days');
  const hoursSpan = document.getElementById('hours');
  const minutesSpan = document.getElementById('minutes');
  const secondsSpan = document.getElementById('seconds');

  function updateCountdown() {
    const now = new Date().getTime();
    const distance = launchDate - now;

    if (distance < 0) {
      countdown.innerHTML = "<div style='font-size:2em;'>We're Live Soon!</div>";
      clearInterval(timer);
      return;
    }

    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((distance % (1000 * 60)) / 1000);

    daysSpan.innerText = String(days).padStart(2, '0');
    hoursSpan.innerText = String(hours).padStart(2, '0');
    minutesSpan.innerText = String(minutes).padStart(2, '0');
    secondsSpan.innerText = String(seconds).padStart(2, '0');
  }

  // Update countdown every second
  const timer = setInterval(updateCountdown, 1000);
  updateCountdown();
</script>

</body>
</html>
