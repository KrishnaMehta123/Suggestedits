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

<HTMLBlock>{`
<div className="release-note article" data-category="security-project-settings" id="pii-tokenization">
  <div className="release-note-header">
    <img
      src="https://files.readme.io/01053ed2e833c5e6bb242a86b84f304b7499ff0b0a26f422c3cc846d70530658-Settings.svg"
      alt=""
      className="release-note-heading-icon"
    />
    <h3 className="release-note-heading">PII Tokenization</h3>
    <div class="badge new-feature">NEW FEATURE</div>
  </div>
  <div className="release-note-body">
    <p>
      You can now protect sensitive user data by ensuring that Personally Identifiable Information (PII) never enters CleverTap’s environment.
      Instead of sending identifiers such as email addresses or phone numbers, you send tokens that map securely to your own vault.
      CleverTap then processes only tokens for Segments, Engagements, and Analytics, keeping all personal data fully within your control.
    </p>

    <p>With PII Tokenization, you can:</p>

    <ul>
      <li><strong>Protect Sensitive Data:</strong> Replace PII with tokens to comply with data privacy and residency regulations.</li>
      <li><strong>Choose Your Vault Model:</strong> Use CleverTap Vault or bring your own for flexibility.</li>
      <li><strong>Simplify Integration:</strong> Generate and manage tokens using the Vault API for seamless client-side setup.</li>
      <li><strong>Control Dispatch Models:</strong> Run the Dispatcher On-Prem (no PII leaves your environment) or Off-Prem (secure, token-only resolution at send time).</li>
    </ul>

    <p>
      For more information, refer to <a href="https://docs.clevertap.com/docs/pii-tokenization" target="_blank" rel="noopener noreferrer">PII Tokenization
      </a>.
    </p>
  </div>
  <hr />
</div>
`}</HTMLBlock>

<br />
