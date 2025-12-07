---
title: Release Notes 2025
fullscreen: false
hidden: true
metadata:
  title: ''
  description: ''
---
###### Stay ahead with CleverTap's latest releases in customer engagement and retention

***

# 2025

## February

<HTMLBlock>{`
<div class="container">
  <div class="filter-content-wrapper">
          <div class="filters">
            <h4>FILTERS</h4>
            <label class="filter-option">
              <input type="checkbox" id="campaigns">
              <span class="badge campaigns">CAMPAIGNS</span>
            </label>
            <label class="filter-option">
              <input type="checkbox" id="journeys">
              <span class="badge journeys">JOURNEYS</span>
            </label>
            <label class="filter-option">
              <input type="checkbox" id="segments">
              <span class="badge segments">SEGMENTS</span>
            </label>
            <label class="filter-option">
              <input type="checkbox" id="cohort">
              <span class="badge cohort">COHORT</span>
            </label>
            <label class="filter-option">
              <input type="checkbox" id="pivot">
              <span class="badge pivot">PIVOT</span>
            </label>
          </div>
          <div class="content">
            <div class="release-note campaigns-article">
              <div class="release-note-header">
                <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg"/></div>
                <div><h3>Introducing Event Personalization Beyond 24 Hours for Live Behavior Campaigns</h3></div>
                <div><span class="badge campaigns">PRIVATE BETA</span></div>
              </div>
              <p>You can now apply Event Personalization to Live Action and Date-time campaigns with a delay of more than 24 hours. You can create highly personalized push campaigns based on event properties to create custom-tailored notifications, driving better targeting and relevance. It also extends the reach of event-triggered communications hours to increase engagement rates and conversions.</p>
              <p>For example, streaming applications can now engage users with personalized messages, even days after their last session, ensuring continued engagement.</p>
              <p>For more information, refer to <a href="">Create Push Notification</a></p>
            </div>
            
      		<hr>
            
            <div class="release-note journeys-article">
              <div class="release-note-header">
                <div><img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg"/></div>
                <div><h3>AI-Powered Message Optimization</h3></div>
                <div><span class="badge journeys">JOURNEYS</span></div>
              </div>
              <p>Message Archiving now supports Google Cloud Platform (GCP), allowing customers to store copies of outgoing messages across different channels in real-time directly in their GCP bucket. The feature is in Public Beta and available to all CleverTap customers using AWS S3 buckets, Azure Blob, and GCP buckets.</p>
              <p>For more information, refer to <a href="https://staging.docs.user.clevertap.net/docs/messaging-archiving" target="_blank">Message Archiving</a></p>
            </div>
            
            <hr>
      
            <div class="release-note segments-article">
              <div class="release-note-header">
                <div><img src="https://files.readme.io/59817747cb1eb7516d6ea352c6f2adbbadb64dd890221fff6690a250f116b012-Bookmarks.svg"/></div>
                <div><h3>Event Personalization Beyond 24 Hours</h3></div>
                <div><span class="badge segments">SEGMENTS</span></div>
              </div>
							<p>The Email Add-on is now available with the CleverTap Essentials Plan. With this add-on, you can use CleverTap as your Email Service Provider (ESP), eliminating the need for third-party integrations.</p>
        <p>To enable the Email add-on from the CleverTap dashboard, purchase the add-on, set up your email preferences, and warm up your dedicated IP to ensure the best possible deliverability.</p>
        <img src="https://files.readme.io/fdf055c4de60720e01da16e73a883ac275845e8884b53a8f46ac757370e3da03-image.png" alt="Email Add-on for CleverTap Essentials Plan"/>
        <p>For more information, refer to <a href="https://docs.clevertap.com/docs/email-add-on-for-clevertap-essentials-plan" target="_blank">Email Add-on.</a></p>
            <hr>
      
            <div class="release-note cohort-article">
              <div class="release-note-header">
                <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg"/></div>
                <div><h3>Enhanced Segmentation Options</h3></div>
                <div><span class="badge cohort">COHORT</span></div>
              </div>
							<p>Scribe for CleverTap Web Push is here to transform your campaign messaging. With Scribe, you can easily and quickly create emotionally resonant web push messages. You can also analyze and refine their tone to better connect with your audience and test multiple variations to maximize campaign effectiveness. This feature is now available to all customers with access to Scribe as part of their Billing Plan.</p>
        <p>For more information refer, <a href="https://staging.docs.user.clevertap.net/docs/scribe#create-a-web-push-notification-using-scribe" target="_blank">Scribe</a></p>
            </div>
            
            <hr>
      
            <div class="release-note pivot-article">
              <div class="release-note-header">
                <div><img src="https://files.readme.io/f59e0d9c60547d4132cb122f31ea7b4f0b72c6609ffe104207d2eca878536871-A_B-Testing.svg"/></div>
                <div><h3>Updated Campaign Analytics Dashboard</h3></div>
                <div><span class="badge pivot">PIVOT</span></div>
              </div>
							 <p>CleverTap now provides Tag Group-wise campaign reports. This is available for Push, Web Push, Email, SMS, and WhatsApp campaigns sent via the Target Users by Identity API. With this enhancement, you can:</p>
        <p>
        <ul>
          <li>Get granular insights with reports broken down by tag groups.</li>
          <li>Optimize campaign strategies by identifying high-performing tag groups.</li>
        </ul>
        </p>
      	<p>
          As a result, you can analyze and refine your messaging strategies effectively. For more information, see <a href="https://docs.clevertap.com/docs/campaign-reports#subscribe-to-reports" target="_blank">Subscribe to Reports.</a>
          </p>
            </div>
          </div>
        </div>
</div>      
`}</HTMLBlock>

<HTMLBlock>{`
<style>
 
 img{
   cursor:pointer;
 }
  /* Main Layout */
.container {
  max-width: 1200px;
  margin: 0 auto;
  height: 100vh;
  overflow: hidden;
}

.filter-content-wrapper {
  display: flex;
  flex-direction: row-reverse;
  gap: 12px;
  height: 100vh;
}

.release-note-header {
  display: flex;
  align-items: center;
  gap: 8px;
}

/* Filters */
.filters {
  width: 200px;
  height: 100%;
  overflow-y: auto;
  position: sticky;              
  top: 20px;                      
  padding: 20px;
  box-sizing: border-box;          
  z-index: 10;                    
}

h4 {
  font-size: 16px;
  color: #444C5A;
  font-weight: bold;
}

.filter-option {
  display: flex;
  align-items: center;
  margin-bottom: 10px;
  cursor: pointer;
}

.filter-option input {
  margin-right: 10px;
  width: 16px;
  height: 16px;
  cursor: pointer;
}
  
/* Content */
.content {
  flex: 1;
  padding: 10px;
  overflow-y: auto;
}

.release-note {
  padding: 10px;
  background-color: white;
  margin-bottom: 20px;
  transition: all 0.3s ease;
}

/* Badges */
.badge {
  font-size: 12px;
  font-weight: 700;
  color: white;
  padding: 0px 4px;
  border-radius: 5px;
  display: inline-block;
}

/* Updated Badge Colors */
.campaigns { background-color: #B0B0B0; }    /* Private Beta -> Campaigns */
.journeys { background-color: #9E9E9E; }     /* Beta -> Journeys */
.segments { background-color: #4CAF50; }     /* New Feature -> Segments */
.cohort { background-color: #2962FF; }       /* Enhancement -> Cohort */
.pivot { background-color: #673AB7; }        /* Update -> Pivot */

a {
  text-decoration: none !important;
}

/* 🌟 Filtering Logic for Multiple Selections 🌟 */
.filter-content-wrapper:has(input:checked) .release-note {
  display: none;
}

.filter-content-wrapper:has(#campaigns:checked) .campaigns-article {
  display: block;
}

.filter-content-wrapper:has(#journeys:checked) .journeys-article {
  display: block;
}

.filter-content-wrapper:has(#segments:checked) .segments-article {
  display: block;
}

.filter-content-wrapper:has(#cohort:checked) .cohort-article {
  display: block;
}

.filter-content-wrapper:has(#pivot:checked) .pivot-article {
  display: block;
}

.filter-content-wrapper:not(:has(input:checked)) .release-note {
  display: block;
}

@media (max-width: 1024px) {
  .container {
    height: auto;
    min-height: 100vh;
  }
  .filter-content-wrapper {
    flex-direction: column;
    height: auto;
  }
  .filters {
    width: 100%;
    position: static;
    top: auto;
    padding: 15px;
    height: auto;
    overflow-y: visible;
  }
  .content {
    width: 100%;
    height: auto;
  }
}

/* Mobile devices */
@media (max-width: 768px) {
  .container {
    padding: 10px;
    height: auto;
    min-height: 100vh;
  }
  .filter-content-wrapper {
    flex-direction: column;
    height: auto;
  }
  .filters {
    width: 100%;
    padding: 10px;
    height: auto;
    overflow-y: visible;
  }
  .content {
    width: 100%;
    padding: 5px;
  }
  .release-note {
    padding: 10px;
    margin-bottom: 15px;
  }
  .release-note-header {
    flex-direction: column;
    align-items: flex-start;
    gap: 4px;
  }
  .badge {
    font-size: 10px;
    padding: 2px 4px;
  }
}
</style>
`}</HTMLBlock>
