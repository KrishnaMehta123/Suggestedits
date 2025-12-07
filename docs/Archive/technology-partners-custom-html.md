---
title: Technology Partners - No
excerpt: Learn about CleverTap's third-party integration
deprecated: true
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
    <title>Interactive Tiles</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css"> <!-- Font Awesome Icons -->
    <style>
        /* Base Styling */
        .tile-container {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f4f4f4; /* Light background */
            color: #333; /* Dark text */
            border-radius: 8px; /* Round corners */
            box-sizing: border-box;
            max-width: 1200px;
            margin-left: auto;
            margin-right: auto;
        }

        /* Tile layout and responsiveness */
        .tile-container .container {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
            padding: 10px;
        }

        .tile-container .tile {
            width: calc(33.33% - 20px); /* 3 columns in larger screens */
            background: rgba(255, 255, 255, 0.8);
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: left;
            cursor: pointer;
            position: relative;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
        }

        .tile-container .tile:hover {
            transform: translateY(-10px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
        }

        .tile-container .tile h3 {
            font-size: 18px;
            margin: 10px 0;
            font-weight: bold;
            margin-left: 40px; /* Space to the right of the icon */
        }

        .tile-container .tile a {
            text-decoration: none;
            color: #007bff;
            display: block;
            margin: 5px 0;
            font-size: 16px;
        }

        .tile-container .tile a:hover {
            text-decoration: underline;
        }

        .tile-container .tile-content {
            display: none;
        }

        .tile-container .tile:hover .tile-content {
            display: block;
        }

        /* Dark Mode Styling */
        @media (prefers-color-scheme: dark) {
            .tile-container {
                background-color: #f4f4f4; /* Light background for dark mode */
                color: #333; /* Dark text for dark mode */
            }

            .tile-container .tile {
                background: rgba(255, 255, 255, 0.8); /* Light tile background */
                color: #333;
            }

            .tile-container .tile a {
                color: #66aaff;
            }

            .tile-container .tile a:hover {
                color: #bbd4ff;
                text-decoration: underline;
            }
        }

        /* Responsive styling for mobile screens */
        @media (max-width: 768px) {
            .tile-container .tile {
                width: calc(50% - 20px); /* 2 columns on medium screens */
            }
        }

        @media (max-width: 480px) {
            .tile-container .tile {
                width: 100%; /* Single column on smaller screens */
            }
        }

        /* Icon Styling */
        .tile-container .tile i {
            font-size: 32px;
            color: #007bff;
            position: absolute;
            left: 20px;
            top: 10px;
        }
    </style>
</head>
<body>

    <div class="tile-container">
        <div class="container">
            <div class="tile" data-category="Category 1">
                <i class="fas fa-cogs"></i> <!-- Sample Icon -->
                <h3>Category 1</h3>
                <div class="tile-content">
                    <a href="#">Link 1A</a>
                    <a href="#">Link 1B</a>
                </div>
            </div>
            <div class="tile" data-category="Category 2">
                <i class="fas fa-bell"></i> <!-- Sample Icon -->
                <h3>Category 2</h3>
                <div class="tile-content">
                    <a href="#">Link 2A</a>
                    <a href="#">Link 2B</a>
                </div>
            </div>
            <div class="tile" data-category="Category 3">
                <i class="fas fa-chart-line"></i> <!-- Sample Icon -->
                <h3>Category 3</h3>
                <div class="tile-content">
                    <a href="#">Link 3A</a>
                    <a href="#">Link 3B</a>
                </div>
            </div>
            <!-- Repeat for other categories -->
        </div>
    </div>

</body>
</html>
`}</HTMLBlock>

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Partner Guide</title>
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@700&display=swap" rel="stylesheet"> <!-- Added Google Font -->
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 0;
      padding: 20px;
      background-color: #f7f7f7;
    }
    .container {
      max-width: 1200px;
      margin: 0 auto;
    }
    .two-col-container {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 20px;
    }
    .link-content {
      background-color: rgba(255, 255, 255, 0.9); /* Semi-transparent background */
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease;
      max-height: 250px;
      overflow: hidden; /* Hide links initially */
      position: relative; /* Necessary for positioning the hover content */
    }
    .link-content:hover {
      transform: translateY(-5px); /* Elevate tile on hover */
    }
    .custom-heading {
      font-family: 'Montserrat', sans-serif; /* Use a stylish font */
      font-size: 1.3em; /* Increased font size */
      font-weight: 700; /* Make font bold */
      color: #333; /* Darker color for better visibility */
      display: flex;
      align-items: center;
      justify-content: flex-start; /* Align content to the left */
      padding: 10px 15px;
      border-radius: 8px; /* Rounded corners for a softer look */
      margin-bottom: 10px; /* Margin between heading and content */
      transition: background-color 0.3s ease; /* Smooth transition effect */
    }
    .custom-heading:hover {
      background-color: #e0e0e0; /* Light background change on hover for interactivity */
    }
    .custom-heading i {
      margin-right: 15px; /* More space between icon and text */
      font-size: 1.6em; /* Slightly larger icon */
      color: #007bff; /* Icon color to make it stand out */
    }
    .links {
      display: none; /* Hide links initially */
      font-size: 1em;
      color: #007bff;
      text-decoration: none;
      margin-bottom: 8px;
      transition: color 0.3s ease;
    }
    .links:hover {
      text-decoration: underline;
      color: #0056b3;
    }
    /* Show links when hovering over the parent link-content */
    .link-content:hover .links {
      display: block;
    }
    /* Style to display multiple links */
    .links-container {
      display: flex;
      flex-direction: column;
    }
  </style>
</head>
<body>

  <div class="container">
    <div class="two-col-container">
      <div class="link-content">
        <h4 class="custom-heading"><i class="fas fa-database"></i> Data and Infrastructure</h4>
        <div class="links-container">
          <p class="links"><a href="#">CDPs</a></p>
          <p class="links"><a href="#">Analytics</a></p>
          <p class="links"><a href="#">Data warehouses</a></p>
          <p class="links"><a href="#">Automation</a></p>
          <p class="links"><a href="#">Support</a></p>
          <p class="links"><a href="#">Experimentation partners</a></p>
        </div>
      </div>
      <div class="link-content">
        <h4 class="custom-heading"><i class="fas fa-comments"></i> Message Orchestration</h4>
        <div class="links-container">
          <p class="links"><a href="#">Attribution</a></p>
          <p class="links"><a href="#">Loyalty</a></p>
          <p class="links"><a href="#">E-commerce</a></p>
          <p class="links"><a href="#">Surveys</a></p>
          <p class="links"><a href="#">Learning partners</a></p>
        </div>
      </div>
      <div class="link-content">
        <h4 class="custom-heading"><i class="fas fa-cogs"></i> Personalization</h4>
        <div class="links-container">
          <p class="links"><a href="#">Dynamic content</a></p>
          <p class="links"><a href="#">Location</a></p>
          <p class="links"><a href="#">Localization</a></p>
        </div>
      </div>
      <div class="link-content">
        <h4 class="custom-heading"><i class="fas fa-envelope"></i> Email</h4>
        <div class="links-container">
          <p class="links"><a href="#">Email providers</a></p>
          <p class="links"><a href="#">Technology partners</a></p>
        </div>
      </div>
      <div class="link-content">
        <h4 class="custom-heading"><i class="fas fa-sms"></i> SMS Providers</h4>
        <div class="links-container">
          <p class="links"><a href="#">SMS providers</a></p>
        </div>
      </div>
      <div class="link-content">
        <h4 class="custom-heading"><i class="fab fa-whatsapp"></i> WhatsApp Providers</h4>
        <div class="links-container">
          <p class="links"><a href="#">WhatsApp providers</a></p>
          <p class="links"><a href="#">Technology partners</a></p>
        </div>
      </div>
    </div>
  </div>

</body>
</html>
`}</HTMLBlock>
