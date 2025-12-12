---
title: Copy of Release Notes Filter Testing
excerpt: >-
  Stay ahead with CleverTap's latest releases in customer engagement and
  retention.
deprecated: false
hidden: true
metadata:
  description: >-
    CleverTap has introduced a range of new features and enhancements to improve
    customer engagement strategies, including support for TikTok remarketing,
    Azure Blob message archiving, WhatsApp carousel templates, and personalized
    email sender fields. These updates aim to enhance user experience,
    streamline campaign management, and provide deeper insights into customer
    interactions.
  keywords:
    - release notes
    - what's new
    - product updates
    - update
    - updates
    - product changelog
  robots: index
---
Stay updated with CleverTap's latest feature releases, cutting-edge feature enhancements, and performance enhancements to help you optimize your experience.

View previous updates in [What's New: 2024](https://docs.clevertap.com/docs/release-notes-2024).

<ClickableTilesForWhatsNew />

# Release Type Legend

<TypesOfProductReleases />

<HTMLBlock>{`
<style>
  .filters {
    margin-top: 40px;
  }

  .filters h1 {
    font-size: 24px;
    font-weight: 600;
    margin-bottom: 16px;
  }

  .filter-box {
    background-color: #f8f9fc;
    border: 1px solid #e2e8f0;
    border-radius: 8px;
    padding: 24px 32px;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.04);
  }

  .filter-options {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 16px 32px;
  }

  .filter-option {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 14px;
    font-weight: 500;
  }

  .filter-option img {
    width: 20px;
    height: 20px;
  }
</style>

<div class="filters">
  <h1>Filter By Feature</h1>
  <div class="filter-box">
    <div class="filter-options">
      <label class="filter-option">
        <input type="checkbox" id="filter-security-project-settings" />
        <span class="security-project-settings">
          <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" />
          Security & Project Settings
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-data-and-integrations" />
        <span class="data-and-integrations">
          <img src="https://files.readme.io/bf86621cc6be2995b3a9323ccfcaae0e172d6da76b2bfedc7983c5be75eb179d-Partners_Icon_Outlined.svg" alt="Data & Integrations" />
          Data & Integrations
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-analytics" />
        <span class="analytics">
          <img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg" alt="Analytics" />
          Analytics
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-segments" />
        <span class="segments">
          <img src="https://files.readme.io/04fe24c1114cef41af4a4e0224cab88f5be4c31160eca491d67942c689cb79c0-Segmentation.svg" alt="Segments" />
          Segments
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-campaigns" />
        <span class="campaigns">
          <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" />
          Campaigns
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-journeys" />
        <span class="journeys">
          <img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" />
          Journeys
        </span>
      </label>

			<label class="filter-option">
        <input type="checkbox" id="filter-promotions" />
        <span class="promotions">
          <img src="https://files.readme.io/c65a9fbb8af21c3a8f01c546faa2089d52a3bf54c2efecc740879b1ea681242e-Property_1Selected.svg" alt="Promotions" />
          Promotions
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-conversations" />
        <span class="conversations">
          <img src="https://files.readme.io/ae95d26dd8714ac2522e7a2b39166d95ace62433496df35d5dcc4d90414527bd-Conversations.svg" alt="Conversations" />
          Conversations
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-product-experiences" />
        <span class="product-experiences">
          <img src="https://files.readme.io/d7de531a1060998537a4e71a078198cf28076d99e1aed3e3c1bdcb5509e29d95-Product_experiences.svg" alt="Product Experiences" />
          Product Experiences
        </span>
      </label>

      <label class="filter-option">
        <input type="checkbox" id="filter-content-manager" />
        <span class="content-manager">
          <img src="https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg" alt="Content Manager" />
          Content Manager
        </span>
      </label>
    </div>
  </div>
</div>
`}</HTMLBlock>

# 2025

## December

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="pii-tokenization">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#pii-tokenization"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">PII Tokenization</h3>
<div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>You can now protect sensitive user data by ensuring that Personally Identifiable Information (PII) never enters CleverTap’s environment. Instead of sending identifiers such as email addresses or phone numbers, you send tokens that map securely to your own vault. CleverTap then processes only tokens for Segments, Engagements, and Analytics, keeping all personal data fully within your control.</p>
<p>With PII Tokenization, you can:</p>
    <p>
      <ul>
        <li><strong>Protect Sensitive Data:</strong> Replace PII with tokens to comply with data privacy and residency regulations.</li>
        <li><strong>Choose Your Vault Model:</strong> Use CleverTap Vault or bring your own for flexibility.</li>
        <li><strong>Simplify Integration:</strong> Generate and manage tokens using the Vault API for seamless client-side setup.</li>
        <li><strong>Control Dispatch Models:</strong> Run the Dispatcher On-Prem (no PII leaves your environment) or Off-Prem (secure, token-only resolution at send time).</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/pii-tokenization" target="_blank">PII Tokenization</a>.</p>
</div>
<hr/>
</div>
`}</HTMLBlock>

## November

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="automated-audit-log-exports-for-siem">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#automated-audit-log-exports-for-siem"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Automated Audit Log Exports for SIEM</h3>
<div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
     <p>You can now securely export audit logs from CleverTap to your own cloud storage providers, including AWS S3, Google Cloud Storage, or Microsoft Azure Blob Storage. This self-serve feature allows you to easily manage, store, and retain audit data within your own cloud environment.</p>
    <p>With SIEM Export, you can:</p>
<p>
  <ul>
    <li><strong>Automate Secure Delivery:</strong> Receive exports every 4 hours in JSON (UTF-8) format.</li>
    <li><strong>Ensure Continuous Visibility:</strong> Monitor all account activities in real time to strengthen compliance and security posture.</li>
    <li><strong>Maintain Full Data Control:</strong> Store audit logs directly within your organization’s cloud to manage retention and governance.</li>
    <li><strong>Integrate Seamlessly with SIEM Tools:</strong> Combine CleverTap’s audit data with broader operational insights across your systems.</li>
  </ul>
</p>

<p>For more information, refer to <a href="https://docs.clevertap.com/docs/automated-audit-log-exports-for-siem" target="_blank">Automated Audit Log Exports for SIEM</a>.</p>
</div>
<hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="whatsapp-flows-for-whatsapp-direct">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#whatsapp-flows-for-whatsapp-direct"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">WhatsApp Flows for WhatsApp Direct</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div> 
  </div>
  <div class="release-note-body">
    <p>Introducing WhatsApp Flows, a form-based experience that lets your users complete tasks such as booking a ticket or placing an order without leaving WhatsApp. CleverTap handles orchestration, analytics, and automation. Flows are created at the WhatsApp Business Account level and appear as a call-to-action button in your message. Tapping the button opens a guided, structured journey that follows Meta’s Flows specification.</p>
    <p>With WhatsApp Flows, you can:</p>
<p>
      <ul>
        <li><strong>Choose Your Setup</strong>: Use static flows, a CleverTap endpoint with customer relay, or your own endpoint for full control.</li>
        <li><strong>
Protect Data End to End</strong>: Keep payloads encrypted on the device and decrypt or re-encrypt according to the selected setup.</li>
        <li><strong>Capture Outcomes in CleverTap</strong>: Record Flow events for reporting and update profile attributes for personalization and segmentation.</li>
        <li><strong>Use Templates Seamlessly</strong>: Attach a Flow to a WhatsApp template, personalize message content, and publish in campaigns.</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/whatsapp-flows" target="_blank">WhatsApp Flows.</a></p>
</div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"campaigns\" id=\"preferred-channel-for-engagement\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#preferred-channel-for-engagement\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n     <img src=\"https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg\" alt=\"Campaigns\" />\n    </div>\n    <h3 class=\"release-note-heading\">Preferred Channel for Engagement</h3>\n    <div class=\"badge new-feature\">NEW FEATURE</div>\n    <div class=\"badge private-beta\">PRIVATE BETA</div>\n  </div>\n\n  <div class=\"release-note-body\">\n    <p>You can now deliver messages through the channel each user is most likely to engage with. Powered by Clever.AI, Preferred Channel analyzes engagement data across Push, Email, SMS, and WhatsApp over the past 90 days to predict and select the best-performing communication channel for every user.</p>\n\n    <p>With Preferred Channel, you can:</p>\n\n    <p>\n      <ul>\n        <li><strong>Leverage AI-Powered Channel Prediction</strong>: Identify the most effective communication channel for each user based on engagement history.</li>\n        <li><strong>Integrate Seamlessly Across CleverTap</strong>: Use the new Preferred Channel user property in Segmentation, Campaigns, Journeys, and Analytics.</li>\n        <li><strong>Boost Conversions and Reduce Noise</strong>: Focus on the channels that drive real engagement and results.</li>\n        <li><strong>Automate Channel Selection</strong>: Let Clever.AI optimize delivery so you can focus on content and strategy.</li>\n      </ul>\n    </p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/preferred-channel\" target=\"_blank\">Preferred Channel</a>.</p>\n  </div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"security-project-settings\" id=\"field-level-at-rest-encryption-for-user-and-event-properties\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#field-level-at-rest-encryption-for-user-and-event-properties\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg\" alt=\"Settings\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">Field-Level at Rest Encryption for User and Event Properties</h3>\n<div class=\"badge new-feature\">NEW FEATURE</div>\n  </div>\n  <div class=\"release-note-body\">\n     <p>CleverTap now supports Field-Level at Rest Encryption, enabling you to encrypt user and event properties for stronger data protection. This capability extends beyond the existing volume-level encryption, providing granular control over how sensitive data, including system and user properties, is secured within the platform.</p>\n    <p>With this capability, you can:</p>\n    <p>\n      <ul>\n        <li><strong>Protect Sensitive Fields:</strong> Selectively encrypt both user and event properties while keeping the rest of your data accessible for Analytics.</li>\n        <li><strong>Choose Your Key Strategy:</strong> Use CleverTap-managed keys or Bring Your Own Keys (BYOK) encryption through AWS KMS.</li>\n        <li><strong>Enable Encryption Easily:</strong> Apply encryption to the properties directly from the Schema page.</li>\n        <li><strong>Maintain Platform Compatibility:</strong> Ensure that encrypted fields continue to work seamlessly across Segments, Campaigns, and Analytics for authorized users.</li>\n      </ul>\n    </p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/field-level-at-rest-encryption\" target=\"_blank\">Field-Level at Rest Encryption</a>.</p>\n</div>\n<hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"security-project-settings\" id=\"bring-your-own-key-byok-for-encryption\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#bring-your-own-key-byok-for-encryption\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg\" alt=\"Settings\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">Bring Your Own Key (BYOK) for Encryption</h3>\n<div class=\"badge new-feature\">NEW FEATURE</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>CleverTap now supports Bring Your Own Key (BYOK), enabling you to use your organization’s own AWS KMS–managed encryption keys for securing data across the platform.</p>\n    <p>With this capability, you can:</p>\n    <p>\n      <ul>\n        <li><strong>Enforce Customer-Controlled Encryption:</strong> Protect data during file uploads using your keys within AWS KMS.</li>\n\n       <li><strong>Meet Enterprise Compliance Requirements:</strong> Maintain strict governance, auditability, and alignment with regulated industry standards.</li>\n\n <li><strong>Enable Seamless Key Rotation:</strong> Update CleverTap encryption to align with your KMS rotation callbacks, without impacting ongoing services.</li>\n\n<li><strong>Ensure Secure Integration:</strong> Retrieve keys securely over HTTPS on TLS 1.2. CleverTap never stores or persists customer keys; only metadata, such as key name and version, is stored.</li>\n      </ul>\n    </p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/bring-your-own-key-byok-encryption\" target=\"_blank\">BYOK Encryption</a>.</p>\n  </div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"security-and-project-settings\" id=\"teams-structured-collaboration-with-enhanced-governance\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#teams-structured-collaboration-with-enhanced-governance\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg\" alt=\"Security & Project Settings\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">Teams: Structured Collaboration with Enhanced Governance</h3>\n    <div class=\"badge new-feature\">NEW FEATURE</div>\n    <div class=\"badge private-beta\">PRIVATE BETA</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>Introducing Teams, a new way to organize and secure collaboration within CleverTap. Teams let you group users and information according to your organization’s structure, ensuring each team accesses only relevant data. This improves visibility, control, and data governance across large operations.</p>\n    <p>With Teams, you can:</p>\n    <p>\n      <ul>\n        <li>View and manage only the campaigns, templates, and data owned by your team.</li>\n        <li>Define teams, assign users, and configure event-level access aligned with your business hierarchy.</li>\n        <li>Work within a clean, focused team view and switch between teams seamlessly.</li>\n        <li>Use API support for Campaign, Custom List Segment, and Email Template APIs.</li>\n      </ul>\n    </p>\n    <p>Teams prevent cross-team data overlap, ensuring integrity, security, and operational efficiency across your organization.</p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/teams-setup\" target=\"_blank\">Teams Setup</a>.</p>\n</div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"data-and-integrations\" id=\"bulk-upload-for-geofences\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#bulk-upload-for-geofences\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg\" alt=\"Data & Integrations\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">Bulk Upload for Geofences</h3>\n    <div class=\"badge enhancement\">ENHANCEMENT</div>\n    <div class=\"badge private-beta\">PRIVATE BETA</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>You can now add multiple geo clusters and fences simultaneously using CSV or JSON files, enabling faster and more efficient setup of large-scale, location-based campaigns. Previously, each cluster and fence had to be added manually — a time-consuming process for campaigns involving hundreds of store locations or regions.</p>\n    <p>With Bulk Upload, you can manage up to 10,000 radius-based geofences effortlessly, streamlining campaign setup for multi-location businesses.</p>\n    <p>Key benefits include:</p>\n    <p>\n      <ul>\n        <li>Faster setup: Upload multiple clusters and fences in a single step.</li>\n        <li>Operational efficiency: Eliminate repetitive manual entry and reduce errors.</li>\n        <li>Scalable targeting: Seamlessly manage large-scale, region-based campaigns.</li>\n      </ul>\n    </p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/geofencing-campaign-1#bulk-upload\" target=\"_blank\">Bulk Upload</a>.</p>\n</div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"campaigns\" id=\"rcs-business-messaging-with-generic-provider-support\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#rcs-business-messaging-with-generic-provider-support\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg\" alt=\"Campaigns\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">RCS Business Messaging with Generic Provider Support</h3>\n    <div class=\"badge new-feature\">NEW FEATURE</div>\n    <div class=\"badge private-beta\">PRIVATE BETA</div> \n  </div>\n  <div class=\"release-note-body\">\n    <p>You can now connect CleverTap with your preferred RCS provider through a simple configuration, keeping all orchestration, analytics, and automation in one place.</p>\n    <p>With this feature, you can:</p>\n    <p>\n      <ul>\n        <li>Bring your own RCS provider with a generic configuration.</li>\n        <li>Drive engagement with rich media and two-way interactions that trigger campaigns and journeys.</li>\n        <li>Maximize reach with automatic SMS fallback and dedicated RCS metrics for delivery, view, and click.</li>\n      </ul>\n    </p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/generic-rcs\" target=\"_blank\">Generic RCS</a> and<a href=\"https://developer.clevertap.com/docs/generic-rcs-api\" target=\"_blank\"> Generic RCS API</a>.</p>\n</div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"security-project-settings\" id=\"end-to-end-pii-encryption-in-transit-for-sdks\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#end-to-end-pii-encryption-in-transit-for-sdks\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg\" alt=\"Settings\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">End-to-End PII Encryption in Transit for SDKs</h3>\n<div class=\"badge new-feature\">NEW FEATURE</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>CleverTap now offers enhanced encryption of all PII and sensitive data in transit between SDKs and backend servers.</p>\n\n    <p>With this enhancement, you can:</p>\n    <p>\n      <ul>\n        <li><strong>Ensure Secure Data Exchange:</strong> Encrypt all PII data transmitted from SDKs using AES-256 encryption, safeguarding against Man in the Middle attacks.</li>\n        <li><strong>Prevent Network-Level Threats:</strong> Protect all SDK communication from man-in-the-middle (MITM) and data interception attempts, maintaining confidentiality throughout transmission.</li>\n        <li><strong>Maintain Compliance Readiness:</strong> Meet financial-grade encryption standards and align with industry standards and enterprise security mandates, supporting fintech and other data-sensitive use cases.</li>\n        <li><strong>Simplify Implementation:</strong> Manage encryption and decryption within the SDK, ensuring seamless, cross-platform protection across Android, iOS, Web, Cordova, Flutter, and React Native.</li>\n      </ul>\n    </p>\n  <p>For more information, refer to <a href=\"https://developer.clevertap.com/docs/android-advanced-features#encryption-in-transit\" target=\"_blank\">Android</a>,\n    <a href=\"https://developer.clevertap.com/docs/advanced-options-ios#encryption-of-pii-data\" target=\"_blank\">iOS</a>, <a href=\"https://developer.clevertap.com/docs/advanced-configurations#encryption-of-pii-data\" target=\"_blank\">Web</a>, <a href=\"https://developer.clevertap.com/docs/cordova-advance-features#encryption-for-pii-data\" target=\"_blank\"> Cordova</a>,<a href=\"https://developer.clevertap.com/docs/flutter-advanced-features#encryption-for-pii-data\" target=\"_blank\"> Flutter</a>, and <a href=\"https://developer.clevertap.com/docs/react-native-advanced-features#encryption-for-pii-data\" target=\"_blank\"> React Native</a>.</p>\n  </div>\n  <hr/>\n</div>
`}</HTMLBlock>

## October

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"Campaigns\" id=\"Nested-Objects-in-Custom-User-Properties-New-Feature\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Nested-Objects-in-Custom-User-Properties-New-Feature\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg\" alt=\"Campaigns\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">Nested Objects in Custom User Properties</h3>\n    <div class=\"badge new-feature\">NEW FEATURE</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>Introducing Nested Objects in Custom User Properties, a powerful feature that simplifies how you represent and ingest complex user data in CleverTap. Define rich, structured entities such as insurance policies, subscriptions, or shopping carts using a JSON  eliminating the need to flatten data or manage multiple attributes across systems.</p>\n    <p>With Nested Objects, you can:</p>\n    <p>\n      <ul>\n        <li>Model structured user data natively within CleverTap, preserving relationships between entities.</li>\n        <li>Build granular, condition-based segments using nested attributes (for example, filter users with a policy missing a beneficiary email).</li>\n        <li>Simplify engineering workflows through direct JSON ingestion without additional data transformation.</li>\n        <li>Visualize and filter nested data within Segment builder, unlocking deeper insights for marketers and analysts.</li>\n      </ul>\n    </p>\n<p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/nested-objects\" target=\"_blank\">Nested Objects</a> and<a href=\"https://developer.clevertap.com/docs/ingesting-nested-objects-via-clevertap-apis\" target=\"_blank\"> Ingesting Nested Objects via CleverTap APIs</a>.</p>\n  </div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"security-project-settings\" id=\"Secure-File-Uploads-through-SFTP-Encryption-Enhancement\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Secure-File-Uploads-through-SFTP-Encryption-Enhancement\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg\" alt=\"Settings\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">Secure File Uploads through SFTP Encryption</h3>\n    <div class=\"badge enhancement\">ENHANCEMENT</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>CleverTap now supports encrypted file uploads via SFTP, ensuring that all data ingested through the SFTP pipeline remains secure and compliant with data protection standards. You can safely transfer sensitive customer data using end-to-end PGP encryption and manage encryption keys flexibly.</p>\n    <p>With SFTP Encryption, you can:</p>\n    <p>\n      <ul>\n        <li>Protect all file transfers using PGP encryption.</li>\n        <li>Choose between CleverTap-managed or customer-managed encryption keys.</li>\n        <li>Continue using your existing ingestion workflows without disruption.</li>\n        <li>Strengthen compliance and audit readiness for enterprise-grade security.</li>\n      </ul>\n    </p>\n<p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/file-upload-encryption\" target=\"_blank\">File Upload Encryption</a>.</p>\n  </div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"Campaigns\" id=\"custom-conversion-window\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#custom-conversion-window\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg\" alt=\"Campaigns\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">Custom Conversion Window</h3>\n    <div class=\"badge enhancement\">ENHANCEMENT</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>Introducing Custom Conversion Window, an enhancement to Campaigns and Journeys that gives marketers precise control over conversion tracking. You can now define custom conversion durations, from 1 minute to 5 months, instead of being limited to fixed options like 7 or 14 days. This enhancement brings greater flexibility, accuracy, and consistency, helping marketers align conversion measurement with real user behavior.</p>\n    <p>With Custom Conversion Window, you can:</p>\n    <p>\n      <ul>\n        <li>Track conversions accurately by aligning the window with your business cycle (for example, 10 days for e-commerce purchases, 72 hours for flash sales).</li>\n        <li>Improve ROI accuracy by removing undercounting or overcounting from preset durations.</li>\n        <li>Maintain consistency across reports and dashboards with unified data tracking.</li>\n      </ul>\n    </p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/create-message-push\" target=\"_blank\">Create Message</a> and<a href=\"https://docs.clevertap.com/docs/push-campaign-stats\" target=\"_blank\"> Stats</a>.</p>\n  </div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="Analytics" id="ai-powered-nps-feedback-analysis">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#ai-powered-nps-feedback-analysis"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg" alt="Analytics" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">AI-Powered NPS Feedback Analysis</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>The NPS Board now offers AI-powered insights that transform raw feedback into actionable sentiment analysis. Beyond numeric scores, you can instantly understand what customers feel and why, helping your teams act faster on key feedback themes.</p>
    <p>With this enhancement, you can:</p>
    <p>
      <ul>
        <li>Generate instant AI summaries of NPS responses, highlighting key insights.</li>
        <li>Identify key themes with positive, negative, or neutral sentiment indicators.</li>
        <li>Visualize frequently mentioned terms using an AI-generated word cloud.</li>
        <li>Track sentiment trends over time using daily, weekly, or monthly intervals..</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/nps-board-1" target="_blank">NPS Board</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"security-project-settings\" id=\"End-to-End-Encryption-for-CPaaS-Communication\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#End-to-End-Encryption-for-CPaaS-Communication\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg\" alt=\"Settings\" />\n    </div>\n    <h3 class=\"release-note-heading\">End-to-End Encryption for CPaaS Communication</h3>\n    <div class=\"badge new-feature\">NEW FEATURE</div>\n    <div class=\"badge ga\">GA</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>CleverTap now supports end-to-end encryption for all CPaaS communications over Email and SMS via the Generic HTTP API configuration. This feature ensures every payload and callback is encrypted using AES-256, securing PII data such as email addresses and phone numbers.</p>\n<p>With CPaaS Encryption, you can:</p>\n    <p>\n      <ul>\n        <li>Protect outbound and inbound data with end-to-end encryption.</li>\n        <li>Meet enterprise security and compliance requirements, and now meet BFSI-grade compliance requirements while maintaining performance and scalability.</li>\n        <li>Enable encryption with a single toggle in the provider setup under Generic HTTP API configuration, supporting both CleverTap-managed and customer-managed keys (BYOK).</li>\n        <li>Scale seamlessly across providers via the Generic HTTP API.</li>\n        <li>Manage key versioning and rotation without service disruption.</li>\n      </ul>\n    </p>\n<p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/cpaas-encryptions\" target=\"_blank\">CPaaS Encryption</a>.</p>\n  </div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"promotions\" id=\"new-in-promotions-custom-rewards\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#new-in-promotions-custom-rewards\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/c65a9fbb8af21c3a8f01c546faa2089d52a3bf54c2efecc740879b1ea681242e-Property_1Selected.svg\" alt=\"Promotions\" />\n    </div>\n    <h3 class=\"release-note-heading\">New in Promotions: Custom Rewards</h3>\n    <div class=\"badge enhancement\">ENHANCEMENT</div>\n    <div class=\"badge private-beta\">PRIVATE BETA</div> \n  </div>\n  <div class=\"release-note-body\">\n    <p>Introducing Custom Rewards, a significant expansion of CleverTap’s Promo capabilities.\nYou can now create, host, and manage your own rewards within CleverTap promo and distribute it to tailored user segments through Promo campaigns. From physical and digital rewards (branded merchandise or OTT subscriptions) to self-managed wallets hosted on your end (real-money cashback or loyalty credits) you can do a webhook-based fulfillment to your systems.</p>\n    <p>With Custom Rewards, you can:</p>\n    <p>\n      <ul>\n        <li>Orchestrate personalized reward campaigns at scale by offering cashback in your hosted wallet for repeat buyers or issuing gift vouchers to users who achieve a milestone.</li>\n        <li>Support diverse engagement use cases such as loyalty programs, event-based rewards, or promotional credits, without relying on fixed, built-in reward types.</li>\n        <li>Simplify reward orchestration with a centralized catalog for all reward types, reducing operational complexity for marketing teams.</li>\n      </ul>\n    </p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/custom-rewards\" target=\"_blank\">Custom Rewards</a>.</p>\n</div>\n  <hr/>\n</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class=\"release-note article\" data-category=\"Campaigns\" id=\"in-app-messages-improvements\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#in-app-messages-improvements\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg\" alt=\"Campaigns\" class=\"release-note-heading-icon\"/>\n    </div>\n    <h3 class=\"release-note-heading\">In-App Messages Improvements</h3>\n    <div class=\"badge enhancement\">ENHANCEMENT</div>\n  </div>\n\n  <div class=\"release-note-body\">\n    <p>CleverTap’s enhanced In-App Messages empower marketers to create fully customizable, interactive, and high-converting campaigns without requiring code. These updates simplify campaign creation, lower time-to-market, and deliver delightful In-App experiences that drive engagement and conversions.</p>\n\n    <p>The following features are now available based on your plan:</p>\n\n    <ul>\n      <li><b>Advanced In-App Builder:</b> Build visually rich In-App messages using a no-code, drag-and-drop editor with animations, flexible layouts, and layered elements. For more information, refer to <a href=\"https://docs.clevertap.com/docs/advanced-in-app-builder\" target=\"_blank\">Advanced In-App Builder</a>.</li>\n\n      <li><b>Gamified Experiences:</b> Use pre-built “Spin the Wheel” and “Scratch Card” templates in the Custom HTML Builder to create engaging, reward-based campaigns. For more information, refer to <a href=\"https://docs.clevertap.com/docs/advanced-in-app-builder\" target=\"_blank\">In-App Gamification Templates</a>.</li>\n\n      <li><b>Custom Code Templates:</b> Create native In-App templates and define custom actions, such as “granting coins” or “navigating to premium”, that marketers can trigger directly from the dashboard. For more information, refer to the Custom Code Templates for <a href=\"https://developer.clevertap.com/docs/ios-custom-code-in-app-templates\" target=\"_blank\">iOS</a>, <a href=\"https://developer.clevertap.com/docs/android-custom-code-in-app-templates\" target=\"_blank\">Android</a>, <a href=\"https://developer.clevertap.com/docs/react-native-custom-code-in-app-templates\" target=\"_blank\">React Native</a>, <a href=\"https://developer.clevertap.com/docs/flutter-custom-code-in-app-templates\" target=\"_blank\">Flutter</a>, and <a href=\"https://developer.clevertap.com/docs/cordova-custom-code-in-app-templates\" target=\"_blank\">Cordova</a>.</li>\n\n      <li><b>Native Prompt Triggers:</b> Allows you to display OS-level prompts such as app rating requests or push pre-permissions within In-App campaigns. For more information on how to render native prompts, refer to <a href=\"https://docs.clevertap.com/docs/advanced-in-app-builder\" target=\"_blank\">Advanced In-App Builder</a>, <a href=\"https://docs.clevertap.com/docs/register-for-push\" target=\"_blank\">Push Primer</a>, <a href=\"https://docs.clevertap.com/docs/app-rating-primer\" target=\"_blank\">App Rating Primer</a>, and <a href=\"https://docs.clevertap.com/docs/app-functions#use-app-functions\" target=\"_blank\">App Functions</a>.</li>\n    </ul>\n  </div>\n  <hr/>\n</div>
`}</HTMLBlock>

<br />

<HTMLBlock>{`
<style>
  nav#hub-sidebar { display: none; }
  
  #content-head h1 {
    font-weight: 500 !important;
    font-size: 35px !important;
  }
  
   .rm-Guides .content-body, .rm-Guides #content-head .col-xs-9 {
      max-width: 100%;
      width: 1000px;
  }
  
  .release-heading-container {
    display: flex;
    align-items: center;
    gap: 5px;
  }
  
  .release-note-heading{
  }
  
  .release-note-body img{
    border: 1px solid rgb(0,0,0,0.2)
  }
  
  .filters h3 {
  margin-bottom: 12px;
  font-size: 20px;
}

.filter-options {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  align-items: center;
}

.filter-option {
  flex: 0 0 calc(33.33% - 14px);
  color: #4A4C4C;
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 16px;
  white-space: nowrap;
}

  .filter-option:hover{
  	cursor:pointer;
    color:#191919;
  }

.filter-option img {
  width: 16px;
  height: 16px;
  color:#4A4C4C;
}

 .filter-option img:hover {
  fill:red;
}

.content-manager {
	display: flex;
  align-items: center;
  gap: 8px;
}

.badges {
  display: flex;
  gap: 4px;
  flex-wrap: wrap;
  align-items: center;
}
  
.badge {
    font-size: 12px;
    font-weight: 700;
    color: white;
  	padding:0px 4px;
    border-radius: 5px;
    display: inline-block;
		min-width: max-content
}
  
  .anchor-link-icon {
  margin-left: -23px;
  opacity: 0;
  transition: opacity 0.3s ease;
}

/* Show the anchor icon on hover */
.release-note-header:hover .anchor-link-icon {
  opacity: 1;
}
 
 .anchor-link-icon{
  	margin-left:-23px;
  }
.anchor-link-icon-inline {
  display: flex;
  align-items: center;
  font-size: 1.2em;
}
  
.release-note-header{
  display:flex;
  gap:8px;
  align-items: center;
 }
  
.private-beta {
    background-color: #B0B0B0;
}
  
.beta {
    background-color: #9E9E9E;
}
  
.new-feature {
    background-color: #4CAF50;
}
  
.enhancement {
    background-color: #2962FF;
}
  
.update {
    background-color: #673AB7;
}
  
/* Hide all articles by default */
.article {
  display: none;
}

/* Show all articles if no filters are checked */
body:not(:has(.filters input:checked)) .article {
  display: block;
}
  
* .rm-Guides a.suggestEdits {
    display: none;
  }

/* Show matching articles */
  body:has(#filter-campaigns:checked) .article[data-category="campaigns"],
	body:has(#filter-promotions:checked) .article[data-category="promotions"],
	body:has(#filter-conversations:checked) .article[data-category="conversations"],
	body:has(#filter-analytics:checked) .article[data-category="analytics"],
	body:has(#filter-segments:checked) .article[data-category="segments"],
	body:has(#filter-journeys:checked) .article[data-category="journeys"],
	body:has(#filter-data-and-integrations:checked) .article[data-category="data-and-integrations"],
	body:has(#filter-product-experiences:checked) .article[data-category="product-experiences"],
	body:has(#filter-content-manager:checked) .article[data-category="content-manager"],
	body:has(#filter-security-project-settings:checked) .article[data-category="security-project-settings"]{
  display: block;
}
  
</style>
`}</HTMLBlock>

<br />
