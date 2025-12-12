---
title: Release Notes Filter Testing
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

<div className="filters">
  <h1>Filter By Feature</h1>

  <div className="filter-box">
    <div className="filter-options">
      <label className="filter-option">
        <input type="checkbox" id="filter-security-project-settings" />
        <span className="security-project-settings">
          <img
            src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg"
            alt="Settings"
          />
          Security &amp; Project Settings
        </span>
      </label>

      <label className="filter-option">
        <input type="checkbox" id="filter-data-and-integrations" />
        <span className="data-and-integrations">
          <img
            src="https://files.readme.io/bf86621cc6be2995b3a9323ccfcaae0e172d6da76b2bfedc7983c5be75eb179d-Partners_Icon_Outlined.svg"
            alt="Data & Integrations"
          />
          Data &amp; Integrations
        </span>
      </label>

      {/* ...repeat same className changes for the rest... */}
    </div>
  </div>
</div>

# 2025

## December

<div class="release-note article" data-category="security-project-settings" id="pii-tokenization">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#pii-tokenization">
        <i class="fa-light fa-anchor" />
      </a>
    </div>

    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon" />
    </div>

    <h3 class="release-note-heading">PII Tokenization</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>

  <div class="release-note-body">
    <p>You can now protect sensitive user data by ensuring that Personally Identifiable Information (PII) never enters CleverTap's environment. Instead of sending identifiers such as email addresses or phone numbers, you send tokens that map securely to your own vault. CleverTap then processes only tokens for Segments, Engagements, and Analytics, keeping all personal data fully within your control.</p>
    <p>With PII Tokenization, you can:</p>

    <ul>
      <li><strong>Protect Sensitive Data:</strong> Replace PII with tokens to comply with data privacy and residency regulations.</li>
      <li><strong>Choose Your Vault Model:</strong> Use CleverTap Vault or bring your own for flexibility.</li>
      <li><strong>Simplify Integration:</strong> Generate and manage tokens using the Vault API for seamless client-side setup.</li>
      <li><strong>Control Dispatch Models:</strong> Run the Dispatcher On-Prem (no PII leaves your environment) or Off-Prem (secure, token-only resolution at send time).</li>
    </ul>

    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/pii-tokenization" target="_blank">PII Tokenization</a>.</p>
  </div>

  <hr />
</div>

## November

<div class="release-note article" data-category="security-project-settings" id="automated-audit-log-exports-for-siem">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#automated-audit-log-exports-for-siem">
        <i class="fa-light fa-anchor" />
      </a>
    </div>

    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon" />
    </div>

    <h3 class="release-note-heading">Automated Audit Log Exports for SIEM</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>

  <div class="release-note-body">
    <p>You can now securely export audit logs from CleverTap to your own cloud storage providers, including AWS S3, Google Cloud Storage, or Microsoft Azure Blob Storage. This self-serve feature allows you to easily manage, store, and retain audit data within your own cloud environment.</p>
    <p>With SIEM Export, you can:</p>

    <ul>
      <li><strong>Automate Secure Delivery:</strong> Receive exports every 4 hours in JSON (UTF-8) format.</li>
      <li><strong>Ensure Continuous Visibility:</strong> Monitor all account activities in real time to strengthen compliance and security posture.</li>
      <li><strong>Maintain Full Data Control:</strong> Store audit logs directly within your organization's cloud to manage retention and governance.</li>
      <li><strong>Integrate Seamlessly with SIEM Tools:</strong> Combine CleverTap's audit data with broader operational insights across your systems.</li>
    </ul>

    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/automated-audit-log-exports-for-siem" target="_blank">Automated Audit Log Exports for SIEM</a>.</p>
  </div>

  <hr />
</div>

<div class="release-note article" data-category="campaigns" id="whatsapp-flows-for-whatsapp-direct">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#whatsapp-flows-for-whatsapp-direct">
        <i class="fa-light fa-anchor" />
      </a>
    </div>

    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon" />
    </div>

    <h3 class="release-note-heading">WhatsApp Flows for WhatsApp Direct</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>

  <div class="release-note-body">
    <p>Introducing WhatsApp Flows, a form-based experience that lets your users complete tasks such as booking a ticket or placing an order without leaving WhatsApp. CleverTap handles orchestration, analytics, and automation. Flows are created at the WhatsApp Business Account level and appear as a call-to-action button in your message. Tapping the button opens a guided, structured journey that follows Meta's Flows specification.</p>
    <p>With WhatsApp Flows, you can:</p>

    <ul>
      <li><strong>Choose Your Setup</strong>: Use static flows, a CleverTap endpoint with customer relay, or your own endpoint for full control.</li>
      <li><strong>Protect Data End to End</strong>: Keep payloads encrypted on the device and decrypt or re-encrypt according to the selected setup.</li>
      <li><strong>Capture Outcomes in CleverTap</strong>: Record Flow events for reporting and update profile attributes for personalization and segmentation.</li>
      <li><strong>Use Templates Seamlessly</strong>: Attach a Flow to a WhatsApp template, personalize message content, and publish in campaigns.</li>
    </ul>

    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/whatsapp-flows" target="_blank">WhatsApp Flows.</a></p>
  </div>

  <hr />
</div>

<div class="release-note article" data-category="campaigns" id="preferred-channel-for-engagement">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#preferred-channel-for-engagement">
        <i class="fa-light fa-anchor" />
      </a>
    </div>

    <div>
      <img src="https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg" alt="Campaigns" class="release-note-heading-icon" />
    </div>

    <h3 class="release-note-heading">Preferred Channel for Engagement</h3>
    <div class="badge new-feature">NEW FEATURE</div>
    <div class="badge private-beta">PRIVATE BETA</div>
  </div>

  <div class="release-note-body">
    <p>You can now deliver messages through the channel each user is most likely to engage with. Powered by Clever.AI, Preferred Channel analyzes engagement data across Push, Email, SMS, and WhatsApp over the past 90 days to predict and select the best-performing communication channel for every user.</p>
    <p>With Preferred Channel, you can:</p>

    <ul>
      <li><strong>Leverage AI-Powered Channel Prediction</strong>: Identify the most effective communication channel for each user based on engagement history.</li>
      <li><strong>Integrate Seamlessly Across CleverTap</strong>: Use the new Preferred Channel user property in Segmentation, Campaigns, Journeys, and Analytics.</li>
      <li><strong>Boost Conversions and Reduce Noise</strong>: Focus on the channels that drive real engagement and results.</li>
      <li><strong>Automate Channel Selection</strong>: Let Clever.AI optimize delivery so you can focus on content and strategy.</li>
    </ul>

    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/preferred-channel" target="_blank">Preferred Channel</a>.</p>
  </div>

  <hr />
</div>

<div class="release-note article" data-category="security-project-settings" id="field-level-at-rest-encryption-for-user-and-event-properties">
  <div class="release-note-header">
    <div class="anchor-link-icon">
      <a href="#field-level-at-rest-encryption-for-user-and-event-properties">
        <i class="fa-light fa-anchor" />
      </a>
    </div>

    <div>
      <img src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg" alt="Settings" class="release-note-heading-icon" />
    </div>

    <h3 class="release-note-heading">Field-Level at Rest Encryption for User and Event Properties</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>

  <div class="release-note-body">
    <p>CleverTap now supports Field-Level at Rest Encryption, enabling you to encrypt user and event properties for stronger data protection. This capability extends beyond the existing volume-level encryption, providing granular control over how sensitive data, including system and user properties, is secured within the platform.</p>
    <p>With this capability, you can:</p>

    <ul>
      <li><strong>Protect Sensitive Fields:</strong> Selectively encrypt both user and event properties while keeping the rest of your data accessible for Analytics.</li>
      <li><strong>Choose Your Key Strategy:</strong> Use CleverTap-managed keys or Bring Your Own Keys (BYOK) encryption through AWS KMS.</li>
      <li><strong>Enable Encryption Easily:</strong> Apply encryption to the properties directly from the Schema page.</li>
      <li><strong>Maintain Platform Compatibility:</strong> Ensure that encrypted fields continue to work seamlessly across Segments, Campaigns, and Analytics for authorized users.</li>
    </ul>

    <p>For more information, refer to <a href="https://docs.clevertap.com/docs/field-level-at-rest-encryption" target="_blank">Field-Level at Rest Encryption</a>.</p>
  </div>

  <hr />
</div>

For the full release notes with styling and filtering functionality, view this page in the CleverTap documentation portal.
