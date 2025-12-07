---
title: Release Notes
excerpt: >-
  Stay ahead with CleverTap's latest releases in customer engagement and
  retention.
deprecated: false
hidden: false
metadata:
  title: ''
  description: >-
    CleverTap has introduced a range of new features and enhancements to improve
    customer engagement strategies, including support for TikTok remarketing,
    Azure Blob message archiving, WhatsApp carousel templates, and personalized
    email sender fields. These updates aim to enhance user experience,
    streamline campaign management, and provide deeper insights into customer
    interactions.
  keywords:
    - release notes
    - ' what''s new'
    - ' product updates'
    - ' update'
    - ' updates'
    - ' product changelog'
  robots: index
next:
  description: ''
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
`}</HTMLBlock>
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
          Data & Inegrations
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
<div class="release-note article" data-category="campaigns" id="preferred-channel-for-engagement">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#preferred-channel-for-engagement"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
     <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" />
    </div>
    <h3 class="release-note-heading">Preferred Channel for Engagement</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>

  <div class="release-note-body">
    <p>You can now deliver messages through the channel each user is most likely to engage with. Powered by Clever.AI, Preferred Channel analyzes engagement data across Push, Email, SMS, and WhatsApp over the past 90 days to predict and select the best-performing communication channel for every user.</p>

    <p>With Preferred Channel, you can:</p>

    <p>
      <ul>
        <li><strong>Leverage AI-Powered Channel Prediction</strong>: Identify the most effective communication channel for each user based on engagement history.</li>
        <li><strong>Integrate Seamlessly Across CleverTap</strong>: Use the new Preferred Channel user property in Segmentation, Campaigns, Journeys, and Analytics.</li>
        <li><strong>Boost Conversions and Reduce Noise</strong>: Focus on the channels that drive real engagement and results.</li>
        <li><strong>Automate Channel Selection</strong>: Let Clever.AI optimize delivery so you can focus on content and strategy.</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/preferred-channel" target="_blank">Preferred Channel</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="field-level-at-rest-encryption-for-user-and-event-properties">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#field-level-at-rest-encryption-for-user-and-event-properties"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Field-Level at Rest Encryption for User and Event Properties</h3>
<div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
     <p>CleverTap now supports Field-Level at Rest Encryption, enabling you to encrypt user and event properties for stronger data protection. This capability extends beyond the existing volume-level encryption, providing granular control over how sensitive data, including system and user properties, is secured within the platform.</p>
    <p>With this capability, you can:</p>
    <p>
      <ul>
        <li><strong>Protect Sensitive Fields:</strong> Selectively encrypt both user and event properties while keeping the rest of your data accessible for Analytics.</li>
        <li><strong>Choose Your Key Strategy:</strong> Use CleverTap-managed keys or Bring Your Own Keys (BYOK) encryption through AWS KMS.</li>
        <li><strong>Enable Encryption Easily:</strong> Apply encryption to the properties directly from the Schema page.</li>
        <li><strong>Maintain Platform Compatibility:</strong> Ensure that encrypted fields continue to work seamlessly across Segments, Campaigns, and Analytics for authorized users.</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/field-level-at-rest-encryption" target="_blank">Field-Level at Rest Encryption</a>.</p>
</div>
<hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="bring-your-own-key-byok-for-encryption">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#bring-your-own-key-byok-for-encryption"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Bring Your Own Key (BYOK) for Encryption</h3>
<div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap now supports Bring Your Own Key (BYOK), enabling you to use your organization’s own AWS KMS–managed encryption keys for securing data across the platform.</p>
    <p>With this capability, you can:</p>
    <p>
      <ul>
        <li><strong>Enforce Customer-Controlled Encryption:</strong> Protect data during file uploads using your keys within AWS KMS.</li>

       <li><strong>Meet Enterprise Compliance Requirements:</strong> Maintain strict governance, auditability, and alignment with regulated industry standards.</li>

 <li><strong>Enable Seamless Key Rotation:</strong> Update CleverTap encryption to align with your KMS rotation callbacks, without impacting ongoing services.</li>

<li><strong>Ensure Secure Integration:</strong> Retrieve keys securely over HTTPS on TLS 1.2. CleverTap never stores or persists customer keys; only metadata, such as key name and version, is stored.</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/bring-your-own-key-byok-encryption" target="_blank">BYOK Encryption</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="security-and-project-settings" id="teams-structured-collaboration-with-enhanced-governance">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#teams-structured-collaboration-with-enhanced-governance"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Security & Project Settings" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Teams: Structured Collaboration with Enhanced Governance</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>Introducing Teams, a new way to organize and secure collaboration within CleverTap. Teams let you group users and information according to your organization’s structure, ensuring each team accesses only relevant data. This improves visibility, control, and data governance across large operations.</p>
    <p>With Teams, you can:</p>
    <p>
      <ul>
        <li>View and manage only the campaigns, templates, and data owned by your team.</li>
        <li>Define teams, assign users, and configure event-level access aligned with your business hierarchy.</li>
        <li>Work within a clean, focused team view and switch between teams seamlessly.</li>
        <li>Use API support for Campaign, Custom List Segment, and Email Template APIs.</li>
      </ul>
    </p>
    <p>Teams prevent cross-team data overlap, ensuring integrity, security, and operational efficiency across your organization.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/teams-setup" target="_blank">Teams Setup</a>.</p>
</div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="data-and-integrations" id="bulk-upload-for-geofences">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#bulk-upload-for-geofences"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg" alt="Data & Integrations" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Bulk Upload for Geofences</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now add multiple geo clusters and fences simultaneously using CSV or JSON files, enabling faster and more efficient setup of large-scale, location-based campaigns. Previously, each cluster and fence had to be added manually — a time-consuming process for campaigns involving hundreds of store locations or regions.</p>
    <p>With Bulk Upload, you can manage up to 10,000 radius-based geofences effortlessly, streamlining campaign setup for multi-location businesses.</p>
    <p>Key benefits include:</p>
    <p>
      <ul>
        <li>Faster setup: Upload multiple clusters and fences in a single step.</li>
        <li>Operational efficiency: Eliminate repetitive manual entry and reduce errors.</li>
        <li>Scalable targeting: Seamlessly manage large-scale, region-based campaigns.</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/geofencing-campaign-1#bulk-upload" target="_blank">Bulk Upload</a>.</p>
</div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="rcs-business-messaging-with-generic-provider-support">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#rcs-business-messaging-with-generic-provider-support"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">RCS Business Messaging with Generic Provider Support</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div> 
  </div>
  <div class="release-note-body">
    <p>You can now connect CleverTap with your preferred RCS provider through a simple configuration, keeping all orchestration, analytics, and automation in one place.</p>
    <p>With this feature, you can:</p>
    <p>
      <ul>
        <li>Bring your own RCS provider with a generic configuration.</li>
        <li>Drive engagement with rich media and two-way interactions that trigger campaigns and journeys.</li>
        <li>Maximize reach with automatic SMS fallback and dedicated RCS metrics for delivery, view, and click.</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/generic-rcs" target="_blank">Generic RCS</a> and<a href="https://developer.clevertap.com/docs/generic-rcs-api" target="_blank"> Generic RCS API</a>.</p>
</div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="end-to-end-pii-encryption-in-transit-for-sdks">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#end-to-end-pii-encryption-in-transit-for-sdks"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">End-to-End PII Encryption in Transit for SDKs</h3>
<div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap now offers enhanced encryption of all PII and sensitive data in transit between SDKs and backend servers.</p>

    <p>With this enhancement, you can:</p>
    <p>
      <ul>
        <li><strong>Ensure Secure Data Exchange:</strong> Encrypt all PII data transmitted from SDKs using AES-256 encryption, safeguarding against Man in the Middle attacks.</li>
        <li><strong>Prevent Network-Level Threats:</strong> Protect all SDK communication from man-in-the-middle (MITM) and data interception attempts, maintaining confidentiality throughout transmission.</li>
        <li><strong>Maintain Compliance Readiness:</strong> Meet financial-grade encryption standards and align with industry standards and enterprise security mandates, supporting fintech and other data-sensitive use cases.</li>
        <li><strong>Simplify Implementation:</strong> Manage encryption and decryption within the SDK, ensuring seamless, cross-platform protection across Android, iOS, Web, Cordova, Flutter, and React Native.</li>
      </ul>
    </p>
  <p>For more information, refer to <a href="https://developer.clevertap.com/docs/android-advanced-features#encryption-in-transit" target="_blank">Android</a>,
    <a href="https://developer.clevertap.com/docs/advanced-options-ios#encryption-of-pii-data" target="_blank">iOS</a>, <a href="https://developer.clevertap.com/docs/advanced-configurations#encryption-of-pii-data" target="_blank">Web</a>, <a href="https://developer.clevertap.com/docs/cordova-advance-features#encryption-for-pii-data" target="_blank"> Cordova</a>,<a href="https://developer.clevertap.com/docs/flutter-advanced-features#encryption-for-pii-data" target="_blank"> Flutter</a>, and <a href="https://developer.clevertap.com/docs/react-native-advanced-features#encryption-for-pii-data" target="_blank"> React Native</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

## October

<HTMLBlock>{`
<div class="release-note article" data-category="Campaigns" id="Nested-Objects-in-Custom-User-Properties-New-Feature">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Nested-Objects-in-Custom-User-Properties-New-Feature"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Nested Objects in Custom User Properties</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>Introducing Nested Objects in Custom User Properties, a powerful feature that simplifies how you represent and ingest complex user data in CleverTap. Define rich, structured entities such as insurance policies, subscriptions, or shopping carts using a JSON  eliminating the need to flatten data or manage multiple attributes across systems.</p>
    <p>With Nested Objects, you can:</p>
    <p>
      <ul>
        <li>Model structured user data natively within CleverTap, preserving relationships between entities.</li>
        <li>Build granular, condition-based segments using nested attributes (for example, filter users with a policy missing a beneficiary email).</li>
        <li>Simplify engineering workflows through direct JSON ingestion without additional data transformation.</li>
        <li>Visualize and filter nested data within Segment builder, unlocking deeper insights for marketers and analysts.</li>
      </ul>
    </p>
<p>For more information, refer to <a href="https://docs.clevertap.com/docs/nested-objects" target="_blank">Nested Objects</a> and<a href="https://developer.clevertap.com/docs/ingesting-nested-objects-via-clevertap-apis" target="_blank"> Ingesting Nested Objects via CleverTap APIs</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="Secure-File-Uploads-through-SFTP-Encryption-Enhancement">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Secure-File-Uploads-through-SFTP-Encryption-Enhancement"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Secure File Uploads through SFTP Encryption</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap now supports encrypted file uploads via SFTP, ensuring that all data ingested through the SFTP pipeline remains secure and compliant with data protection standards. You can safely transfer sensitive customer data using end-to-end PGP encryption and manage encryption keys flexibly.</p>
    <p>With SFTP Encryption, you can:</p>
    <p>
      <ul>
        <li>Protect all file transfers using PGP encryption.</li>
        <li>Choose between CleverTap-managed or customer-managed encryption keys.</li>
        <li>Continue using your existing ingestion workflows without disruption.</li>
        <li>Strengthen compliance and audit readiness for enterprise-grade security.</li>
      </ul>
    </p>
<p>For more information, refer to <a href="https://docs.clevertap.com/docs/file-upload-encryption" target="_blank">File Upload Encryption</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="Campaigns" id="custom-conversion-window">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#custom-conversion-window"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Custom Conversion Window</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>Introducing Custom Conversion Window, an enhancement to Campaigns and Journeys that gives marketers precise control over conversion tracking. You can now define custom conversion durations, from 1 minute to 5 months, instead of being limited to fixed options like 7 or 14 days. This enhancement brings greater flexibility, accuracy, and consistency, helping marketers align conversion measurement with real user behavior.</p>
    <p>With Custom Conversion Window, you can:</p>
    <p>
      <ul>
        <li>Track conversions accurately by aligning the window with your business cycle (for example, 10 days for e-commerce purchases, 72 hours for flash sales).</li>
        <li>Improve ROI accuracy by removing undercounting or overcounting from preset durations.</li>
        <li>Maintain consistency across reports and dashboards with unified data tracking.</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/create-message-push" target="_blank">Create Message</a> and<a href="https://docs.clevertap.com/docs/push-campaign-stats" target="_blank"> Stats</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

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

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="End-to-End-Encryption-for-CPaaS-Communication">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#End-to-End-Encryption-for-CPaaS-Communication"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" />
    </div>
    <h3 class="release-note-heading">End-to-End Encryption for CPaaS Communication</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge ga">GA</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap now supports end-to-end encryption for all CPaaS communications over Email and SMS via the Generic HTTP API configuration. This feature ensures every payload and callback is encrypted using AES-256, securing PII data such as email addresses and phone numbers.</p>
<p>With CPaaS Encryption, you can:</p>
    <p>
      <ul>
        <li>Protect outbound and inbound data with end-to-end encryption.</li>
        <li>Meet enterprise security and compliance requirements, and now meet BFSI-grade compliance requirements while maintaining performance and scalability.</li>
        <li>Enable encryption with a single toggle in the provider setup under Generic HTTP API configuration, supporting both CleverTap-managed and customer-managed keys (BYOK).</li>
        <li>Scale seamlessly across providers via the Generic HTTP API.</li>
        <li>Manage key versioning and rotation without service disruption.</li>
      </ul>
    </p>
<p>For more information, refer to <a href="https://docs.clevertap.com/docs/cpaas-encryptions" target="_blank">CPaaS Encryption</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="promotions" id="new-in-promotions-custom-rewards">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#new-in-promotions-custom-rewards"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/c65a9fbb8af21c3a8f01c546faa2089d52a3bf54c2efecc740879b1ea681242e-Property_1Selected.svg" alt="Promotions" />
    </div>
    <h3 class="release-note-heading">New in Promotions: Custom Rewards</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div> 
  </div>
  <div class="release-note-body">
    <p>Introducing Custom Rewards, a significant expansion of CleverTap’s Promo capabilities.
You can now create, host, and manage your own rewards within CleverTap promo and distribute it to tailored user segments through Promo campaigns. From physical and digital rewards (branded merchandise or OTT subscriptions) to self-managed wallets hosted on your end (real-money cashback or loyalty credits) you can do a webhook-based fulfillment to your systems.</p>
    <p>With Custom Rewards, you can:</p>
    <p>
      <ul>
        <li>Orchestrate personalized reward campaigns at scale by offering cashback in your hosted wallet for repeat buyers or issuing gift vouchers to users who achieve a milestone.</li>
        <li>Support diverse engagement use cases such as loyalty programs, event-based rewards, or promotional credits, without relying on fixed, built-in reward types.</li>
        <li>Simplify reward orchestration with a centralized catalog for all reward types, reducing operational complexity for marketing teams.</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/custom-rewards" target="_blank">Custom Rewards</a>.</p>
</div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="Campaigns" id="in-app-messages-improvements">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#in-app-messages-improvements"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">In-App Messages Improvements</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>

  <div class="release-note-body">
    <p>CleverTap’s enhanced In-App Messages empower marketers to create fully customizable, interactive, and high-converting campaigns without requiring code. These updates simplify campaign creation, lower time-to-market, and deliver delightful In-App experiences that drive engagement and conversions.</p>

    <p>The following features are now available based on your plan:</p>

    <ul>
      <li><b>Advanced In-App Builder:</b> Build visually rich In-App messages using a no-code, drag-and-drop editor with animations, flexible layouts, and layered elements. For more information, refer to <a href="https://docs.clevertap.com/docs/advanced-in-app-builder" target="_blank">Advanced In-App Builder</a>.</li>

      <li><b>Gamified Experiences:</b> Use pre-built “Spin the Wheel” and “Scratch Card” templates in the Custom HTML Builder to create engaging, reward-based campaigns. For more information, refer to <a href="https://docs.clevertap.com/docs/advanced-in-app-builder" target="_blank">In-App Gamification Templates</a>.</li>

      <li><b>Custom Code Templates:</b> Create native In-App templates and define custom actions, such as “granting coins” or “navigating to premium”, that marketers can trigger directly from the dashboard. For more information, refer to the Custom Code Templates for <a href="https://developer.clevertap.com/docs/ios-custom-code-in-app-templates" target="_blank">iOS</a>, <a href="https://developer.clevertap.com/docs/android-custom-code-in-app-templates" target="_blank">Android</a>, <a href="https://developer.clevertap.com/docs/react-native-custom-code-in-app-templates" target="_blank">React Native</a>, <a href="https://developer.clevertap.com/docs/flutter-custom-code-in-app-templates" target="_blank">Flutter</a>, and <a href="https://developer.clevertap.com/docs/cordova-custom-code-in-app-templates" target="_blank">Cordova</a>.</li>

      <li><b>Native Prompt Triggers:</b> Allows you to display OS-level prompts such as app rating requests or push pre-permissions within In-App campaigns. For more information on how to render native prompts, refer to <a href="https://docs.clevertap.com/docs/advanced-in-app-builder" target="_blank">Advanced In-App Builder</a>, <a href="https://docs.clevertap.com/docs/register-for-push" target="_blank">Push Primer</a>, <a href="https://docs.clevertap.com/docs/app-rating-primer" target="_blank">App Rating Primer</a>, and <a href="https://docs.clevertap.com/docs/app-functions#use-app-functions" target="_blank">App Functions</a>.</li>
    </ul>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<br />

## September

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="restore-discarded-custom-events-event-properties-and-user-properties">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#restore-discarded-custom-events-event-properties-and-user-properties"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" />
    </div>
    <h3 class="release-note-heading">Restore Discarded Custom Events, Event Properties, and User Properties</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge ga">GA</div>
  </div>

  <div class="release-note-body">
    <p>Admins can now restore discarded Custom Events, Event Properties, and User Properties within 24 hours of deletion. This safeguard prevents accidental removals from impacting analytics, segmentation, and campaign workflows.</p>
     <p>With this feature, you can:</p>
    <p>
      <ul>
        <li><strong>Protect Your Data:</strong> Recover deleted Custom Events, Event Properties, and User Properties within 24 hours.</li>
        <li><strong>Ensure Business Continuity:</strong> Restore accidentally removed items to avoid disruptions in campaigns and reporting.</li>
        <li><strong>Maintain Control:</strong> Restrict restore access to Admins to ensure security and accountability.</li>
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/schema" target="_blank">Schema</a>.</p>
</div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="updated-audit-logs-coverage-for-authentication-and-authorization">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#updated-audit-logs-coverage-for-authentication-and-authorization"><i class="fa-light fa-anchor"></i></a>
    </div>
    
<div>
  <img 
src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" />
    </div>
    <h3 class="release-note-heading">Updated Audit Logs Coverage for Authentication and Authorization</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge ga">GA</div>
  </div>
<div class="release-note-body">
    <p><p>We are excited to announce enhanced coverage of Audit Logs, expanding visibility into authentication and authorization events. This update strengthens compliance, audit readiness, and security monitoring across user management activities.</p>
    <p><strong>The following are the new events captured in Audit Logs:</strong></p>
    <p>
      <ul>
        <li><strong>User Invited:</strong> A new user was invited.</li>
        <li><strong>User Revoked:</strong> Access was revoked for an existing user.</li>
        <li><strong>User Deleted:</strong> A user was removed from the dashboard.</li>
        <li><strong>User Role Updated:</strong> The role of an active user was updated.</li>
        <li><strong>Role Created:</strong> A new role was created with specific permissions.</li>
        <li><strong>Role Edited:</strong> An existing role was modified.</li>
        <li><strong>Role Deleted:</strong> A role was removed from the account.</li>
        <li><strong>Password Reset:</strong> A user’s password was reset from the profile page.</li>
        <li><strong>Account Locked:</strong> Triggered after 20 consecutive failed login attempts.</li>
      </ul>
  </p>
<p>For more information, refer to <a href="https://docs.clevertap.com/docs/audit-logs"target="_blank">Audit Logs</a>.</p
</div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Attachments-in-Email-Campaigns">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Attachments-in-Email-Campaigns"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" " alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Attachments in Email Campaigns</h3>
  	<div class="badge private-beta">PRIVATE BETA</div>  
		<div class="badge new-feature">NEW FEATURE</div>
  </div>

  <div class="release-note-body">
    <p>You can now add attachments directly to your email campaigns, whether created from the dashboard or via API. This feature allows you to securely deliver files to your recipients without depending on external links.</p>
     <p>With this feature, you can:</p>
    <p>
      <ul>
        <li>Attach up to 10 files (PDF, JPG, PNG, GIF).</li>
        <li>Upload via local file picker, HTTPS URLs, or Content Manager.</li>
        <li>Preview attachments in the campaign overview.</li>
        <li>Send test emails with attachments.</li>
        <li>Deliver to CC/BCC recipients.</li> 
      </ul>
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/using-attachments-in-email" target="_blank">Using Attachments in Email</a> and <a href="https://developer.clevertap.com/docs/create-campaign-api-with-email-attachment" target="_blank">Add Attachments via Campaign API</a>.</p>
</div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="Campaigns" id="Improved-Anonymous-to-Identified-Profile-Merge-Behavior">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Improved-Anonymous-to-Identified-Profile-Merge-Behavior"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Improved Anonymous-to-Identified Profile Merge Behavior</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge ga">GA</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to announce how CleverTap handles anonymous-to-identified profile merges. From now on, any anonymous events from a second device or later ingested after the feature is enabled seamlessly flow into the corresponding identified profile upon a merge, unlocking richer insights, more accurate segmentation, and complete funnel analytics across all devices.</p>

    <p>With this enhancement, the following changes are implemented:</p>

    <ul>
      <li><strong>Complete Transfer of Anonymous Events:</strong> All anonymous events created on second, third, or later devices merge directly into the identified profile on login.</li>
      <li><strong>Inclusive Segmentation & Funnels:</strong> Transferred events are fully usable in segmentation, funnels, flows, and engagement targeting, with no more greyed-out or “blacklisted” data points.</li>
      <li><strong>No Initial Event Limits:</strong> For this initial release, the number of post-rollout events that can be transferred is unlimited. (A generous lookback period may be introduced in future iterations.)</li>
      <li><strong>Historical Data Remains Unchanged:</strong> Events generated before the feature rollout remain the same, so customer historical data stays stable and reliable.</li>
    </ul>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="automated-expiry-alerts-for-sso-saml-certificate">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#automated-expiry-alerts-for-sso-saml-certificate"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" />
    </div>
    <h3 class="release-note-heading">Automated Expiry Alerts for SSO SAML Certificate</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge ga">GA</div>
  </div>

  <div class="release-note-body">
    <p>SSO now sends automated expiry alerts that notify Admins as SAML certificates near expiry—enabling timely updates, preventing login disruptions, and removing reliance on manual reminders.</p>
    <p>With this enhancement, you can:</p>
    <p>
      <ul>
        <li>Receive proactive alerts starting 30 days before expiry, sent weekly until updated.</li>
        <li>Stay informed via Email and the CleverTap dashboard.</li>
        <li>Restrict visibility to Admins for precise actioning.</li>
        <li>Stop alerts automatically once the SAML certificate is updated.</li>
      </ul>
    </p>
  <p>For more information on updating the SAML certificate, refer to <a href "https://docs.clevertap.com/docs/single-sign-on-sso#update-renewed-sso-certificate" target="_blank">Single Sign On (SSO)</a>.</p>
 </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="Campaigns" id="email-alerts-for-nearing-fair-usage-policy-fup-limits">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#email-alerts-for-nearing-fair-usage-policy-fup-limits"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Email Alerts for Nearing Fair Usage Policy (FUP) Limits</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
<div class="release-note-body">
    <p>We’re introducing automated email alerts to help Admins proactively manage event consumption and avoid service interruptions.</p>
    <p>Alerts trigger as usage approaches defined thresholds, enabling timely action and keeping teams informed to maintain business continuity.</p>
    <p>With this feature, you can:</p>
    <p>
      <ul>
        <li>Receive alerts at 75%, 90%, and 100% of allocated capacity.</li>
        <li>Keep stakeholders informed in real time to prevent overages and ensure continuity.</li>
      </ul>
    </p>
</div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Email-Subscription-Status-in-Get-User-Profile-API">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Email-Subscription-Status-in-Get-User-Profile-API"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" " alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Email Subscription Status in Get User Profile API</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>                              
  </div>
  <div class="release-note-body">
    <p>The Get User Profile API now returns a user’s email subscription status, providing a unified and real-time consent check for both the overall email channel and individual subscription groups.</p>
<p>For more information, refer to <a href="https://developer.clevertap.com/docs/email-subscription-details-via-api"target="_blank">Get User Profiles</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<div class="release-note article" data-category="Campaigns" id="Improved-Limits-in-Campaigns-and-Journeys">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Improved-Limits-in-Campaigns-and-Journeys"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Improved Limits in Campaigns and Journeys</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now cap the total number of times a user ever receives a specific Campaign or Journey message. This new lifetime limit option is available alongside existing choices to send every time or at intervals.</p>
    <p>Enhanced Limits help marketers reduce message fatigue, enforce governance, and protect customer experience by preventing over-saturation of onboarding, promotional, or reminder messages.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/notification-delivery-options-1#limits-for-engagements" target="_blank">Limits for Engagements</a>.</p>
  </div>
  <hr/>
</div>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Single-Image-Annotations-for-Gmail-Promotions-Tab">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Single-Image-Annotations-for-Gmail-Promotions-Tab"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" " alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Single Image Annotations for Gmail Promotions Tab</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>                              
  </div>
  <div class="release-note-body">
    <p>You can now add a single image to your marketing email preview in Gmail’s Promotions tab, making it more visual, discoverable, and engaging.

With this enhancement, you can:</p>
    <ul>
      <li>Add a standalone image or pair it with deal annotations, such as coupon codes, discounts, expiry dates, and badges.</li>
      <li>Stand out in crowded inboxes with a simple setup and flexible options.</li>
			<li>Use a single image for brand impact or showcase multiple products through the existing Product Carousel annotations feature.</li>
</ul>
<p>For more information, refer to <a href="https://docs.clevertap.com/docs/gmail-annotations-promotion-cards"target="_blank">Gmail Promotional Annotations</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Advanced-Web-Pop-up-Builder">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Advanced-Web-Pop-up-Builder"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Advanced Web Pop-up Builder</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>The Advanced Web Pop-up Builder lets you design and publish fully custom, on-brand web pop-ups without developer support. This feature includes a drag-and-drop editor, flexible layouts, advanced styling, custom backgrounds, animations, and device-specific designs with live previews.</p>
    <p>With this update, you can:</p>
    <p>
      <ul>
        <li>Launch campaigns faster with marketer autonomy</li>
        <li>Customize beyond standard templates with deeper styling options</li>
        <li>Experiment effortlessly through A/B testing</li>
        <li>Deliver consistent, responsive experiences across devices</li>
      </ul>
    </p>
 <div class="release-note-image">
    <div style="text-align: center;">
 			<img src="https://files.readme.io/5b1658e304b13c4612022e8966ead0b127665078c182bbada0c0d9354cf071fc-Advanced.png" alt="Advanced Web Pop-up Builder" style="max-width: 100%; height: auto;" />
      <p class="caption">Advanced Web Pop-up Builder</p>
    </div>
  </div>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/advanced-web-pop-up-builder" target="_blank">Advanced Web Pop-up Builder</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<div class="release-note article" data-category="Campaigns" id="Enhanced-Limits-in-Campaigns-and-Journeys">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Enhanced-Limits-in-Campaigns-and-Journeys"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Enhanced Limits in Campaigns and Journeys</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>Enhanced Limits help marketers reduce message fatigue, enforce governance, and protect customer experience by preventing over-saturation of onboarding, promotional, or reminder messages.
</p>
    <p>You can now cap the total number of times a user ever receives a specific campaign or journey message. This new lifetime limit option is available alongside existing choices to send every time or at intervals.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/notification-delivery-options-1#limits-for-engagements" target="_blank">Limits for Engagements</a>.</p>
  </div>
  <hr/>
</div>

<HTMLBlock>{`
<div class="release-note article" data-category="promotions" id="Promotions-Add-on-for-CleverTap-Essentials-Plan">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Promotions-Add-on-for-CleverTap-Essentials-Plan"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/c65a9fbb8af21c3a8f01c546faa2089d52a3bf54c2efecc740879b1ea681242e-Property_1Selected.svg" alt="Promotions" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Promotions Add-on for CleverTap Essentials Plan</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>The Promotions Add-on is now available with the CleverTap Essentials Plan. With this add-on, you can use the Promotions feature to deliver loyalty points, discount coupons, and partner vouchers at scale, without needing external systems.</p>
    <p>To enable the Promotions Add-on from the CleverTap dashboard, purchase the add-on, configure your loyalty wallets, coupons, partner voucher settings, and start running reward-based campaigns across apps, websites, and POS systems.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/promo-campaigns" target="_blank">Promo Campaigns</a>.</p>
    <div class="release-note-image">
    <div style="text-align: center;">
 			<img src="https://files.readme.io/482444a7d4b516a9647b2a4655358166a86e2a826a733d4892eea7300c5906f1-image.png" alt="Promo Add-on" style="max-width: 100%; height: auto;" />
      <p class="caption">Promo Add-on</p>
    </div>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

## August

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Enhanced-Generic-SMTP-Email-Integration-with-Deeper-Analytics">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Enhanced-Generic-SMTP-Email-Integration-with-Deeper-Analytics"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" " alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Enhanced Generic SMTP Email Integration with Deeper Analytics</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>                              
  </div>
  <div class="release-note-body">
    <p>Generic SMTP email integration now provides deeper insights into email campaigns, enabling better decision-making and performance analysis.

With this enhancement, you can:</p>
    <ul>
      <li>Track successful email delivery across User Profiles, Campaign Stats, Provider Stats, Exports, and Reports.</li>
      <li>Gain visibility into errors such as Soft Bounce, Hard Bounce, Spam, and Unsubscribed, with details available in Campaign Stats, Notification Failed Events, Exports, Reports, and Provider Stats.</li>
      <li>Analyze email performance and make data-driven decisions with precise performance metrics.</li>
 </ul>
<p>For more information, refer to <a href="https://docs.clevertap.com/docs/generic-smtp-v2-payload"target="_blank">Generic SMTP</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Generic-HTTP-Email-Integration">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Generic-HTTP-Email-Integration"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" " alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Generic HTTP Email Integration</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>                              
  </div>
  <div class="release-note-body">
    <p>The new Generic HTTP Email integration makes connecting your email provider with CleverTap easy using just an API URL, key, and request body. It works with any provider that supports HTTP/HTTPS and allows you to add personalization, custom headers, and batch sends.

With this integration, you can:</p>
    <ul>
      <li>Track delivered, bounced, or unsubscribed events via HTTP callbacks.</li>
      <li>View delivery success or failure across campaign stats reports, exports, and user profiles.</li>
 </ul>
<p>For more information, refer to <a href="https://docs.clevertap.com/docs/generic-http"target="_blank">Generic HTTP</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Domain Whitelisting for Data Ingestion via Web SDK">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Domain Whitelisting for Data Ingestion via Web SDK"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" " alt="Enhanced-Push-Notifications-for-Smarter,-Faster-Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Domain Whitelisting for Data Ingestion via Web SDK</h3>
    <div class="badge new-feature">ENHANCEMENT</div>                           
  </div>
  <div class="release-note-body">
    <p>Domain Whitelisting for the Web SDK allows you to define a list of approved domains, ensuring that only trusted sources can send data into your CleverTap account.
What this means for you:</p>
    <ul>
      <li> <strong> Secure Your Data: </strong>Only trusted domains can send data to your CleverTap project</li>
      <li> <strong> Protect Campaigns: </strong>Prevent failures caused by unauthorized or malformed data</li>
      <li> <strong> Support Compliance: </strong>Meet audit requirements from security and compliance teams</li>
</ul>  
 <p> For more information, refer to <a href="https://docs.clevertap.com/docs/domain-whitelisting"target="_blank">Domain Whitelisting for Web SDK.</a></p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<br />

<div class="release-note article" data-category="Campaigns" id="Domain-Whitelisting-for-Web-SDK">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Domain-Whitelisting-for-Web-SDK"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Domain Whitelisting for Web SDK</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge ga">GA</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap now supports Domain Whitelisting for data ingestion through the Web SDK. Customers can approve specific domains, ensuring only trusted sources send data to CleverTap.</p>
    <p>This update prevents unauthorized data ingestion, reducing risks of data pollution, billing abuse, and invalid campaign triggers.</p>
    <p>Key benefits include:</p>
    <p>
      <ul>
        <li>Stronger data security by blocking unapproved domains</li>
        <li>Safeguarded campaigns with cleaner event data</li>
        <li>Operational control over allowed domains</li>
        <li>Compliance support for audits and security reviews</li>
      </ul>
    </p>
  </div>
  <hr/>
</div>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Improved-Push-Notifications-for-Smarter,-Faster-Campaigns">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Imporved-Push-Notifications-for-Smarter,-Faster-Campaigns"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" " alt="Enhanced-Push-Notifications-for-Smarter,-Faster-Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Improved Push Notifications for Smarter, Faster Campaigns</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>                              
  </div>
  <div class="release-note-body">
    <p>The Push Notification channel now includes key enhancements that make campaign creation easier and help you deliver higher-quality messages. 

These key enhancements allow you to:</p>
    <ul>
      <li> <strong> Work with Flexible Templates:</strong> Choose from Text over Image (Zero Bezel), Advanced (Basic), Auto Carousel, Timer, and Standard templates and define CTAs.</li>
      <li> <strong> Preview and Test your Notifications:</strong>  See real-time previews across Android/iOS versions and dark/light modes (collapsed and expanded states). Preview and Test your designs before sending.</li>
      <li> <strong> Design with More Control:</strong>  Use the redesigned WHAT section with structured left navigation for Content, Android and iOS options, and Post Action Webhook. Fine-tune media rendering with new Image Scaling options.</li>
 </ul>
<h3 class="release-note-heading">SDK Compatibility</h3>
                                
To access these enhancements, ensure that your app is integrated with the following SDK versions: </p>
   <ul> 
   <li> Android SDK v7.3.0 and above </li>
   <li> CT Push Templates SDK v2.1.0 and above </li>
   <li> iOS CTNotificationContent SDK v1.1.0 and above </li>
   </ul>
 <p> Campaigns with existing templates continue to work seamlessly. For more information, refer to <a href="https://docs.clevertap.com/docs/push-editor"target="_blank">Push Editor</a>, <a href= "https://developer.clevertap.com/docs/android-push-templates"target="_blank">Android Push Templates</a>, <a href= "https://developer.clevertap.com/docs/ios-rich-push-notifications-v2"target="_blank">iOS Rich Push Notifications</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

## July

<HTMLBlock>{`
<div class="release-note article" data-category="security-&-project-settings" id="Link-Events-to-User-Properties">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Link-Events-to-User-Properties"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Link-Events-to-User-Properties" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Link Events to User Properties</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>The new capability to link events to user properties allows you to trigger campaigns, conversions, and exits when a user property changes. It also supports real-time, personalized messaging based on profile changes, enabling immediate responses to user behavior.

For example, a gaming app can link the Game Level Upgraded event to the Game Level user property to automatically trigger a reward campaign when the level increases.

The following key capabilities are included in this release:</p>
    <ul>
      <li>Link an event to a user property only if the user property is active.</li>
      <li>Discard linked events when these events are no longer needed</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/schema#create-linked-event-for-user-property"target="_blank">Create Linked Events for User Properties</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="settings" id="Role-Based-Channel-Level-Access-for-Campaigns-and-Journeys">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Role-Based-Channel-Level-Access-for-Campaigns-and-Journeys"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Role-Based-Channel-Level-Access-for-Campaigns-and-Journeys" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Role-Based Channel-Level Access for Campaigns and Journeys</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to announce Role based Channel-Level Access for Campaigns and Journeys, giving admins more precise control over who can manage each messaging channel. With this enhancement, admins can now define channel-specific permissions, so users can only view or manage the channels for which they are responsible (such as Push, Email, SMS, Web Push, App Inbox, and so on). Here are some key features:</p>
    <ul>
      <li><strong>Granular Permissions</strong>: Assign channel-level read or write access within Campaigns and Journeys.</li>
      <li> <strong>Governance at Scale</strong>: Prevent accidental edits by limiting control to authorized users.</li>
      <li> <strong>Built for Multi-Team Orgs</strong>: Support business units managing different channels independently. </li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/role-based-access-control-advance-governance#engagement-permissions" target="_blank">Engagement Permissions</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="promotions" id="CleverTap-Promotions">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#CleverTap-Promotions"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/c65a9fbb8af21c3a8f01c546faa2089d52a3bf54c2efecc740879b1ea681242e-Property_1Selected.svg" alt="Promo-Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">CleverTap Promotions</h3>
    <div class="badge new-feature">New Feature</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap introduces the Promotions feature, which was earlier in Public Beta, and is now generally available. Promotions enable brands to reward users at scale with loyalty points, discount coupons, and partner vouchers. This release allows brands to create personalized reward campaigns across mobile apps, websites, and POS systems.</p>
    
    <p>The feature includes the following key features:</p>
      <ul>
        <li><strong>Loyalty Wallets:</strong> Launch digital wallets that let users earn and redeem loyalty points from campaigns, cashback coupons, APIs, or manual top-ups, with real-time balance updates and seamless checkout redemption. For more information, refer to <a href="https://docs.clevertap.com/docs/loyalty-wallets" target="_blank">Loyalty Wallets</a>.</li>
        <li><strong>Coupons:</strong> Create personalized fixed coupon codes or unique bulk coupon codes with flexible rules based on user profile, cart value, product category, and time. Distribute via Promo campaigns and use APIs for real-time validation and redemption. This ensures reliable coupon usage in high-volume transactions. For more information, refer to <a href="https://docs.clevertap.com/docs/coupons" target="_blank">Coupons</a>.</li>
        <li><strong>Partner Vouchers:</strong> Upload and assign third-party brand vouchers to your users. Scalable assignment logic supports multiple partner voucher programs in parallel, each with voucher lists containing millions of codes. For more information, refer to <a href="https://docs.clevertap.com/docs/partner-vouchers" target="_blank">Partner Vouchers</a>.</li>
        <li><strong>Promo Campaigns:</strong> Run loyalty campaigns at scale based on past behaviors or real-time user actions, giving points, coupons, or partner vouchers directly from the CleverTap dashboard. Supports concurrent campaigns for personalized, high-impact experiences. For more information, refer to <a href="https://docs.clevertap.com/docs/promo-campaigns" target="_blank">Promo Campaigns</a>.</li>
        <li><strong>Promo APIs:</strong> Enable real-time loyalty experiences directly within a client app, website, or POS system, ensuring fast, seamless integration across all user touchpoints. For more information, refer to <a href="https://developer.clevertap.com/docs/promo-apis" target="_blank">Promo APIs</a>.</li>
      </ul>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Custom Templates for Advanced Web Personalization">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Custom Templates for Advanced Web Personalization"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Custom Templates for Advanced Web Personalization</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>We have introduced two new templates under Advanced Web Personalization to help you deliver richer, more dynamic web campaigns. CleverTap customers can now use the following templates: </p>
    <ul>
      <li><strong>Custom HTML Templates:</strong> Use your HTML/CSS/JS code to design personalized Web Native Display campaigns, directly within a built-in code editor.</li>
      <li><strong>Custom JSON Templates:</strong> Dynamically render web content using JSON passed from your end when users meet campaign criteria.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/advanced-personalization#custom-templates" target="_blank">Custom Templates</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Hyper-personalized Experiences With Support For Personalization In Push & Email">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Hyper-personalized Experiences With Support For Personalization In Push & Email"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Hyper-personalized Experiences With Support For Personalization In Push & Email</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>You can now test personalized content for both Push Notifications and Email using test or internal profiles before launching your campaign. With this feature, you gain deeper insights into end-user experience, helping you debug potential errors. It provides seamless support for various personalization features such as @Personalization, Liquid Tags, Linked Content, and Constant Event Properties, so you can check if the peronsalization renders as intended for the end users.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/send-test-personalization-for-push" target="_blank">Send Test Personalization for Push</a> and <a href="https://docs.clevertap.com/docs/send-test-personalization-for-email" target="_blank">  Send Test Personalization for Email</a> </p> 
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Facebook-Audiences">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Facebook-Audiences"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Facebook Audiences</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p> You can now add multiple Facebook Ad Accounts, create custom-named audiences without linking to Ad Sets, and use control groups to measure incremental impact with the revamped Facebook Audience Export. The update also allows modifying existing audiences and tracks Sent and Failed events to make campaign stats actionable.</p>
    <p>For more information, refer to the following documents:</p>
    <ul>
      <li><a href="https://docs.clevertap.com/docs/facebook-audiences-private-beta" target="_blank">Facebook Audiences</a></li>
      <li><a href="https://docs.clevertap.com/docs/facebook-audience-setup-private-beta" target="_blank">Facebook Audiences - Setup</a></li>
      <li><a href="https://docs.clevertap.com/docs/facebook-audiences-create-message-private-message" target="_blank">Facebook Audiences - Create Message</a></li>
      <li><a href="https://docs.clevertap.com/docs/facebook-audiences-stats-private-beta" target="_blank">Facebook Audiences - Stats</a></li>
<li><a href="https://docs.clevertap.com/docs/facebook-audiences-stats-private-beta" target="_blank">Facebook Audiences - Troubleshooting and FAQs</a></li>
    </ul>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Notification-Failed-Event-for-WhatsApp-Analytics">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Notification-Failed-Event-for-WhatsApp-Analytics"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Notification Failed Event for WhatsApp Analytics</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>Announcing a significant enhancement to our WhatsApp Analytics: the <strong>Notification Failed</strong> event that gives you more deeper insights into campaign errors. With this update, CleverTap captures a <em>Notification Failed</em> event, along with the reason for failure, enabling better targeting and resolution.</p>
    <ul>
      <li><strong>Improved Targeting:</strong> Target users through alternate channels when errors occur. For example, if users encounter soft bounce errors, you can re-target them via other channels.</li>
      <li><strong>Error Analysis:</strong> Analyze the root causes of errors to resolve issues and optimize future engagements.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/events#:~:text=Notification%20Failed,in%20the%20campaign" target="_blank">Notification Failed Event</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Upload-HTML-ZIP-Email-Templates">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Upload-HTML-ZIP-Email-Templates"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Upload HTML (.ZIP) to Create Email Templates</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now upload a ZIP file containing your custom HTML and referenced image assets to create email templates in CleverTap.</p>
    <p>This enhancement is ideal for teams using external design tools or working with agencies. CleverTap automatically converts the uploaded .ZIP file into a reusable email template and saves all associated assets to the Content Manager.</p>
    <p>There are two ways to upload custom html .ZIP file: either through the CMS or directly during campaign creation. For more information, refer to the following documents:</p>
    <ul>
      <li><a href="https://docs.clevertap.com/docs/content-manager-templates-upload-html#upload-html-templates-using-zip-file" target="_blank">Upload via CMS</a></li>
      <li><a href="https://docs.clevertap.com/docs/email-editor-upload-html-zip#upload-html-templates-using-zip-files" target="_blank">Upload through Campaign Creation</a></li>
    </ul>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="App-Functions-for-Push-Primer-and-App-Rating">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#App-Functions-for-Push-Primer-and-App-Rating"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
		<img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">App Functions for Push Primer and App Rating</h3>
    <div class="badge private-beta">PRIVATE BETA</div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap has introduced <strong>App Functions</strong>, a new capability in In-App Campaigns that lets you trigger native system prompts directly from CleverTap.</p>
    <p>This release includes the following two System App Functions:</p>
    <ul>
      <li><strong>Request Push Permission</strong>: Prompt users with the native OS dialog.</li>
      <li> <strong>Request App Rating</strong>: Ask satisfied users to leave an in-app review.</li>
    </ul>
    <p>You can use these as standalone campaigns or as button actions in the Advanced In-app Builder. CleverTap automatically handles targeting logic, including cases where users have previously opted out.</p>
    <p><strong>Availability:</strong><li>Android SDK 7.4.0 and highher</li><li>iOS SDK 7.2.0 and higher</li></p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/app-functions" target="_blank">App Functions</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="analytics" id="Boards-2.0-Smarter-Dashboarding">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Boards-2.0-Smarter-Dashboarding"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Boards 2.0: Smarter Dashboarding</h3>
    <div class="badge private-beta">PRIVATE BETA</div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>Boards 2.0 is now available in Private Beta, offering a faster, more flexible way to create dashboards with visuals from <a href="https://staging.docs.user.clevertap.net/docs/trends-v2" target="_blank">Trends 2.0</a> and <a href="https://staging.docs.user.clevertap.net/docs/funnels-v2" target="_blank">Funnels 2.0</a>.</p>
    <p>This revamped experience makes it easier to analyze, compare, and present insights with minimal friction.</p>
    <p>Boards 2.0 includes the following enhancements:</p>
    <ul>
      <li>Pin updated widgets: Trend Charts, Bar Charts, Number Tiles, and Funnels</li>
      <li>Compare data across different time periods</li>
      <li>Edit filters directly on individual charts</li>
      <li>Resize widgets with more layout flexibility</li>
      <li>Improved tooltips for deeper insights</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/custom-boards-v2" target="_blank">Boards 2.0</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Out-of-the-Box-HTML-and-AMP-Email-Templates">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Out-of-the-Box-HTML-and-AMP-Email-Templates"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Introducing Out-of-the-Box HTML and AMP Email Templates</h3>
    <div class="badge private-beta">PRIVATE BETA</div>
		<div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap now offers 40+ new Out-of-the-Box HTML and AMP Email templates to help you accelerate email campaign creation.</p>
    <p>These ready-to-use templates are fully customizable, simplify campaign setup, and are designed to support the most common marketing and transactional journeys. Whether you want to welcome new users, send promotional offers, or share account updates, the templates let you go live faster with minimal design or development effort.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/ootb-email-templates" target="_blank">Email Templates</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="data-and-integrations" id="Technology-Partner-Integrations">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Technology-Partner-Integrations"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/bf86621cc6be2995b3a9323ccfcaae0e172d6da76b2bfedc7983c5be75eb179d-Partners_Icon_Outlined.svg" alt="Data & Integrations" />
    </div>
    <div><h3>100+ Technology Partner Integrations Now Available</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>

  <div class="release-note-body">
    <p>We’re excited to announce a significant expansion of the CleverTap Partner ecosystem, with over <strong>100+ technology integrations</strong>. These integrations are designed to help you personalize at scale, automate with ease, and deliver seamless omnichannel experiences across every stage of the customer journey.</p>

    <h4>Integration Summary</h4>
<p>Here’s a breakdown of key categories + notable partners to help you get started:</p>
    <ul>
      <li><strong>CRM Integrations</strong> → Leverage customer data with <strong>Leadsquared</strong>.</li>
      <li><strong>Localization</strong> → Deliver region/language-based experiences with <strong>Lokalise</strong>, <strong>Crowdin</strong>.</li>
      <li><strong>Dynamic Content</strong> → Auto-personalize creatives using <strong>Movable Ink</strong>, <strong>Litmus</strong>, <strong>Jasper.ai</strong>, <strong>Rocketium</strong>, <strong>SurveyMonkey</strong>.</li>
      <li><strong>Email Templates Management</strong> → Build emails faster with <strong>Stripo</strong>, <strong>Alpaco</strong>.</li>
      <li><strong>Direct Mail</strong> → Run physical + digital campaigns with <strong>Optilyz</strong>, <strong>Inkit</strong>.</li>
      <li><strong>Contextual Location</strong> → Trigger campaigns based on user location with <strong>Radar</strong>, <strong>Accuweather</strong>.</li>
      <li><strong>Payments</strong> → Power subscriptions & In-App purchases via <strong>Purchasely</strong>, <strong>Qonversion</strong>.</li>
      <li><strong>Workflow Automation</strong> → Automate tasks with <strong>Pipedream</strong>, <strong>SheetsDB</strong>, <strong>SheetLabs</strong>.</li>
    </ul>

    <h4>Value Proposition</h4>
    <ul>
      <li><strong>Expanding Campaign Reach</strong> → Integrate seamlessly with your martech stack.</li>
      <li><strong>Enhancing Personalization</strong> → Dynamically adapt campaigns based on users’ profiles, locations, and preferences.</li>
      <li><strong>Accelerating Time-to-Market</strong> → Leverage ready integrations without dev effort.</li>
    </ul>

    <h4>Availability</h4>
 <p>
  Refer to the 
  <a href="https://docs.clevertap.com/docs/technology-partners" target="_blank" rel="noopener">
    Technology Partners Directory
  </a> 
  to integrate these partners.
</p>
    <p>
      If you cannot find your required partner, submit your request to:
      <a href="mailto:integrations@clevertap.com">integrations@clevertap.com</a>
    </p>

    <div style="text-align: center;">
      <img src="https://files.readme.io/aceb603a9976fde9cfefd1c014780116fcffb6a351545441e13784d21f2353d8-clevertap_solar_system_1.png" alt="Technology Partner Integrations" style="max-width: 100%; height: auto;" />
      <div style="font-size: 14px; color: #555; margin-top: 8px;"><em>Technology Partner Integrations</em></p></div>
      <hr>
    </div>
  </div>
</div>
`}</HTMLBlock>

## June

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="Import-Shopify-Historical-Data-to-CleverTap">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Import-Shopify-Historical-Data-to-CleverTap"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" /></div>
    <div><h3>Import Shopify Historical Data to CleverTap</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap now supports importing historical user and order data from Shopify, making onboarding faster and smarter. Customers integrating via the Shopify Plugin can now upload existing profile and charged event data, eliminating the need to start from scratch.</p><p> With this update, you can:<li>Bring past user and order data into CleverTap from day one</li><li>Use historical data to segment and engage users instantly</li><li>Preserve key events for better analytics and decision-making</li></p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/shopify#import-existing-shopify-data-into-clevertap" target="_blank">Import Existing Shopify Data into CleverTap.</a></p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<br />

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Marketing-Lite-API-for-WhatsApp-Direct">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Marketing-Lite-API-for-WhatsApp-Direct"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Marketing Lite API for WhatsApp Direct</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>Marketing Lite API is now generally available for all WhatsApp Direct customers, offering a faster, simpler, and more cost-effective way to launch campaigns—especially with the new WhatsApp pricing effective July 1. This API requires no development effort, allows instant activation, and provides control over how long Meta retries message delivery for both marketing and utility templates. It also offers deeper performance insights such as message reads, link clicks, and conversions, and has demonstrated up to 9% higher delivery rates in India for high-engagement campaigns, driven by dynamic delivery scaling based on user responsiveness.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/whatsapp-marketing-messages-lite-api" target="_blank">Marketing Lite API for WhatsApp Direct.</a></p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="security-project-settings" id="Branded-Domain-Support-SMS-WhatsApp">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Cart-Recovery-with-the-Enhanced-Shopify-Plugin">
        <i class="fa-light fa-anchor"></i>
      </a>
    </div>
    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Cart Recovery with the Enhanced Shopify Plugin</h3>
    <div class="badges">
      <div class="badge enhancement">ENHANCEMENT</div>
    </div>
  </div>

  <div class="release-note-body">
    <p>
      We have rolled out a powerful update to the Shopify Plugin making abandoned cart recovery faster and easier to set up.
CleverTap now auto-syncs your product catalog and cart data in a structured format using new Catalog Sync and Cart Tracking toggles, with no developer work required. 
    </p>
    <p>
      With this update, you get:<li><b>Automated Catalog Sync</b>:Keep product data fresh with daily updates.</li><li><b>Smarter Personalization</b>: Use Liquid tags to dynamically insert product information.</li><li><b>Time Savings</b>: Eliminate manual setup and integration hassles.</li><li><b>Higher Conversions</b>: Launch personalized, multi-product cart recovery campaigns that convert.</li>
    </p>
    <p>
      For more information, refer to 
      <a href="https://docs.clevertap.com/docs/shopify#cart-abandonment-use-case" target="_blank">Cart Abandonment Use Case</a>.
    </p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="content-manager" id="Reusable-Content-Blocks">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Reusable-Content-Blocks"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg" alt="Content Manager" /></div>
    <div><h3>Introducing Reusable Content Blocks for Greater Efficiency</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to introduce Content Blocks in CleverTap’s Content Manager. Content Blocks are reusable snippets for standardized elements, such as footers, logos, or disclaimers.</p>
  <div style="text-align: center;">
  <img src="https://files.readme.io/686373549b6ac569fd3abb3ab7bafddabdd0b37236d60ce08b551e2a559309e1-image.png" alt="Footer Standardization with Content Blocks" />
  <p class="caption" style="margin-top: 8px;"><em>Footer Standardization with Content Blocks</em></p>
</div>
    <p>These blocks are designed to simplify the reuse of content across email campaigns, saving you valuable time. They help you maintain consistent messaging and standardize your brand communication.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/content-blocks" target="_blank">Content Blocks</a> and <a href="https://developer.clevertap.com/docs/content-blocks-api" target="_blank">Content Block APIs</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Role-Based Privileges for Global Campaign and Throttle Limits">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Role-Based Privileges for Global Campaign and Throttle Limits"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Role-Based Privileges for Global Campaign and Throttle Limits</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>WWe have added a new layer of governance to help teams manage communication frequency and scale, with role-based control over <strong>Global Campaign Limits</strong> and <strong>Global Throttle Limits</strong>.</p>
    <p>Admins can now define who can override Campaign and Throttle Limit settings based on user roles.</p>
    <p>With this feature, you can:</p>
    <ul>
      <li>Prevent over-communication </li>
      <li>Enable fine-grained control </li>
      <li>Extend support to Journeys </li>
      <li>Retain backward compatibility </li>
    </ul>
    <p>For more information, refer to the <a href="https://docs.clevertap.com/docs/role-based-access-control-advanced-governance-limits" target="_blank">Setup Roles</a> and <a href="https://docs.clevertap.com/docs/campaign-permissions" target="_blank">Campaign Permissions</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Banner-Ads-InApps">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Banner-Ads-InApps"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Banner Ads Support in In-Apps</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge beta">BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now create no-code <b>Banner Ads</b> using the Advanced In-App Builder. This non-intrusive format appears as a header or footer in your app without blocking usage.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/advanced-in-app-builder#banners" target="_blank">Banners</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

## May

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Branded-Domain-Support-SMS-WhatsApp">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Branded-Domain-Support-SMS-WhatsApp">
        <i class="fa-light fa-anchor"></i>
      </a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Branded Domain Support for SMS and WhatsApp Campaigns</h3>
    <div class="badges">
      <div class="badge enhancement">ENHANCEMENT</div>
      <div class="badge private-beta">PRIVATE BETA</div>
    </div>
  </div>

  <div class="release-note-body">
    <p>
      You can now deliver trustworthy, branded short links with real-time click tracking without any effort.
    </p>
    <p>
      CleverTap’s new link-shortening feature lets you create on-brand short URLs inside SMS and WhatsApp campaigns. With each click tracked in real time, you gain visibility into who clicked, when, and from which campaign message. This release also eliminates TRAI compliance overhead by using only whitelisted domains, ensuring seamless delivery across regulated markets.
    </p>
    <p>
      For more information, refer to 
      <a href="https://docs.clevertap.com/docs/branded-domain" target="_blank">Branded Domain</a>.
    </p>
  </div>
  
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Elevate-Your-Marketing-Strategy-with-TikTok-Remarketing">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Elevate-Your-Marketing-Strategy-with-TikTok-Remarketing"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
      <h3 class="release-note-heading">Elevate Your Marketing Strategy with TikTok Remarketing</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to announce that CleverTap now supports TikTok as a remarketing channel. This integration empowers our customers to leverage CleverTap’s powerful segmentation capabilities to upload user data into TikTok Audiences, enabling advanced retargeting campaigns.</p>
   <div style="text-align: center;">
  <img src="https://files.readme.io/8989db3a6e9d984763aac232b75f7cee3e0cf1b269109c2653bf85970623f078-image.png" alt="TikTok Remarketing" />
  <p class="caption" style="margin-top: 8px;"><em>TikTok Remarketing</em></p>
</div>
    <p>Maximize your reach with targeted TikTok ads by:</p>
    <ul>
      <li><strong>Retargeting Campaigns:</strong> Reach users who have previously engaged with your app or website, increasing conversion rates by connecting with them on TikTok, a frequently used platform.</li>
      <li><strong>Abandoned Cart Recovery:</strong> Remind users who abandoned their carts with personalized TikTok ads, encouraging them to complete their purchases.</li>
      <li><strong>Lapsed User Re-engagement:</strong> Reignite interest among users who have not interacted with your app or service recently, capturing their attention through TikTok ads.</li>
      <li><strong>Cross-platform Campaigns:</strong> Boost user engagement by combining TikTok with other channels like Push or Email to create cohesive multi-channel remarketing strategies.</li>
      <li><strong>Lookalike Audience Expansion:</strong> Identify converted user behaviors to create lookalike audiences, targeting potential new customers with similar characteristics.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/tiktok-remarketing" target="_blank">TikTok Remarketing</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="analytics" id="Smarter-Profile-Merging">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Smarter-Profile-Merging"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg" alt="Analytics" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Smarter Profile Merging for Cross-Device Insights</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge beta">BETA</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to introduce enhanced Anonymous-to-Identified Profile Merging. This update ensures that anonymous events from secondary devices are seamlessly merged into identified user profiles—giving you a complete view of customer behavior across devices.</p>
    <p>Key benefits of this enhancement:</p>
    <ul>
      <li><strong>Full Event Transfer:</strong> Anonymous events from new or secondary devices are merged into the user’s main profile upon login.</li>
      <li><strong>Segmentation & Funnels:</strong> Merged events are instantly available in segmentation, funnels, and campaigns for end-to-end visibility.</li>
      <li><strong>No Event Limits (Limited Time):</strong> No cap on how many anonymous events can be merged for a limited period.</li>
      <li><strong>Historical Accuracy:</strong> Pre-existing data remains unchanged to ensure consistency.</li>
    </ul>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

## April

<HTMLBlock>{`
<div class="release-note article" data-category="analytics" data-tag="Analytics" id="Bookmarks-in-New-Analytics">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Bookmarks-in-New-Analytics"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg" alt="Analytics" class="release-note-heading-icon" />
    </div>
    <div>
      <h3 class="release-note-heading">Bookmarks in New Analytics</h3>
    </div>
    <div class="badges">
      <div class="badge enhancement">ENHANCEMENT</div>
      <div class="badge private-beta">PRIVATE BETA</div>
    </div>
  </div>
  <div class="release-note-body">
    <p>We’re excited to introduce the Bookmarks feature across the all-new Analytics pages, including Trends, Funnels, and Flows. This feature lets you save your analysis views with all filters and settings applied, so you can return to them anytime without setting them up again. With editable bookmarks, you can easily refine your insights as your analysis goals evolve.</p>
    
    <p>For more information, refer to
      <a href="https://docs.clevertap.com/docs/flows-v2#bookmark-a-flow-analysis" target="_blank">Bookmarks in Flows</a>, 
      <a href="https://docs.clevertap.com/docs/funnels-v2#bookmark-a-funnel-analysis" target="_blank">Bookmarks in Funnels</a>, and
      <a href="https://docs.clevertap.com/docs/trends-v2#bookmark-a-trend-analysis" target="_blank">Bookmarks in Trends</a>
    </p>
  </div>
  <hr />
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Web-Visual-Editor-Personalization">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Web-Visual-Editor-Personalization"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Web Visual Editor: More Control, Better Personalization</h3>
    <div class="badges">
      <div class="badge enhancement">ENHANCEMENT</div>
      <div class="badge private-beta">PRIVATE BETA</div>
    </div>
  </div>

  <div class="release-note-body">
    <p>We have rolled out powerful enhancements to the Web Visual Editor, giving marketers greater control to personalize website elements without writing code. Key enhancements include:</p>
    <ul>
      <li><b>Mobile + Desktop Preview:</b> Optimize content for any device with responsive previews.</li>
      <li><b>Inline Editor Selection:</b> Choose how you want to edit page elements, right on the webpage.</li>
      <li><b>Insert & Clone Elements:</b> Easily add or clone sections for more dynamic layouts.</li>
      <li><b>Event & Profile Property Personalization:</b> Use event and profile properties to deliver hyper-personalized experience to users.</li>
      <li><b>Change Logs:</b> Track, undo, or delete changes with full visibility.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/advanced-personalization" target="_blank">Advanced Personalization.</a></p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="Web-Native-Display-Journeys">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Web-Native-Display-Journeys"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" />
    </div>
    <div><h3>Web Native Display in Journeys</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p><strong>Web Native Display</strong> is now integrated into Journeys, empowering marketers to deliver personalized omnichannel experiences. Until now, these campaigns ran standalone. With this release, you can re-engage users who drop off before key actions and achieve use cases such as Abandoned Checkouts or Purchase journey drop-offs, by using Web Native Display channel in journeys.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/journey-concepts#types-of-engagement-nodes" target="_blank">Types of Engagement Nodes</a>.</p>
  </div>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Reminders-Timely-Personalized-Nudges">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Reminders-Timely-Personalized-Nudges"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Reminders – Timely Actions with Personalized Nudges</h3>
    <div class="badges">
      <div class="badge new-feature">NEW FEATURE</div>
    </div>
  </div>

  <div class="release-note-body">
    <p>Introducing <b>Reminders</b>, a powerful feature that helps you boost engagement by sending timely, personalized messages that prompt users to take action before or after important dates. Whether it’s completing a task, meeting a deadline, or returning to the app, Reminders ensure users stay on track, improving productivity, time management, and campaign effectiveness.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/reminders" target="_blank">Reminders</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Dynamic-Personalization-for-Linked-Content">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Dynamic-Personalization-for-Linked-Content"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Dynamic Personalization for Linked Content</h3>
    <div class="badges">
      <div class="badge enhancement">ENHANCEMENT</div>
      <div class="badge private-beta">PRIVATE BETA</div>
    </div>
  </div>

  <div class="release-note-body">
    <p>We are excited to introduce Dynamic Personalization for Linked Content, which allows you to embed dynamic user data directly within your linked content responses. This removes the need for extra configuration or custom formatting, letting you deliver highly personalized content with minimal effort.</p>

    <ul>
      <li><b>Inline Personalization:</b> Personalization attributes are now supported directly in the linked content response, enabling customization at runtime.</li>
      <li><b>Localization:</b> Combine with external translation platforms to automatically serve content in the user’s preferred language without needing extra logic.</li>
    </ul>

    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/linked-content#using-personalization-in-linked-content-response" target="_blank">Using Personalization in Linked Content Response</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Email-Click-Heatmap">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Email-Click-Heatmap"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon"/>
    </div>
    <h3 class="release-note-heading">Email Click Heatmap</h3>
    <div class="badges">
      <div class="badge new-feature">NEW FEATURE</div>
      <div class="badge beta">BETA</div>
    </div>
  </div>
  <div class="release-note-body">
    <p>We are excited to introduce <b>Click Heatmap</b>, an advanced visual tool that maps user engagement onto your email layout, enabling you to see precisely which links and CTAs receive the most interaction within the actual design.</p>
    <p>This enhancement helps you instantly identify high-performing CTAs, understand link-level performance with unique and total clicks, and optimize content placement with color-coded insights.</p>
    <p>The heatmap supports multivariate and AMP/HTML campaigns, allowing you to compare engagement across versions using a simple dropdown.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/email-campaign-stats-heatmap#click-map" target="_blank">Click Heatmap</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Unique-Email-Engagement-Stats">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Unique-Email-Engagement-Stats"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns"/>
    </div>
    <h3 class="release-note-heading">Unique Email Engagement Stats</h3>
    <div class="badges">
      <div class="badge enhancement">ENHANCEMENT</div>
      <div class="badge beta">BETA</div>
    </div>
  </div>
  <div class="release-note-body">
    <p>We are excited to introduce <b>Unique Email Engagement Stats</b>. This enhancement allows you to switch from <i>Total</i> to <i>Unique</i> metrics in your email campaign stats, helping you track campaigns more precisely and accurately.</p>
    <p>By tracking unique metrics like opens or clicks, marketers can measure how many individual users engaged with an email, eliminating duplicates and providing a clearer view of audience engagement.</p>
    <p>With this enhancement, you can now track <b>Unique Sent, Delivered, Views, Clicks, and CTR</b>, enabling deeper insights and more personalized strategies.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/email-campaign-stats-uniquestats" target="_blank">Email Campaign Stats</a> and <a href="https://docs.clevertap.com/docs/campaign-reports" target="_blank">Campaign Reports</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="RCS-Business-Messaging-on-CleverTap">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#RCS-Business-Messaging-on-CleverTap"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns"/>
    </div>
    <h3 class="release-note-heading">RCS Business Messaging on CleverTap</h3>
    <div class="badges">
      <div class="badge enhancement">ENHANCEMENT</div>
      <div class="badge beta">BETA</div>
    </div>
  </div>
  <div class="release-note-body">
    <p>We are excited to launch <b>RCS Business Messaging</b> for customers in India. This feature enables brands to deliver rich, interactive, and two-way messaging experiences directly via the native messaging app on Android.</p>
    <p>
    <div style="text-align: center;">
  	<img src="https://files.readme.io/ba3510d2df54555813c3530132e9a966f43c6542351932a24034f60d90f87e81-RCS_Graphic.png" alt="RCS Business Messaging on CleverTap" />
  <p class="caption" style="margin-top: 8px;"><em>RCS Business Messaging</em></p>
</div>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/rcs" target="_blank">RCS</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="segments" id="Segment-Prioritization-Drag-Drop">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Segment-Prioritization-Drag-Drop"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/04fe24c1114cef41af4a4e0224cab88f5be4c31160eca491d67942c689cb79c0-Segmentation.svg" alt="Segments"/>
    </div>
    <h3 class="release-note-heading">Segment Prioritization Now Supports Drag-and-Drop</h3>
    <div class="badges">
      <div class="badge enhancement">ENHANCEMENT</div>
      <div class="badge beta">BETA</div>
    </div>
  </div>
  <div class="release-note-body">
    <p>You can now <b>drag and drop segments</b> to reorder user segments from the CleverTap dashboard and define their priority. This ensures that users always see the most relevant variable value when they qualify for multiple segments.</p>
    <p>For more details, refer to <a href="https://docs.clevertap.com/docs/remote-config" target="_blank">Remote Config</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="segments" id="NextGen-Segment-Builder">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#NextGen-Segment-Builder"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/04fe24c1114cef41af4a4e0224cab88f5be4c31160eca491d67942c689cb79c0-Segmentation.svg" alt="Segments"/>
    </div>
    <h3 class="release-note-heading">NextGen Segment Builder – Smarter, More Flexible Segmentation</h3>
    <div class="badges">
      <div class="badge enhancement">ENHANCEMENT</div>
      <div class="badge beta">BETA</div>
    </div>
  </div>
  <div class="release-note-body">
    <p>We are excited to launch the <b>NextGen Segment Builder</b>. This powerful update brings unmatched flexibility to segmentation, allowing marketers to craft highly personalized user segments with ease.</p>
    <p>With this enhancement, you can combine rules and groups of rules with <b>AND/OR</b> operators, customize logic across events, behaviors, and properties, use <b>User Buckets</b>, add <b>Multi-Triggers</b> to Live Segments, and easily <b>Clone</b> and <b>Bulk Delete</b> segments.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/segmentation" target="_blank">NextGen Segment Builder</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

## March

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="iOS-iPadOS-WebPush-Safari">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#iOS-iPadOS-WebPush-Safari"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" />
    </div>
    <h3 class="release-note-heading">Reach iOS and iPadOS Users with Web Push on Safari</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>Web Push is now fully supported on iOS and iPadOS Safari, powered by VAPID integration. You can now re-engage high-value Apple users with timely, personalized push notifications without needing an app.</p>
    <p>For more information, refer to <a href="https://developer.clevertap.com/docs/web-push#iosipados-web-push-configurations" target="_blank">iOS/iPadOS Web Push Configurations</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="WebPush-SoftPrompt-BellIcon">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#WebPush-SoftPrompt-BellIcon"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" />
    </div>
    <h3 class="release-note-heading">Web Push Soft Prompt Customization and New Bell Icon Prompt</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>Introducing two major enhancements to <b>Web Push Soft Prompts</b>. You can now customize the web soft prompt to match your brand’s tone and look. You can also add a <b>Bell Icon</b> to your website, giving users a persistent, convenient way to subscribe to web push notifications anytime.</p>
    <p>These updates offer greater flexibility and boost user opt-in rates for push notifications.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/setup-web-push#soft-prompt" target="_blank">Soft Prompt</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Event-Personalization-24H-Live-Campaigns">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Event-Personalization-24H-Live-Campaigns"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" />
    </div>
    <h3 class="release-note-heading">Event Personalization Beyond 24 Hours for Live Behavior Campaigns</h3>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>You can now apply Event Personalization to <i>Live Action</i> and <i>Date time</i> campaigns with a delay of more than 24 hours. You can create highly personalized push campaigns based on event properties to create custom-tailored notifications, driving better targeting and relevance.</p>
    <p>It also extends the reach of event-triggered communications hours to increase engagement rates and conversions.</p>
    <p>For example, streaming applications can now engage users with personalized messages, even days after their last session, ensuring continued engagement.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/create-message-push" target="_blank">Create Push Notification</a>.</p>
  </div>
  <hr/>
</div>
`}</HTMLBlock>

## February

<HTMLBlock>{`
<div class="release-note article" data-category="analytics" id="Flows-2.0">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Flows-2.0"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg" alt="Analytics" />
    </div>
    <div>
      <h3>Flows 2.0</h3>
    </div>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>

  <div class="release-note-body">
    <p>
      We are excited to introduce the new <b>Flows</b>. The enhanced Flows experience enables you to visualize all user paths from a selected event, making the analysis faster, more intuitive, and more comprehensive.
    </p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/233f86e9210bd94d1fb8f3eab939963e27f5cbc3462f3d56c35dc08b84a201b9-Flows_1.gif" alt="Flows 2.0 UI" />
  <p class="caption" style="margin-top: 8px;"><em>Flows 2.0</em></p>
</div>
    <p>
      For more information, refer to
      <a href="https://docs.clevertap.com/docs/flows-v2" target="_blank">Flows 2.0</a>.
    </p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Reminders-Timely-Actions">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Reminders-Timely-Actions"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" />
    </div>
    <div>
      <h3>Reminders – Timely Actions with Personalized Nudges</h3>
    </div>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>

  <div class="release-note-body">
    <p>Introducing <b>Reminders</b>, a powerful feature that helps you boost engagement by sending timely, personalized messages that prompt users to take action before or after important dates. Whether it’s completing a task, meeting a deadline, or returning to the app, Reminders ensure users stay on track, improving productivity, time management, and campaign effectiveness.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/reminders" target="_blank">Reminders</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="content-manager" id="Organize-Content-Manager">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Organize-Content-Manager"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg" alt="Content Manager" />
    </div>
    <div><h3>Organize Content with Content Manager</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p><strong>Content Manager</strong> is now available on the CleverTap dashboard. This powerful new feature enables you to efficiently manage and organize all your digital content, including media files, folders, and email templates, within a single, centralized location.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/content-manager" target="_blank">Content Manager</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Group-Campaign-Reports-Tags">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Group-Campaign-Reports-Tags"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" />
    </div>
    <div><h3>Group Campaign Reports by Tags for Deeper Insights</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap now provides Tag Group-wise campaign reports. This is available for Push, Web Push, Email, SMS, and WhatsApp campaigns sent via the <em>Target Users by Identity</em> API. With this enhancement, you can:</p>
    <ul>
      <li>Get granular insights with reports broken down by tag groups.</li>
      <li>Optimize campaign strategies by identifying high-performing tag groups.</li>
    </ul>
    <p>As a result, you can analyze and refine your messaging strategies effectively. For more information, see <a href="https://docs.clevertap.com/docs/campaign-reports#subscribe-to-reports" target="_blank">Subscribe to Reports</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Message-Archiving-Multi-Cloud">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Message-Archiving-Multi-Cloud"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Message Archiving with Multi-Cloud Support</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>The Message Archiving feature now fully supports <strong>Google Cloud Platform (GCP)</strong>, <strong>Azure Blob</strong>, and <strong>AWS S3 buckets</strong>. Customers can store copies of outgoing messages across various channels in real time. This allows seamless integration with multiple cloud storage platforms, offering flexibility and improved data management.</p>
    <ul>
      <li><strong>Google Cloud Platform (GCP) Bucket:</strong> Archive outgoing messages directly to your GCP bucket in real time.</li>
      <li><strong>Azure Blob:</strong> Effortlessly store message copies in Azure Blob storage.</li>
      <li><strong>AWS S3 Bucket:</strong> Store message archives reliably in your AWS S3 bucket.</li>
    </ul>
    <div style="text-align: center;">
  <img src="https://files.readme.io/e4b66d18ba25fdd9c90ef6497e34617a6c55a36340d8f5793cd037326bdaaf69-Message_Archiving_with_Multi-Cloud_Support_New_Feature.jpg" alt="Message Archiving with Multi-Cloud Support" />
  <p class="caption" style="margin-top: 8px;"><em>Message Archiving with Multi-Cloud Support</em></p>
</div>
    <p>This feature is available as a paid add-on. For more details, refer to <a href="https://docs.clevertap.com/docs/message-archiving" target="_blank">Message Archiving</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Email-Delivery-Tracking">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Email-Delivery-Tracking"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Email Delivery Tracking: Enhanced Campaign Insights</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>
      CleverTap now offers Email Delivery Tracking, providing deeper visibility into campaign performance beyond just sent emails.
      With this enhancement, you can now track actual deliveries to users' inboxes, measure delivery rates, analyze engagement based on delivered emails,
      and gain insights into errors affecting end user delivery. This feature is currently in Private Beta for customers using SendGrid and Infobip (Advanced Email) providers.
    </p>
    <p>For more details, refer to <a href="https://docs.clevertap.com/docs/email-campaign-stats-delivered" target="_blank">Campaign Stats</a> and <a href="https://docs.clevertap.com/docs/email-provider-operations-delivered#view-provider-stats" target="_blank">Provider Stats</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Emoji-Support-Web-Push">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Emoji-Support-Web-Push"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Emoji Support for Web Push Notification</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>
      You can now personalize your notifications and make them fun by adding emojis in the improved Web Push Editor.
      All message customization options, such as Scribe, Personalization, and Emojis, are accessible below the text fields,
      making it easier to create engaging notifications.
    </p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/d6d84e856b1b3fbbb667311ee22af4a6f8cea0fef43525fed5f35a416cee59da-image.png" alt="Emoji-enabled Web Push UI" />
  <p class="caption" style="margin-top: 8px;"><em>Emoji Support for Web Push Notification</em></p>
</div>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/create-message-web-push#web-push-editor" target="_blank">Web Push Editor</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Scribe-Web-Push">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Scribe-Web-Push"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Scribe for Web Push: Emotionally Intelligent Campaigns Made Easy</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>
      Scribe for CleverTap Web Push is here to transform your campaign messaging.
      With Scribe, you can easily and quickly create emotionally resonant web push messages.
      You can also analyze and refine their tone to better connect with your audience and test multiple variations to maximize campaign effectiveness.
      This feature is now available to all customers with access to Scribe as part of their Billing Plan.
    </p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/scribe#create-a-web-push-notification-using-scribe" target="_blank">Scribe</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="Unsaved-Changes-Journey-Canvas">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Unsaved-Changes-Journey-Canvas"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" /></div>
    <div><h3>Prevent Accidental Data Loss with Unsaved Changes Prompt on Journey Canvas</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>
      We have introduced an <strong>"Unsaved Changes"</strong> prompt to help prevent accidental loss of work on the Journey canvas.
      This feature ensures that users are alerted before navigating away without saving changes. Also, it reduces the risk of unintentional data loss.
    </p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/23aaaad32d048a865e65b4bb6c55e2da4f44f37421f3bc26b26c23123142e809-Unsaved_Changes_Prompt-20250206-131047.gif" alt="Save Changes" />
  <p class="caption" style="margin-top: 8px;"><em>Save Changes</em></p>
</div>
    <p>For more details, refer to <a href="https://docs.clevertap.com/docs/journey-states#draft-state" target="_blank">Draft State</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="Journey-List-Columns">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Journey-List-Columns"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" /></div>
    <div><h3>Addition of New Columns on the Journey List Page</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>We have added new columns to the Journey List page: <em>Created By</em>, <em>Created On</em>, <em>Published By</em>, and <em>Published On</em>. These additions provide users with more comprehensive information at a glance.</p>
    <p>This simplifies tracking and auditing of journeys, allowing for better collaboration and visibility across teams and various roles using the CleverTap dashboard for publishing Journeys.</p>
    <p>For more details, refer to <a href="https://docs.clevertap.com/docs/journeys-list" target="_blank">Journey List</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="Journey-Description">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Journey-Description"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" /></div>
    <div><h3>Adding Descriptions for Journey</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to announce that you can now add a description or summary while publishing a journey. This new feature allows you to provide additional context and insights to your internal users.</p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/ca82e80342401ea4b991fee118fd63bb122ce9f4e03e485833d9520568599b71-Add_Journey_Description-20250206-155958.gif" alt="Add Journey Description" />
  <p class="caption" style="margin-top: 8px;"><em>Add Journey Description</em></p>
</div>
    <p>You can update this description only when editing the published journey.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/add-a-journey-description#publish-journeys" target="_blank">Publish Journeys</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

## January

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Email-Add-on-Essentials">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Email-Add-on-Essentials"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Email Add-on for CleverTap Essentials Plan</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div class="release-note-body">
    <p>The Email Add-on is now available with the CleverTap Essentials Plan. With this add-on, you can use CleverTap as your Email Service Provider (ESP), eliminating the need for third-party integrations.</p>
    <p>To enable the Email add-on from the CleverTap dashboard, purchase the add-on, set up your email preferences, and warm up your dedicated IP to ensure the best possible deliverability.</p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/fdf055c4de60720e01da16e73a883ac275845e8884b53a8f46ac757370e3da03-image.png" alt="Email Add-on for CleverTap Essentials Plan" />
  <p class="caption" style="margin-top: 8px;"><em>Email Add-on for CleverTap Essentials Plan</em></p>
</div>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/email-add-on-for-clevertap-essentials-plan" target="_blank">Email Add-on</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="DND-in-Journeys">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#DND-in-Journeys"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" /></div>
    <div><h3>DND in Journeys</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>The updated DND feature sends notifications delayed by DND at their original scheduled time instead of right after the DND period ends. For example, a message was scheduled for 10 AM but was postponed due to a DND setup between Friday at 9 PM and Monday at 9 AM. The message will now be sent on Tuesday at 10 AM and not immediately after DND ends at 9 AM on Monday. This ensures a more controlled and user-friendly notification delivery experience.</p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/6484ade9dd9a326b59d5028ee3e318bccc100934a463a0294fd65492907ba7ea-DND_in_Journeys.png" alt="DND in Journeys" />
  <p class="caption" style="margin-top: 8px;"><em>DND in Journeys</em></p>
</div>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/setup-journey#dnd-and-timezone" target="_blank">DND and Timezone</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="Journey-Throttling">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Journey-Throttling"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" /></div>
    <div><h3>Introducing Throttling in Journeys</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>You can now set throttling limits from the Journey Setup. This allows smoother regulation of message delivery rates during large-scale engagements.</p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/a952feef88184d47da95cbeb1d8d8b7aef29b46eb2886a34a49c59bfba54c0a6-Set_Up_Throttle_Limits_from_Journeys.gif" alt="Set Up Throttle Limits from Journeys" />
  <p class="caption" style="margin-top: 8px;"><em>Set Up Throttle Limits from Journeys</em></p>
</div>
    <p>With this enhancement, you can:</p>
    <ul>
      <li>Control message delivery rates directly within the Journey, ensuring more efficient communication.</li>
      <li>Prevent system overload and maintain optimal app and web performance, even during high-volume campaigns.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/messaging-frequency-caps#throttle" target="_blank">Throttling in Journeys</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Automated-Shopify-Catalog-Sync">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Automated-Shopify-Catalog-Sync"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Automated Shopify Catalog Sync for Enhanced Personalization</h3></div>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>Introducing the Catalog Sync feature that simplifies product data management. The Catalog Sync toggle automates the synchronization of product data between your users’ Shopify and CleverTap accounts. This ensures daily catalog updates while also eliminating manual effort and errors.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/shopify#catalog-sync" target="_blank">Catalog Sync</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="product-experiences" id="Create-Variables-Dashboard">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Create-Variables-Dashboard"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/d7de531a1060998537a4e71a078198cf28076d99e1aed3e3c1bdcb5509e29d95-Product_experiences.svg" alt="Product Experiences" /></div>
    <div><h3>Create Variables from the Dashboard</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>You can now create variables to use in Product Experiences directly from the Dashboard, removing the need to sync them from the code. This allows you to integrate Product Experiences and build a proof of concept quickly. You can then share these variables with the developers to add the backend code later. It is a game-changer that saves you time and accelerates your workflow!</p>
    <p><strong>Note:</strong> Creating File type variables is currently not supported from the dashboard.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/remote-config#create-variables-from-the-dashboard" target="_blank">Create Variables from Dashboard</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="product-experiences" id="User-Property-Personalization">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#User-Property-Personalization"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/d7de531a1060998537a4e71a078198cf28076d99e1aed3e3c1bdcb5509e29d95-Product_experiences.svg" alt="Product Experiences" /></div>
    <div><h3>Personalize User Properties in Product Experiences</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>All customers using Product Experiences can now personalize their variable values using User Properties. For example, the text content on a product carousel can be personalized based on the user's profile data, such as their name and membership validity.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/remote-config#user-profile-personalization" target="_blank">User Profile Personalization</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

# 2024

## December

<HTMLBlock>{`
<div class="release-note article" data-category="content-manager" id="Reusable-Content-Blocks">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Reusable-Content-Blocks"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg" alt="Content Manager" /></div>
    <div><h3>Introducing Reusable Content Blocks for Greater Efficiency</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to introduce Content Blocks in CleverTap’s Content Manager. Content Blocks are reusable snippets for standardized elements, such as footers, logos, or disclaimers.</p>
  <div style="text-align: center;">
  <img src="https://files.readme.io/686373549b6ac569fd3abb3ab7bafddabdd0b37236d60ce08b551e2a559309e1-image.png" alt="Footer Standardization with Content Blocks" />
  <p class="caption" style="margin-top: 8px;"><em>Footer Standardization with Content Blocks</em></p>
</div>
    <p>These blocks are designed to simplify the reuse of content across email campaigns, saving you valuable time. They help you maintain consistent messaging and standardize your brand communication.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/content-blocks" target="_blank">Content Blocks</a> and <a href="https://developer.clevertap.com/docs/content-blocks-api" target="_blank">Content Block APIs</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Store-Messages-Archiving">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Store-Messages-Archiving"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Store Outgoing Messages Using Message Archiving</h3></div>
    <div class="badge beta">BETA</div>
  </div>
  <div class="release-note-body">
    <p>Message Archiving now supports Google Cloud Platform (GCP), allowing customers to store copies of outgoing messages across different channels in real-time directly in their GCP bucket. The feature is in Public Beta and available to all CleverTap customers using AWS S3 buckets, Azure Blob, and GCP buckets.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/message-archiving" target="_blank">Message Archiving</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Customizable-URL-Schema-SMS">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Customizable-URL-Schema-SMS"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Introducing Customizable URL Schema for SMS Campaigns</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to introduce a new enhancement that allows you to shorten and customize the links in your SMS messages. This means you can create links that match your brand, comply with TRAI regulations, and ensure smooth delivery to customers, all while improving campaign performance.</p>
    <p>With this enhancement, you can include sender IDs in SMS URLs for seamless DLT whitelisting and create personalized URL structures that align with your branding. This ensures uninterrupted delivery and enhances customer engagement.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/sms-regulations#url-whitelisting-for-sms-marketing-campaigns" target="_blank">URL Whitelisting for SMS Marketing Campaigns</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Enhanced-Delivery-Triggers-Web-Popups">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Enhanced-Delivery-Triggers-Web-Popups"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Enhanced Delivery Triggers for Web Pop-ups</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to unveil our new and improved web pop-up triggers that enable timely and relevant messaging. The new triggers are based on various user interactions, such as scrolling behavior, inactivity, encountering a timed delay, or attempting to exit the webpage on a desktop.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/create-message-web-popup#triggers-for-campaign-delivery" target="_blank">Triggers for Campaign Delivery</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="Analyze-Notifications-Journey-Labels">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Analyze-Notifications-Journey-Labels"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" /></div>
    <div><h3>Analyze Notifications Sent Using Journeys Labels</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>You can now use Journey labels in the <em>Analytics</em> section to analyze the <em>Notifications Sent</em> event. You can now easily track and derive insights from notifications sent through Journeys tagged with specific labels.</p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/7f26df255f646c42fcdfbb0a6760afa7be9495d671c751f7d2d28431e2000008-Analyze_Journey_Performance_Using_Journey_Label.png" alt="Analyze Journey Performance Using Journey Labels" />
  <p class="caption" style="margin-top: 8px;"><em>Analyze Journey Performance Using Journey Labels</em></p>
</div>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/journeys-list#assign-label-to-journeys" target="_blank">Assign Label to Journeys</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="journeys" id="Enhanced-Entry-Timelines-Journey-Setup">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Enhanced-Entry-Timelines-Journey-Setup"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg" alt="Journeys" /></div>
    <div><h3>Enhanced Entry Timelines in Journey Setup</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap has redesigned <em>Journey Entry Timelines</em> to remove redundancies and improve usability. Also, the error handling has been improved to manage scenarios such as incorrect date or day of recurrence inputs.</p>
    <p>These enhancements ensure a smoother, more intuitive Journey setup process for all CleverTap users.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/setup-journey#define-the-journey-entry-timelines" target="_blank">Define Journey Entry Timelines</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Custom-Headers-Message-Extras">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Custom-Headers-Message-Extras"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Custom Headers and Message Extras for Enhanced Email Analytics</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now enhance your email tracking and analytics capabilities with Custom Headers and Message Extras. This feature enables you to add key-value pairs to email headers and bodies, offering seamless integration with third-party tools and internal systems. It is available for users with Sendgrid, Amazon SES, Generic SMTP, and Infobip (Advanced Email Add-on).</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/create-message-email-custom-kv#custom-headers" target="_blank">Custom Headers</a> and <a href="https://docs.clevertap.com/docs/create-message-email-custom-kv#custom-extras" target="_blank">Message Extras</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

## November

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="AppsFlyer-OneLink-Email">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#AppsFlyer-OneLink-Email"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>AppsFlyer OneLink Integration for Email</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>Introducing the updated AppsFlyer OneLink integration for Email. This new version makes it easier for users to set up and track clicks by managing everything from the AppsFlyer dashboard. You no longer need to configure anything on the CleverTap dashboard. The setup is now fully managed from the AppsFlyer dashboard itself, removing the need for configuration on CleverTap.</p>
    <p>The older integration is no longer available, so you must switch to the new setup to keep using it. Currently, this integration supports Sendgrid ESP only. To enable it, contact <a href="https://www.appsflyer.com/company/contact/" target="_blank">AppsFlyer support</a>.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/appsflyer-onelink#set-up-appsflyer-onelinks" target="_blank">AppsFlyer OneLink Integration</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Campaign-ID-Personalization-Email">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Campaign-ID-Personalization-Email"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Campaign ID Personalization for Email</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>Campaign ID Personalization is now available in both the <em>Email HTML (Rich Media) Editor</em> and <em>Drag & Drop Editor</em>, giving you more flexibility when personalizing email campaigns. You can create unique links and track engagements more accurately.</p>
    <ul>
      <li>Personalize URLs with campaign IDs for better attribution and tracking.</li>
      <li>Integrate easily with external tools to analyze engagement and meet custom analytics needs.</li>
      <li>Automate workflows using campaign IDs as payloads for custom key-value pairs.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/personalize-message-email#campaign-id-personalization" target="_blank">Campaign ID Personalization</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Event-Personalization-Email-24hrs">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Event-Personalization-Email-24hrs"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Event Personalization Beyond 24 Hours for Email</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now apply Event Personalization to <em>Live Action</em> and <em>Date Time</em> campaigns with a delay of more than 24 hours. Create highly personalized Email campaigns based on event properties broadening the window for event-triggered communications to create custom-tailored notifications, driving better targeting and relevance.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/personalize-message-email" target="_blank">Personalize Message</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="OAuth-2.0-Webhook-Campaigns">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#OAuth-2.0-Webhook-Campaigns"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>OAuth 2.0 for Webhook Campaigns</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to offer a more secure and streamlined way to connect to your webhook endpoints. By adopting OAuth 2.0 authentication, we align with industry-standard security protocols to safeguard your interactions with external APIs while improving efficiency and ease of use.</p>
    <p>Enhance your Webhook security and efficiency with:</p>
    <ul>
      <li><strong>OAuth 2.0 Authentication:</strong> Robust security for webhook connections.</li>
      <li><strong>Flexible Grant Types:</strong> Support for <em>Password Credentials</em> and <em>Client Credentials</em>.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/setup-webhooks#oauth-20" target="_blank">OAuth 2.0</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Amazon-SES-Email-HTTP">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Amazon-SES-Email-HTTP"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Amazon SES Email Delivery via HTTP Protocol</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>CleverTap’s email delivery system now supports the HTTP protocol with Amazon Simple Email Service (SES), enabling faster and more efficient email delivery compared to the traditional SMTP protocol.</p>
    <p>Existing Amazon SES integrations that are using SMTP can now switch to HTTP by updating the provider setup with the required additional details.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/amazon-simple-email-service" target="_blank">Amazon Simple Email Service (SES)</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Azure-Blob-Support-Archiving">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Azure-Blob-Support-Archiving"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Support for Azure Blob in Message Archiving</h3></div>
    <div class="badge beta">BETA</div>
  </div>
  <div class="release-note-body">
    <p>Message Archiving now supports Azure Blob. It allows customers to store copies of outgoing messages across different channels in real-time. The feature is in Public Beta and available to all CleverTap customers using AWS S3 buckets and Azure Blob.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/message-archiving" target="_blank">Message Archiving</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

## October

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="WhatsApp-Carousel-Gupshup">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#WhatsApp-Carousel-Gupshup"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>WhatsApp Carousel Templates Now Available for Gupshup</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>We are excited to announce that carousel templates are now available for CleverTap using Gupshup with CleverTap. You can now create interactive WhatsApp campaigns with up to 10 dynamic carousel cards, allowing recipients to scroll through engaging content.</p>
    <p>With Carousel Templates on CleverTap Gupshup, you can now:</p>
    <ul>
      <li><strong>Message Bubble:</strong> Offers up to 1024 characters for detailed context.</li>
      <li><strong>Carousel Cards:</strong> Each card includes:
        <ul>
          <li><strong>Card Header:</strong> Add a media type which can be either Image or Video.</li>
          <li><strong>Card Body:</strong> Add up to 160 characters for concise messaging.</li>
          <li><strong>Card Buttons:</strong> Add up to two action buttons per card.</li>
        </ul>
      </li>
    </ul>
    <p><strong>Use Cases:</strong></p>
    <ul>
      <li><strong>E-commerce:</strong> Showcase products or promote flash sales to drive purchases.</li>
      <li><strong>Fintech:</strong> Highlight investment options or provide financial education.</li>
      <li><strong>Food Delivery:</strong> Display menu highlights or specialty dishes to entice users.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/gupshup" target="_blank">Gupshup</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Live-Behavior-Event-Personalization">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Live-Behavior-Event-Personalization"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Introducing Event Personalization Beyond 24 Hours for Live Behavior Campaigns</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now apply Event Personalization to Live Action and Date time campaigns with a delay of more than 24 hours. You can create highly personalized push campaigns based on event properties to create custom-tailored notifications, driving better targeting and relevance. It also extends the reach of event-triggered communications hours to increase engagement rates and conversions.</p>
    <p>For example, streaming applications can now engage users with personalized messages, even days after their last session, ensuring continued engagement.</p>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/create-message-advanced-personalization#push-editor" target="_blank">Create Push Notification</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="analytics" id="Compare-Trends-Across-Time">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Compare-Trends-Across-Time"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg" alt="Analytics" /></div>
    <div><h3>Compare Trends Across Time</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>You can now compare an event across different time periods. For example, a user can display the count of users for the <em>Charged</em> event for Week 1 and Week 2 in the same chart. The trend line for Week 2 will be displayed as a dotted line so that it is easy to distinguish it from the Week 1 trend line. It helps create a visual comparison to quickly spot trends and differences across time frames.</p>
    <div style="text-align: center;">
  <img src="https://files.readme.io/a105d0d551ff34f815b22214179e27afbc372155fd0719d07a83baf0bca32217-trends_compare.gif" alt="Compare Trends Between Different Time Periods" />
  <p class="caption" style="margin-top: 8px;"><em>Compare Trends Between Different Time Periods</em></p>
</div>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/trends-v2#compare-trends-between-time-periods" target="_blank">Compare Trends Between Time Periods</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Notification-Failed-Event">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Notification-Failed-Event"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Notification Failed Event for Email Analytics</h3></div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>
  <div class="release-note-body">
    <p>Announcing a significant enhancement to our Email Analytics: the <strong>Notification Failed</strong> event that gives you more deeper insights into campaign errors. With this update, CleverTap captures a <em>Notification Failed</em> event, along with the reason for failure, enabling better targeting and resolution.</p>
    <ul>
      <li><strong>Improved Targeting:</strong> Target users through alternate channels when errors occur. For example, if users encounter soft bounce errors, you can re-target them via other channels.</li>
      <li><strong>Cleaner Email List:</strong> Unsubscribe users with persistent errors to maintain an accurate and engaged subscriber base.</li>
      <li><strong>Error Analysis:</strong> Analyze the root causes of errors to resolve issues and optimize future engagements.</li>
    </ul>
    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/events#:~:text=Notification%20Failed,in%20the%20campaign" target="_blank">Notification Failed Event</a>.</p>
  </div>
  <hr>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<div class="release-note article" data-category="campaigns" id="Subscription-Group-Insights-Email">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#Subscription-Group-Insights-Email"><i class="fa-light fa-anchor"></i></a>
    </div>
    <div><img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" /></div>
    <div><h3>Subscription Group Insights in Email Campaign Analytics</h3></div>
    <div class="badge enhancement">ENHANCEMENT</div>
  </div>
  <div class="release-note-body">
    <p>The new Subscription Group Insights in Email Campaign Analytics will allow you to have a more granular view of unsubscribes by subscription group providing detailed insights, including:</p>
    <ul>
      <li><strong>Group-Level Unsubscribes and Resubscribes:</strong> Track the number of unsubscribes and resubscribes for each targeted subscription group from your campaign stats.</li>
      <li><strong>Comprehensive Subscription View:</strong> View the activities of the targeted subscription groups. Additionally, you can track any changes made through the Email Preference Center for other subscription groups.</li>
      <li><strong>Enhanced Analytics:</strong> Understand user behavior better by analyzing how different subscription groups engage with your campaigns.</li>
    </ul>
    <p>For more information, refer to the documentation links below:</p>
    <ul>
      <li><a href="https://docs.clevertap.com/docs/email-campaign-stats-cc-bcc-group-unsubscribe" target="_blank">Campaign Stats (for customers with cc/bcc Beta)</a></li>
      <li><a href="https://docs.clevertap.com/docs/email-stats" target="_blank">Campaign Stats (all other customers)</a></li>
    </ul>
  </div>
</div>
`}</HTMLBlock>

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
  
/* .rm-Guides a.suggestEdits {
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
`}