---
title: Device Previews for A/B Tests
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Before you publish your A/B tests to your entire audience, you can now **preview and test multiple experiments simultaneously** on specific devices or profiles. This ensures that your variants render correctly and behave as expected across devices before the test goes live.

## Overview

CleverTap’s **Preview and Test Mode** allows you to perform the following actions:

* Mark specific devices as _test devices_ for controlled QA.
* Assign specific variants to specific devices or user profiles.
* Run multiple A/B tests at the same time in _Test Mode_.
* View and manage all active test sessions directly from the dashboard.

These capabilities help QA and product teams verify complex, multi-device setups, ensuring a consistent user experience before launch.

## Prerequisites

Before you begin:

* You must have **A/B Test creation** permissions.
* Check that the devices you want to test are **registered test devices** in your user profiles.
* Your app is running the **latest SDK version** that supports the A/B Test Enhancements. (@murtaza, please provide the SDK version)

***

## Mark a Device as a Test Device

1. Navigate to **Users > Find People**.
2. Search for the **user profile** you want to test with (by Identity or CleverTap ID).
3. Under **Devices**, click **Mark as Test Device** next to the required device.
4. The button changes to **Unmark as Test Device** when active.

<br />

<Callout icon="📘" theme="info">
  Note

  You can mark multiple devices under the same profile for testing.
  Only marked devices appear in the _Test Devices_ segment selector in the A/B Test dashboard
</Callout>

<Image alt="Placeholder: Screenshot showing “Mark as Test Device” button on user profile" border={false} src="#" />

## Step 2: Assign Variants to Specific Devices

Once you’ve marked test devices, you can assign them to particular test variants.

1. Open your A/B test from **Product Experiences > A/B Tests**.
2. Go to the **Variables** tab and click the **+ Add Segment** icon.
3. From the dropdown, select:

   * **Test Devices → Registered Test Devices**
4. Choose the profile(s) and test device(s) you want to associate with a specific variant.
5. Click **Save**.

This allows you to test multiple variants on multiple devices for the same profile — for example:

* Variant A on the home screen on _iPhone 17_
* Variant B on the settings screen on _Pixel 10_

<Image alt="Placeholder: Screenshot showing test device selection for variant assignment" border={false} src="#" />

***

## Step 3: Enable Preview and Test Mode

After assigning devices and variants:

1. From the A/B test list, click **Preview and Test** for the test you want to validate.
2. The status column updates to **Test Mode**.
3. Use your marked test devices to preview the variants in your app.

> **Tip:**
> You can enable test mode for **multiple A/B tests** at once — perfect for teams testing multiple experiences in parallel.

<Image alt="Placeholder: Screenshot showing “Preview and Test” toggle and Test Mode status" border={false} src="#" />

***

## Step 4: View and Manage Running Tests

To view all currently running test sessions:

1. Click **View Running Tests** in the A/B Test dashboard.
2. The modal displays:

   * All profiles and devices currently in test mode
   * The A/B tests they’re assigned to
3. You can:

   * **Update Test:** Add or remove devices
   * **Stop Test:** End the test session

> **Note:**
> Stopping a test session removes the device from test mode but does not delete the A/B test configuration.

<Image alt="Placeholder: Screenshot showing View Running Tests modal" border={false} src="#" />

***

## Troubleshooting

| Issue                                   | Possible Cause                            | Solution                                                                                        |
| --------------------------------------- | ----------------------------------------- | ----------------------------------------------------------------------------------------------- |
| Device not showing in Test Devices list | Device not marked as test device          | Go to **Users > Find People**, mark the device as a test device, and refresh the A/B Test page. |
| Can’t run multiple A/B tests            | One or more tests are still in draft mode | Publish or enable test mode for each test separately.                                           |
| Variant not appearing on device         | Device not linked correctly               | Reassign the test device in the variant settings and re-publish the test.                       |

***

## FAQs

**Can I run test mode for multiple tests simultaneously?**
Yes. You can now enable test mode for several A/B tests at once. Each test’s status will display **Test Mode** in the dashboard.

**Will test mode affect real users?**
No. Test Mode runs only on devices marked as _test devices_.

**Can I unmark a test device later?**
Yes. Click **Unmark as Test Device** on the user profile to remove it from the test device list.

***

## Summary

The **Preview and Test Mode** feature helps you confidently validate experiments before rollout. By combining device-level targeting with multi-test capability, QA and marketing teams can simulate real-world scenarios across devices and variants efficiently.

***

### [Open Questions]

* [ ] Confirm if screenshots for “Mark as Test Device” and “Preview and Test” are available in the Figma file.
* [ ] Confirm SDK version required for device-level A/B testing.
* [ ] Confirm if “Test Mode” is visible only to users with QA/Tester permissions.

***

### ✅ Style & Structure Notes

* Follows TEC Style Guide and MSTP hierarchy.
* Correct heading structure (H1 → H2 → H3).
* Ordered and unordered lists formatted consistently.
* Image placeholders labeled clearly.
* Internal anchors ready for cross-references from “Run an A/B Test” page.

***

Would you like me to:

* Add a **“Link to this page” section** (for integration into the main A/B Test doc tree)?
* Or produce this as a **standalone page** with navigation metadata (front matter for docs.clevertap.com)?
