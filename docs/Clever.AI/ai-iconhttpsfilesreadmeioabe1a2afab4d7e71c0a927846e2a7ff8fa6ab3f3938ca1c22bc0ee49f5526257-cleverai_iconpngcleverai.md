---
title: Clever.AI
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CleverTap Partner Guide</title>
  <style>
    /* Scoped styles for the partner tiles */
    .partner-section {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      padding: 40px;
      max-width: 1200px;
      margin: 0 auto;
    }

    .partner-tile {
      text-align: center;
      padding: 20px;
      border-radius: 8px;
      background-color: transparent; /* Transparent for both light and dark modes */
      border: 1px solid #0F2C47;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      transition: transform 0.2s ease, box-shadow 0.2s ease, background-color 0.2s ease, border-color 0.2s ease;
    }

    .partner-tile:hover {
      transform: scale(1.05); /* Slightly enlarge on hover */
      box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2); /* Increase shadow on hover */
    }
    
    .partner-logo {
      max-width: 80px;
      height: auto;
      margin-bottom: 15px;
    }

    .partner-link {
      color: #0073e6; /* Always show blue color for links */
      font-size: 1.1rem;
      font-weight: normal;
      transition: transform 0.2s ease, color 0.2s ease, text-decoration 0.2s ease;
      transform: scale(1.05); /* Always slightly enlarged */
    }

    /* Dark mode styles */
    @media (prefers-color-scheme: dark) {
      .partner-tile {
        background-color: transparent; /* Same transparent background */
        border: 3px solid #0F2C47;
      }

      .partner-link {
        color: #1E90FF; /* Lighter blue for dark mode */
      }
    }

    /* Responsive grid for tablets */
    @media (max-width: 768px) {
      .partner-section {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    /* Responsive grid for mobile phones */
    @media (max-width: 480px) {
      .partner-section {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <div class="partner-section">
   
    <!-- Partner 1 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/9435c2787127d52d2c2662c3806e18e99ce2dae51766cfb1a5f3ad2f5f7ffff4-Ask_Icon.png" alt="AppsFlyer Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/ask" target="_blank" rel="noopener noreferrer">CleverTap Ask AI</a></p>
    </div>
    <!-- Partner 2 -->
    <div class="partner-tile">
      <img src="" alt="Predictions Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/predictions" target="_blank" rel="noopener noreferrer">Predictions </a></p>
    </div>
     <!-- Partner 3 -->
    <div class="partner-tile">
      <img src="" alt="Recommendations Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/recommendations" target="_blank" rel="noopener noreferrer">Recommendations</a></p>
    </div>
     <!-- Partner 4 -->
    <div class="partner-tile">
      <img src="" alt="Scribe Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/scribe" target="_blank" rel="noopener noreferrer">Scribe</a></p>
  </div>
</body>
</html>
`}</HTMLBlock>
