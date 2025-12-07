---
title: Demo Filters
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
    <title>Filters UI & Campaign Reports</title>
    <style>
        /* Tabs/Filters */
        .tabs {
            margin-bottom: 20px;
            display: flex;
            gap: 5px;
        }
        .tab-label {
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 12px;
            font-weight: bold;
            color: white;
            cursor: pointer;
        }
        .new-feature { background-color: #4CAF50; }
        .enhancement { background-color: #2962FF; }
        .update { background-color: #673AB7; }
        .all { background-color: #888; }
        
        /* Articles */
        .tab-content {
            display: none;
            max-width: 700px;
        }
        .article {
            border: 1px solid #ddd;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 5px;
            background-color: #f9f9f9;
        }
        
        /* Badge inside articles */
        .badge {
            display: inline-block;
            padding: 3px 8px;
            border-radius: 4px;
            font-size: 11px;
            font-weight: bold;
            color: white;
        }
        
        /* Show the checked tab content */
        #tab1:checked ~ #content1,
        #tab2:checked ~ #content2,
        #tab3:checked ~ #content3,
        #tab4:checked ~ #content4 {
            display: block;
        }
        
        /* Hide radio buttons */
        input[type="radio"] {
            display: none;
        }
    </style>
</head>
<body>
    <h3>FILTERS</h3>
    
    <!-- Hidden Radio Buttons for Tabs -->
    <input type="radio" id="tab1" name="tabs" checked>
    <input type="radio" id="tab2" name="tabs">
    <input type="radio" id="tab3" name="tabs">
    <input type="radio" id="tab4" name="tabs">
    
    <!-- Tab Labels -->
    <div class="tabs">
        <label for="tab1" class="tab-label all">ALL</label>
        <label for="tab2" class="tab-label new-feature">NEW FEATURE</label>
        <label for="tab3" class="tab-label enhancement">ENHANCEMENT</label>
        <label for="tab4" class="tab-label update">UPDATE</label>
    </div>
    
    <!-- Tab Contents -->
    <!-- All Articles -->
    <div id="content1" class="tab-content">
        <div class="article new-feature">
            <h2>February</h2>
            <h3>New Feature Release <span class="badge new-feature">NEW FEATURE</span></h3>
            <p>This is a new feature update.</p>
        </div>
        <div class="article enhancement">
            <h2>February</h2>
            <h3>Enhancement Update <span class="badge enhancement">ENHANCEMENT</span></h3>
            <p>Enhancements have been added.</p>
        </div>
        <div class="article update">
            <h2>February</h2>
            <h3>System Update <span class="badge update">UPDATE</span></h3>
            <p>The system has been updated.</p>
        </div>
    </div>
    
    <!-- New Feature Articles -->
    <div id="content2" class="tab-content">
        <div class="article new-feature">
            <h2>February</h2>
            <h3>New Feature Release <span class="badge new-feature">NEW FEATURE</span></h3>
            <p>This is a new feature update.</p>
        </div>
    </div>
    
    <!-- Enhancement Articles -->
    <div id="content3" class="tab-content">
        <div class="article enhancement">
            <h2>February</h2>
            <h3>Enhancement Update <span class="badge enhancement">ENHANCEMENT</span></h3>
            <p>Enhancements have been added.</p>
        </div>
    </div>
    
    <!-- Update Articles -->
    <div id="content4" class="tab-content">
        <div class="article update">
            <h2>February</h2>
            <h3>System Update <span class="badge update">UPDATE</span></h3>
            <p>The system has been updated.</p>
        </div>
    </div>
</body>
</html>
`}</HTMLBlock>
