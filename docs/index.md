<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>All In Technologies - Coming Soon</title>
<!-- Google Fonts for a modern look -->
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet" />
<style>
  body {
    margin: 0;
    padding: 0;
    font-family: 'Montserrat', sans-serif;
    background-color: #000;
    color: #fff;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
    align-items: center;
    justify-content: center;
    text-align: center;
  }

  /* Logo styling with actual image */
  .logo-container {
    margin-bottom: 30px;
  }

  .logo-container img {
    max-width: 250px;
    width: 100%;
    height: auto;
    display: block;
  }

  /* Mission statement styling */
  .mission {
    font-size: 1.5em;
    margin-bottom: 40px;
    padding: 0 20px;
    max-width: 800px;
    line-height: 1.4;
  }

  /* Coming Soon text with animation */
  .coming-soon {
    font-size: 2.5em;
    font-weight: 700;
    letter-spacing: 2px;
    margin-bottom: 20px;
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.6; }
  }

  /* Optional: Add a subtle footer or subscribe placeholder */
  .footer {
    margin-top: 40px;
    font-size: 1em;
    opacity: 0.7;
  }

  /* Responsive adjustments */
  @media(max-width: 600px) {
    .logo-container img {
      max-width: 150px;
    }
    .mission {
      font-size: 1.2em;
    }
    .coming-soon {
      font-size: 2em;
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

<!-- Coming Soon Message -->
<div class="coming-soon">
  Coming Soon
</div>

<!-- Optional Footer -->
<div class="footer">
  Stay tuned for updates!
</div>

</body>
</html>
