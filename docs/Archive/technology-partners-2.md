---
title: Technology Partners
excerpt: Learn about CleverTap's third-party integration
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

    /* Hover effect on partner tile */
    .partner-tile:hover {
      transform: scale(1.05); /* Slightly enlarge on hover */
      box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2); /* Increase shadow on hover */
    }
    
    .partner-logo {
      max-width: 120px;
      height: auto;
      margin-bottom: 15px;
    }

    /* Always apply hover styles to the link */
    .partner-link {
      color: #0073e6; /* Always show blue color for links */
      /*text-decoration: none; /* Always underlined */
      /*text-shadow: 0 0 6px rgba(0, 115, 230, 0.6); /* Always apply glow effect */
      font-size: 1.1rem;
      font-weight: normal;
      transition: transform 0.2s ease, color 0.2s ease, text-decoration 0.2s ease;
      transform: scale(1.05); /* Always slightly enlarged */
    }

    /* Dark mode styles */
    @media (prefers-color-scheme: dark) {
      /* Partner tile styles for dark mode */
      .partner-tile {
        background-color: transparent; /* Same transparent background */
        border: 3px solid #0F2C47;
      }

      /* Link color for dark mode */
      .partner-link {
        color: #1E90FF; /* Lighter blue for dark mode */
       /*text-shadow: 0 0 8px rgba(255, 255, 255, 0.7); /* Brighter glow in dark mode */
      }
    }
  </style>
</head>
<body>
  <div class="partner-section">
    <!-- Partner 1 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/23fd665782166f4d600186f115087220302698acf45fdae629e2be83590a3ae5-FB.png" alt="Facebook Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/facebook-audience-network-1" target="_blank" rel="noopener noreferrer">Facebook Audience Network</a></p>
    </div>
    <!-- Partner 2 -->
    <div class="partner-tile">
      <img src="https://readme-server.com/images/actionable-logo.png" alt="Actionable Logo" class="partner-logo">
      <p><a class="partner-link" href="https://docs.actionable.me" target="_blank" rel="noopener noreferrer">Actionable.me Documentation</a></p>
    </div>
    <!-- Partner 3 -->
    <div class="partner-tile">
      <img src="https://readme-server.com/images/actioniq-logo.png" alt="ActionIQ Logo" class="partner-logo">
      <p><a class="partner-link" href="https://docs.actioniq.com" target="_blank" rel="noopener noreferrer">ActionIQ Documentation</a></p>
    </div>
    <!-- Partner 4 -->
    <div class="partner-tile">
      <img src="https://readme-server.com/images/ada-logo.png" alt="Ada Logo" class="partner-logo">
      <p><a class="partner-link" href="https://docs.ada.com" target="_blank" rel="noopener noreferrer">Ada Documentation</a></p>
    </div>
    <!-- Partner 5 -->
    <div class="partner-tile">
      <img src="https://readme-server.com/images/adjust-logo.png" alt="Adjust Logo" class="partner-logo">
      <p><a class="partner-link" href="https://docs.adjust.com" target="_blank" rel="noopener noreferrer">Adjust Documentation</a></p>
    </div>
    <!-- Partner 6 -->
    <div class="partner-tile">
      <img src="https://readme-server.com/images/airbridge-logo.png" alt="Airbridge Logo" class="partner-logo">
      <p><a class="partner-link" href="https://docs.airbridge.io" target="_blank" rel="noopener noreferrer">Airbridge Documentation</a></p>
    </div>

   <!-- Partner 7 -->
    <div class="partner-tile">
      <img src="https://readme-server.com/images/airbridge-logo.png" alt="Airbridge Logo" class="partner-logo">
      <p><a class="partner-link" href="https://docs.airbridge.io" target="_blank" rel="noopener noreferrer">Airbridge Documentation</a></p>
    </div>
 
   <!-- Partner 8 -->
    <div class="partner-tile">
      <img src="https://readme-server.com/images/airbridge-logo.png" alt="Airbridge Logo" class="partner-logo">
      <p><a class="partner-link" href="https://docs.airbridge.io" target="_blank" rel="noopener noreferrer">Airbridge Documentation</a></p>
    </div>
  
   <!-- Partner 9 -->
    <div class="partner-tile">
      <img src="https://readme-server.com/images/airbridge-logo.png" alt="Airbridge Logo" class="partner-logo">
      <p><a class="partner-link" href="https://docs.airbridge.io" target="_blank" rel="noopener noreferrer">Airbridge Documentation</a></p>
    </div>
  </div>
</body>
</html>
`}</HTMLBlock>
