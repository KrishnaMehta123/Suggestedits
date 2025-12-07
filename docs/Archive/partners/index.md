---
title: Partners
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
      max-width: 120px;
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
      <img src="https://files.readme.io/fcb10746ed2f856c488de6cafde7afec5867a38ea1a8ec91ee251a815d88b401-image.png" alt="AppsFlyer Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/appsflyer" target="_blank" rel="noopener noreferrer">AppsFlyer</a></p>
    </div>
     <!-- Partner 2 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/e8f57ccc1e77bd6311bef387802b8067d9b91fd4229436bc384c11177e69a762-image.png" alt="Apteligent Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/apteligent" target="_blank" rel="noopener noreferrer">Apteligent</a></p>
    </div>
    <!-- Partner 3 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/4263d4cd3d5992e8f0bd5ac32c904898b4e475025b6b4812650edaea6af59dab-image.png" alt="Branch Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/branch" target="_blank" rel="noopener noreferrer">Branch </a></p>
    </div>
     <!-- Partner 4 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/979d95f901ef31ff7cdad528c874975c3e024156f673b09bbe480617bdd4f6f3-4143903D-0DBE-4F47-838F-D28BB4455FF8_4_5005_c.jpeg" alt="Exotel Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/exotel" target="_blank" rel="noopener noreferrer">Exotel</a></p>
    </div>
    <!-- Partner 5 -->
      <div class="partner-tile">
      <img src="https://files.readme.io/23fd665782166f4d600186f115087220302698acf45fdae629e2be83590a3ae5-FB.png" alt="Facebook Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/facebook-audience-network-1" target="_blank" rel="noopener noreferrer">Facebook Audience Network</a></p>
    </div>
     <!-- Partner 6 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/47bba6f1edbd911135cdeea12f87e65e1864ae7101fc5af43badc02f3f4e2b97-image.png" alt="Mixpanel Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/mixpanel-export" target="_blank" rel="noopener noreferrer">Mixpanel (Export)</a></p>
    </div>
    <!-- Partner 7 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/47bba6f1edbd911135cdeea12f87e65e1864ae7101fc5af43badc02f3f4e2b97-image.png" alt="Mixpanel Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/mixpanel-integration" target="_blank" rel="noopener noreferrer">Mixpanel (Import)</a></p>
    </div>
    <!-- Partner 8 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/9ce16ceeb78591c60bdd59ead934f5bff3aaef6112568fb1d19c9ff9b2b48146-image.png" alt="Mandrill Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/mandrill" target="_blank" rel="noopener noreferrer">Mandrill</a></p>
    </div>

    <!-- Partner 9 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/c6676770f43da282016b1a4a6d90241ce5c5b56452fc08cc901a28e1a78cd12c-image.png" alt="Netcore Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/netcore" target="_blank" rel="noopener noreferrer">Netcore</a></p>
    </div>
    <!-- Partner 10 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/087870bdd291d76a4e50e05cc1ee2d63151e23a8c002a51a173224791c11f6e9-image.png" alt="Nexmo Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/nexmo" target="_blank" rel="noopener noreferrer">Nexmo</a></p>
    </div>
    <!-- Partner 11 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/5511c6fe72316a7769d78b141d26d481fa8f8f5e04f9cc8c1d3c6019460bb67f-image.png" alt="Plivo Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/plivo" target="_blank" rel="noopener noreferrer"> Plivo</a></p>
    </div>
     <!-- Partner 12 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/016645ed45ba760cb130a08e0d58be963e3d469e25808e772e79c48b5fa682c6-image.png" alt="PostMark Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/postmark" target="_blank" rel="noopener noreferrer">Postmark</a></p>
    </div>
    <!-- Partner 13 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/32436f92f0a6107e9541d7abcb58401167eea69b0801d5b6275cc48a2ec229d2-image.png" alt="Revenuecat Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/revenuecat" target="_blank" rel="noopener noreferrer">RevenueCat </a></p>
    </div>
    <!-- Partner 14 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/c528e963a5fe70c64bd6471517f9178eab3a643aa3c84e2a1ea022f00a5304fd-C9CF19B6-7E1C-43F8-95C9-B271CAD25969.jpeg" alt="Twilio Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/twilio" target="_blank" rel="noopener noreferrer">Twilio</a></p>
    </div>
    <!-- Partner 15 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/9fec55cfd2f6131bb361042d77ab8c2bfe9ff8a2e248ed21222e96a55ea181f0-image.png" alt="Zendesk Logo" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/zendesk" target="_blank" rel="noopener noreferrer">Zendesk </a></p>
    </div>
<!-- Partner 16 -->
<div class="partner-tile">
  <img src="https://files.readme.io/eaee1e03a2781bbf12b9f916e69eaa2f9a1fd0bd8293fb976423a71cd8582037-image.png" 
       alt="Treasure Data Integration Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/twilio" target="_blank" rel="noopener noreferrer">Treasure Data</a></p>
</div>
<!-- Partner 17 -->
<div class="partner-tile">
  <img src="https://files.readme.io/6d10752b4f1288d026b0e1864a73817487b514db39a77943c0975225d4efce8e-idPo7J6YFZ_1735814056251.png" 
       alt="Amplitude Export Integration Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/amplitude-export" target="_blank" rel="noopener noreferrer">Amplitude (Export)</a></p>
</div>
     <!-- Partner 18 -->
    <div class="partner-tile">
      <img src="https://files.readme.io/6d10752b4f1288d026b0e1864a73817487b514db39a77943c0975225d4efce8e-idPo7J6YFZ_1735814056251.png" alt="Amplitude (Import)" class="partner-logo">
      <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/amplitude-cohort-import" target="_blank" rel="noopener noreferrer"> Amplitude (Import)</a></p>
    </div>
<!-- Partner 19 -->
<div class="partner-tile">
  <img src="https://files.readme.io/fc4cc4baf4a3ddf417b0d0f44ec132fd293642e435c5a1c6f27ef7f759089df3-idFJ3xL-zK_logos.png" alt="Adjust Logo" class="partner-logo">
  <p><a class="partner-link" href="https://developer.clevertap.com/docs/adjust" target="_blank" rel="noopener noreferrer">Adjust</a></p>
</div>

<!-- Partner 20 -->
<div class="partner-tile">
  <img src="https://files.readme.io/00716ced5b580dbc845953b8d99115a0e1da67d360a0537372686a3574caa5b0-image.png" alt="Airbridge Logo" class="partner-logo">
  <p><a class="partner-link" href="https://developer.clevertap.com/docs/airbridge" target="_blank" rel="noopener noreferrer">Airbridge</a></p>
</div>

<!-- Partner 21 -->
<div class="partner-tile">
  <img src="https://files.readme.io/46681d5ff8b86649f7ce5f3aa1bda1971cf5b5642044677413709c5572f219d9-image.png" alt="Singular Logo" class="partner-logo">
  <p><a class="partner-link" href="https://developer.clevertap.com/docs/singular-apsalar" target="_blank" rel="noopener noreferrer">Singular</a></p>
</div>

<!-- Partner 22 -->
<div class="partner-tile">
  <img src="https://files.readme.io/307800535d4b2a731449c2042d3a5c575a3c07daee7f8994e4821c8454f395f8-idG07FmFHq_1735814548006.png" alt="Plot Projects Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/plot-projects" target="_blank" rel="noopener noreferrer">Plot Projects</a></p>
</div>

<!-- Partner 23 -->
<div class="partner-tile">
  <img src="https://files.readme.io/137ad2642b86e317d6fbfc77182b562752812f18feea8557b8a9de2ea1248a49-Logo.png" alt="RudderStack Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.dev.clevertap.net/docs/rudderstack" target="_blank" rel="noopener noreferrer">RudderStack</a></p>
</div>

<!-- Partner 24 -->
<div class="partner-tile">
  <img src="https://files.readme.io/5b7aa86c55252fd45afc25791b6bc5bb7e251c5579cacbcb0684baeb3a674443-Logo_1.png" alt="Segment Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.dev.clevertap.net/docs/segment" target="_blank" rel="noopener noreferrer">Segment</a></p>
</div>

<!-- Partner 25 -->
<div class="partner-tile">
  <img src="https://files.readme.io/f8fd877c5dd70fd80fa58f10a01a187003cd4afb0abbc2c610cede1a93afa624-idS5TK0MYh_1735814892868.png" alt="AWS S3 Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/data-export-to-aws-s3" target="_blank" rel="noopener noreferrer">AWS S3</a></p>
</div>

<!-- Partner 26 -->
<div class="partner-tile">
  <img src="https://files.readme.io/0bfe16c1c951ed411e999e73e2eab3ce72bdc59a62d9846bcaab5a4abfa76920-idELQUIEcj_1735815182727.png" alt="Crowdin Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging .docs.user.clevertap.net/docs/crowdin" target="_blank" rel="noopener noreferrer">Crowdin</a></p>
</div>

<!-- Partner 27 -->
<div class="partner-tile">
  <img src="https://files.readme.io/ccbcb0f06b98add8bb14b153f1ffb453964a61dbfc584372418da16e3f749dd0-idI2L9W1ED_1735815201579.png" alt="Lokalise Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/lokalise" target="_blank" rel="noopener noreferrer">Lokalise</a></p>
</div>

<!-- Partner 28 -->
<div class="partner-tile">
  <img src="https://files.readme.io/79ee0c8ba2b5d795b687e8803cd5513e19e8d646f2d8afde510802b7e211252b-id41ZGr5Lm_logos_1.png" alt="Storyly Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/storyly" target="_blank" rel="noopener noreferrer">Storyly</a></p>
</div>

<!-- Partner 29 -->
<div class="partner-tile">
  <img src="https://files.readme.io/4abd8efd9ca072cf0a0d276c800c53144eb84fcd17c075f224fb7564d82f3f08-Logo_2.png" alt="Shopify Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/shopify" target="_blank" rel="noopener noreferrer">Shopify</a></p>
</div>

<!-- Partner 30 -->
<div class="partner-tile">
  <img src="https://files.readme.io/1bcdfb2b63ea27241f4a18650972555ec77b7f1371b65e13e9e2217badd2b5ff-image.png" alt="Amazon Simple Email Service Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/amazon-simple-email-service" target="_blank" rel="noopener noreferrer">Amazon Simple Email Service</a></p>
</div>

<!-- Partner 31 -->
<div class="partner-tile">
  <img src="https://files.readme.io/4a9428170cfb37034ed8c7c4864fba6fb4bcdb7c6c2843804f5291908a62a9cd-Logo_3.png" alt="SendGrid Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/sendgrid" target="_blank" rel="noopener noreferrer">SendGrid</a></p>
</div>

<!-- Partner 32 -->
<div class="partner-tile">
  <img src="https://files.readme.io/8ac3de2b442c7329d6d3cb3ee356a6126328b60e8198b958cef81d82b4cac848-idHnfRwKrN_1735815939149.png" alt="Clearout Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/clearout" target="_blank" rel="noopener noreferrer">Clearout</a></p>
</div>

<!-- Partner 33 -->
<div class="partner-tile">
  <img src="https://files.readme.io/56cc97d3fd9741ace58f8379b71ec15501d411f4fea74e41e3c41047356ad6e8-idib7Se0EO_1735819060115.png" alt="Talon.One Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/talonone" target="_blank" rel="noopener noreferrer">Talon.One</a></p>
</div>

<!-- Partner 34 -->
<div class="partner-tile">
  <img src="https://files.readme.io/9a8f6ff1a49e7318c9a6ee661b973e6e6c91b081f09d368928 008643d32809a4-id41KDIGMl_logos.png" alt="LINE Messenger Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/line-messenger" target="_blank" rel="noopener noreferrer">LINE Messenger</a></p>
</div>

<!-- Partner 35 -->
<div class="partner-tile">
  <img src="https://files.readme.io/73acd9327faf2859ff2f59d07eb70d348e7f25514b134c8fa67e3cbf1e45ed7f-idhSgf3I1V_1735818778160.png" alt="Sendbird Business Messaging Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/sendbird-business-messaging" target="_blank" rel="noopener noreferrer">Sendbird Business Messaging</a></p>
</div>

<!-- Partner 36 -->
<div class="partner-tile">
  <img src="https://files.readme.io/9646d80f1bf012c3b1827dcfea6f5d4522fbba16626e6a8486eb8038928a11e0-image.png" alt="Google Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/google-adwords" target="_blank" rel="noopener noreferrer">Google</a></p>
</div>

<!-- Partner 37 -->
<div class="partner-tile">
  <img src="https://files.readme.io/4af1ba909bf7b670046cd63a6e52b6d2c00adb0d988355780c7226761cfe06ac-Logo_5.png" alt="TikTok Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/tiktok" target="_blank" rel="noopener noreferrer">TikTok</a></p>
</div>

<!-- Partner 38 -->
<div class="partner-tile">
  <img src="https://files.readme.io/395eda874ab55efccaef0008363eca076f747bfbfed7a59e277bc5218c7aeb0b-idAO57ZGr5_logos.png" alt="Taxi for Email Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/taxi-for-email" target="_blank" rel="noopener noreferrer">Taxi for Email</a></p>
</div>

<!-- Partner 39 -->
<div class="partner-tile">
  <img src="https://files.readme.io/58ea76e62b65b93d4dda91772e97cd36eae8f6e50c15b6c9dbd3d2ca6ee9c59d-idsFujJg_H_1735818195090.png" alt="MSG91 Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/msg91" target="_blank" rel="noopener noreferrer">MSG91</a></p>
</div>

<!-- Partner 40 -->
<div class="partner-tile">
  <img src="https://files.readme.io/6ad39e9dfcb133a77fd6f9da418bcb60a0316cb63ee94917b72aeccce92cea1c-idVFN-12JI_logos.png" alt="SMSINDIAHUB Logo" class="partner-logo">
  <p><a class="partner-link" href="https://docs.clevertap.com/docs/generic-sms" target="_blank" rel="noopener noreferrer">SMSINDIAHUB</a></p>
</div>

<!-- Partner 41 -->
<div class="partner-tile">
  <img src="https://files.readme.io/0d6a575eb519162151933942dda8a004004e1ca4fca83a749c3d247da843327b-idCMoarBF6_1735818324244.png" alt="TextLocal Logo" class="partner-logo">
  <p><a class="partner-link" href="https://docs.clevertap.com/docs/generic-sms" target="_blank" rel="noopener noreferrer">TextLocal</a></p>
</div>

<!-- Partner 42 -->
<div class="partner-tile">
  <img src="https://files.readme.io/a089ba2607c6375d642b2004b17c9934622d2c141eef2cd053af1dd96dfba4d0-iddZIe6dUF_1735818412045.png" alt="Infobip Logo" class="partner-logo">
  <p><a class="partner-link" href="https://docs.clevertap.com/docs/infobip-sms" target="_blank" rel="noopener noreferrer">Infobip</a></p>
</div>

<!-- Partner 43 -->
<div class="partner-tile">
  <img src="https://files.readme.io/c88be4a6f746d6e37d75de2456cf9f893fa9c47839c93a7b348c9ad034d05bb8-id_U5e2wf1_1735818429084.png" alt="GupShup Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/gupshup" target="_blank" rel="noopener noreferrer">GupShup</a></p>
</div>

<!-- Partner 44 -->
<div class="partner-tile">
  <img src="https://files.readme.io/745d1024bdc88924e2b890a8aff31c0c762a406bc343e133b2e6e5b767f6eead-idBMSXTqwE_logos.png" alt="Haptik Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/haptik" target="_blank" rel="noopener noreferrer">Haptik</a></p>
</div>

<!-- Partner 45 -->
<div class="partner-tile">
  <img src="https://files.readme.io/6d28a85f13a343fbb468636944ac9dbc12190df3faaf205485f0b653a12c0545-id3Fys_58M_logos.png" alt="Yellow.AI Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/yellowai" target="_blank" rel="noopener noreferrer">Yellow.AI</a></p>
</div>

<!-- Partner 46 -->
<div class="partner-tile">
  <img src="https://files.readme.io/27d66d23ad126e43e53cc0c7770bbbecb3dc72629a37a54a69eac16a261648d1-idkXAD-6HN_1735818502640.png" alt="Kaleyra Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/kaleyra" target="_blank" rel="noopener noreferrer">Kaleyra</a></p>
</div>

<!-- Partner 47 -->
<div class="partner-tile">
  <img src="https://files.readme.io/f59fb14e6fbbface19d3a97c3e2fb9a47bd1df4964c41774714c222e61723657-idMPnFrbc7_1735818519416.png" alt="Zapier Logo" class="partner-logo">
  <p><a class="partner-link" href="https://staging.docs.user.clevertap.net/docs/zapier" target="_blank" rel="noopener noreferrer">Zapier</a></p>
</div>
<!-- Partner 48 -->
<div class="partner-tile">
  <img src="https://files.readme.io/a238474a2c5b87c76908bb670c7b5805ce2e88228b060edaf1e98e9739db4a5b-image.png" alt="HighTouch Logo" class="partner-logo">
  <p><a class="partner-link" href="https://docs.clevertap.com/docs/hightouch" target="_blank" rel="noopener noreferrer">HighTouch</a></p>
</div>
  </div>
</body>
</html>
`}</HTMLBlock>
