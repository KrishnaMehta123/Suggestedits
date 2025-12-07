---
title: CSS Testing for Tabbed Information
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
    <title>CSS-Only Horizontal Tabs</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f9f9f9;
            padding: 20px;
        }

        .tab-container {
            max-width: 800px;
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        input[type="radio"] {
            display: none;
        }

        .tab-labels {
            display: flex;
            border-bottom: 2px solid #ddd;
        }

        .tab-label {
            flex: 1;
            padding: 15px;
            cursor: pointer;
            background: #f0f0f0;
            text-align: center;
            font-weight: bold;
            color: #333;
            transition: background 0.3s ease;
            border-bottom: 3px solid transparent;
        }

        input[type="radio"]:checked + .tab-label {
            background: #e0e0e0;
            color: #007bff;
            border-bottom: 3px solid #007bff;
        }

        .tab-content-wrapper {
            position: relative;
            width: 100%;
        }

        .tab-content {
            display: none;
            padding: 20px;
            font-size: 14px;
            color: #333;
            animation: fadeIn 0.3s ease;
        }

        input[type="radio"]:checked + .tab-label + .tab-content-wrapper .tab-content {
            display: block;
        }

        pre {
            background: #f5f5f5;
            padding: 15px;
            border-radius: 5px;
            overflow: auto;
            font-family: 'Courier New', monospace;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>

    <div class="tab-container">
        <!-- Tab 1 -->
        <input type="radio" id="tab1" name="tab-group" checked>
        <label class="tab-label" for="tab1">Webhook Details</label>
        
        <input type="radio" id="tab2" name="tab-group">
        <label class="tab-label" for="tab2">Transformation Code</label>

        <!-- Content wrapper -->
        <div class="tab-content-wrapper">
            <div class="tab-content" id="content1">
                <h3>Webhook Details</h3>
                <pre>
{
    "headers": {},
    "payload": {
        "event_id": "01HC3M3NF4TR1DR47RHYSWTRP5",
        "event_type": "form_response",
        "form_response": {
            "form_id": "uaIA4a7Y",
            "title": "Project Feedback Survey"
        }
    }
}
                </pre>
            </div>

            <div class="tab-content" id="content2">
                <h3>Transformation Code</h3>
                <pre>
// Example transformation code
let brazecall = {
    attributes: [
        {
            external_id: payload.user_id,
            _update_existing_only: true,
            attribute_1: payload.attribute_1
        }
    ],
    events: []
};
                </pre>
            </div>
        </div>
    </div>

</body>
</html>
`}</HTMLBlock>
