---
title: Release Notes nav
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
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Navbar + Filters + Main Content</title>
  <style>
    /* 🌟 Your Original CSS 🌟 */
    .container {
      max-width: 100%;
      margin: 0 auto;
      height: 100vh;
      display: flex;
      overflow: hidden;
    }

    .layout-wrapper {
      display: flex;
      width: 100%;
    }

    /* Navigation */
    #leftNav {
      width: 260px;
      background-color: #F1F5FB;
      padding: 20px;
      box-shadow: 2px 0 10px rgba(0, 0, 0, 0.1);
      overflow-y: auto;
      position: sticky;
      top: 0;
      height: 100vh;
      box-sizing: border-box;
    }

    .nav-content {
      display: flex;
      flex-direction: column;
    }

    .topsearch-text {
      font-size: 18px;
      font-weight: bold;
      margin-bottom: 20px;
    }

    .nav-link {
      color: #434761;
      font-size: 14px;
      line-height: 32px;
      padding: 5px 10px;
      text-decoration: none;
      border-radius: 4px;
      transition: background 0.3s;
    }

    .nav-link:hover {
      background-color: #E1E7F0;
    }

    .nav-link:active, .nav-link:focus {
      color: #2962FF;
    }

    /* Filters and Content */
    .filter-content-wrapper {
      display: flex;
      flex: 1;
      overflow: hidden;
    }

    .filters {
      width: 200px;
      padding: 20px;
      background: #fff;
      border-left: 1px solid #ddd;
      overflow-y: auto;
      position: sticky;
      top: 0;
      height: 100vh;
      box-sizing: border-box;
    }

    h4 {
      font-size: 16px;
      color: #444C5A;
      font-weight: bold;
    }

    .filter-option {
      display: flex;
      align-items: center;
      margin-bottom: 12px;
      cursor: pointer;
    }

    .filter-option input {
      margin-right: 10px;
      width: 16px;
      height: 16px;
      cursor: pointer;
    }

    .content {
      flex: 1;
      padding: 20px;
      overflow-y: auto;
    }

    .release-note {
      background: white;
      padding: 20px;
      margin-bottom: 20px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      transition: all 0.3s ease;
    }

    .badge {
      font-size: 12px;
      font-weight: bold;
      color: white;
      padding: 4px 8px;
      border-radius: 5px;
      display: inline-block;
    }

    .campaigns { background-color: #4CAF50; }
    .journeys { background-color: #2962FF; }
    .segments { background-color: #FF9800; }
    .cohort { background-color: #9C27B0; }
    .pivot { background-color: #FF5722; }

    @media (max-width: 1024px) {
      .layout-wrapper {
        flex-direction: column;
      }

      #leftNav, .filters {
        width: 100%;
        height: auto;
        position: static;
      }

      .content {
        width: 100%;
      }
    }

    @media (max-width: 768px) {
      .container {
        padding: 10px;
      }

      .release-note {
        padding: 15px;
        margin-bottom: 15px;
      }

      .badge {
        font-size: 10px;
        padding: 2px 4px;
      }
    }
  </style>
</head>
<body>

<div class="container">
  <!-- Left Navbar -->
  <div id="leftNav">
    <div class="nav-content">
      <p class="topsearch-text">Article Sections</p>
      <a href="#section1" class="nav-link">Introduction</a>
      <a href="#section2" class="nav-link">Features</a>
      <a href="#section3" class="nav-link">Enhancements</a>
      <a href="#section4" class="nav-link">Beta Updates</a>
      <a href="#section5" class="nav-link">Conclusion</a>
    </div>
  </div>

  <!-- Main Content and Filters -->
  <div class="filter-content-wrapper">
    <div class="content">
      <div class="release-note campaigns-article">
        <div class="release-note-header">
          <h3>Event Personalization for Live Campaigns</h3>
          <span class="badge campaigns">CAMPAIGNS</span>
        </div>
        <p>Personalized push campaigns based on event properties to drive better targeting.</p>
      </div>

      <div class="release-note journeys-article">
        <div class="release-note-header">
          <h3>AI-Powered Message Optimization</h3>
          <span class="badge journeys">JOURNEYS</span>
        </div>
        <p>Enhancing real-time message archiving with Google Cloud Platform (GCP) support.</p>
      </div>

      <div class="release-note segments-article">
        <div class="release-note-header">
          <h3>Email Add-on for CleverTap Essentials Plan</h3>
          <span class="badge segments">SEGMENTS</span>
        </div>
        <p>Enables CleverTap as your Email Service Provider (ESP) without third-party integrations.</p>
      </div>

      <div class="release-note cohort-article">
        <div class="release-note-header">
          <h3>Enhanced Segmentation Options</h3>
          <span class="badge cohort">COHORT</span>
        </div>
        <p>Improved segmentation capabilities for better audience targeting and messaging.</p>
      </div>

      <div class="release-note pivot-article">
        <div class="release-note-header">
          <h3>Updated Campaign Analytics Dashboard</h3>
          <span class="badge pivot">PIVOT</span>
        </div>
        <p>Granular insights with reports broken down by tag groups.</p>
      </div>
    </div>

    <!-- Filters -->
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
  </div>
</div>

</body>
</html>
`}</HTMLBlock>

<HTMLBlock>{`
<style>
  /* Main Layout */
.container {
  max-width: 1200px;
  margin: 0 auto;
  height: 100vh;
  display:flex;
  overflow: hidden;
}

.filter-content-wrapper {
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
  height: 100vh;
  overflow-y: auto;
  position: sticky;
  top: 0;
  padding: 10px;
  box-sizing: border-box;
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

/* Tablets and small screens */
@media (max-width: 1024px) {
  .filter-content-wrapper {
    flex-direction: column;
  }
  .filters {
    width: 100%;
    position: static;
    top: auto;
    padding: 15px;
  }
  .content {
    width: 100%;
  }
}

/* Mobile devices */
@media (max-width: 768px) {
  .container {
    padding: 10px;
  }

  .content {
    width: 100%;
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
