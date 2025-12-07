---
title: Partner Landing page - Shreyans
excerpt: ''
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
    <title>Integration Grid</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
    <a href="https://www.google.com/?client=safari">      <!-- change the link here for re-directing -->
        <div class="integration-card">
            <div class="logo-container">
                <img src="https://files.readme.io/93bb344627f1bd8a4d187ff5ebc1da06604fb3a7805ea6fdae208089fb6c5b6b-Airbnb_Symbol_0.svg" alt="Adjust" class="logo"> <!-- change the link for the logo -->
            </div>
            <div class="content">
                <div class="name">Adjust</div>
                <div class="category">Attribution</div>
            </div>
        </div>
      </a>
  
      
      
        <div class="integration-card">
            <div class="logo-container">
                <img src="https://files.readme.io/487110869d01e0f2e506e9748d03217555ba50b6fc30f24fcd22ceeee65047a4-Adjust_idZed2gUTA_0.svg" alt="Airbridge" class="logo">
            </div>
            <div class="content">
                <div class="name">Airbridge</div>
                <div class="category">Attribution</div>
            </div>
        </div>
      
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Amazon EventBridge" class="logo">
            </div>
            <div class="content">
                <div class="name">Amazon EventBridge</div>
                <div class="category">Analytics</div>
            </div>
        </div>
      
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Amazon S3" class="logo">
            </div>
            <div class="content">
                <div class="name">Amazon S3</div>
                <div class="category">Cloud storage</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Amplitude" class="logo">
            </div>
            <div class="content">
                <div class="name">Amplitude</div>
                <div class="category">Analytics</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Apps Flyer" class="logo">
            </div>
            <div class="content">
                <div class="name">Apps Flyer</div>
                <div class="category">Attribution</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="AppTrove" class="logo">
            </div>
            <div class="content">
                <div class="name">AppTrove</div>
                <div class="category">Attribution</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Branch" class="logo">
            </div>
            <div class="content">
                <div class="name">Branch</div>
                <div class="category">Attribution</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="CleverTap" class="logo">
            </div>
            <div class="content">
                <div class="name">CleverTap</div>
                <div class="category">Attribution</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Google Cloud" class="logo">
            </div>
            <div class="content">
                <div class="name">Google Cloud</div>
                <div class="category">Cloud storage</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Microsoft Azure" class="logo">
            </div>
            <div class="content">
                <div class="name">Microsoft Azure</div>
                <div class="category">Cloud storage</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Mixpanel" class="logo">
            </div>
            <div class="content">
                <div class="name">Mixpanel</div>
                <div class="category">Analytics</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="mParticle" class="logo">
            </div>
            <div class="content">
                <div class="name">mParticle</div>
                <div class="category">Customer data platform</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Segment" class="logo">
            </div>
            <div class="content">
                <div class="name">Segment</div>
                <div class="category">Customer data platform</div>
            </div>
        </div>
        <div class="integration-card">
            <div class="logo-container">
                <img src="/Users/shreyans_satpute/Desktop/images.jpeg" alt="Singular" class="logo">
            </div>
            <div class="content">
                <div class="name">Singular</div>
                <div class="category">Attribution</div>
            </div>
        </div>
    </div>
</body>
</html>
`}</HTMLBlock>

<br />

# Attribution

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
    <a href="https://www.google.com/?client=safari">      <!-- change the link here for re-directing -->
        <div class="integration-card">
            <div class="logo-container">
                <img src="https://files.readme.io/93bb344627f1bd8a4d187ff5ebc1da06604fb3a7805ea6fdae208089fb6c5b6b-Airbnb_Symbol_0.svg" alt="Adjust" class="logo"> <!-- change the link for the logo -->
            </div>
            <div class="content">
                <div class="name">Adjust</div>
                <div class="category">Attribution</div>
            </div>
        </div>
      </a>
      <a href="https://www.google.com/?client=safari">      <!-- change the link here for re-directing -->
        <div class="integration-card">
            <div class="logo-container">
                <img src="https://files.readme.io/93bb344627f1bd8a4d187ff5ebc1da06604fb3a7805ea6fdae208089fb6c5b6b-Airbnb_Symbol_0.svg" alt="Adjust" class="logo"> <!-- change the link for the logo -->
            </div>
            <div class="content">
                <div class="name">Adjust</div>
                <div class="category">Attribution</div>
            </div>
        </div>
      </a>
  </div>
</body>
</html>
`}</HTMLBlock>

<br />

# Analytics

<br />

<HTMLBlock>{`
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Integration Grid</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

       .content-toc.grid-25{
      	display:None;
      }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
       

        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(350px, 1fr)); /* made the value 350px to make grid 3x3 */
            gap: 1rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .integration-card { /* styling for the cards */
            display: flex;
            align-items: center;
            padding: 1.5rem;
            #background: #F5F5F5;
          	background: white;
            border-radius: 12px;
          	min-width:200px;
            border: 1px solid rgba(0, 0, 0, 0.1);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }

        .integration-card:hover {
            
            box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
           
        }

        .logo-container {
            display: flex;
            align-items: center;
            padding-right: 1rem;
            border-right: 1px solid rgba(0, 0, 0, 0.1);
            margin-right: 1rem;
            height: 100%;
        }

        .logo { /* logo sizing */
            width: 50px;
            height: 50px;
            object-fit:fill;
            flex-shrink: 0;
            border-radius: 5px;
        }

        .content {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            min-width: 0;
            height: 100%;
        }

        .name {
            font-size: 1rem;
            font-weight: 500;
            color: #000;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            margin-bottom: 0.5rem;
        }

        .category {
            font-size: 0.8rem;
            color: #92969f;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

       
/* responsive elements */
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
        }
    

        @media (max-width: 480px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="grid">
      <!-- use this card below for replication and change the link to the desired one -->
    <a href="https://www.google.com/?client=safari">      <!-- change the link here for re-directing -->
        <div class="integration-card">
            <div class="logo-container">
                <img src="https://files.readme.io/93bb344627f1bd8a4d187ff5ebc1da06604fb3a7805ea6fdae208089fb6c5b6b-Airbnb_Symbol_0.svg" alt="Adjust" class="logo"> <!-- change the link for the logo -->
            </div>
            <div class="content">
                <div class="name">Adjust</div>
                <div class="category">Attribution</div>
            </div>
        </div>
      </a>
      <a href="https://www.google.com/?client=safari">      <!-- change the link here for re-directing -->
        <div class="integration-card">
            <div class="logo-container">
                <img src="https://files.readme.io/93bb344627f1bd8a4d187ff5ebc1da06604fb3a7805ea6fdae208089fb6c5b6b-Airbnb_Symbol_0.svg" alt="Adjust" class="logo"> <!-- change the link for the logo -->
            </div>
            <div class="content">
                <div class="name">Adjust</div>
                <div class="category">Attribution</div>
            </div>
        </div>
      </a>
  </div>
</body>
</html>
`}</HTMLBlock>
