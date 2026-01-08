---
title: Device Previews for A/B Tests
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

## Overview

Before publishing your A/B tests, you can **preview and test variants across multiple devices** to ensure everything works as expected. CleverTap’s enhanced A/B Test feature lets you test on registered devices, view live variants, and run multiple tests in _Test Mode_ at once.

The **Preview and Test Mode** in CleverTap enables you to:

* Mark devices as _test devices_ and target them for QA.
* Assign specific variants to individual devices or user profiles.
* Run and preview multiple A/B tests simultaneously in test mode.
* Verify app behavior and visual consistency before rollout.

This feature is designed for QA, marketing, and product teams who want complete control over their A/B testing environment.

## Prerequisites

Before testing an A/B experiment:

* Ensure your **CleverTap SDK** is updated to the latest version that supports test device registration.
* You must have **A/B test creation** and **test mode access** permissions.
* The devices you plan to use for testing must be **registered as test devices**.

## Step 1: Mark a Device as a Test Device

To register a device for testing:

1. Go to **Users → Find People**.
2. Search for a user profile using **Identity** or **CleverTap ID**.
3. Under the **Devices** section, click **Mark as Test Device**.
4. The button label changes to **Unmark as Test Device** when active.

> **Note:**
> You can mark multiple devices on the same user profile. Only devices marked as test devices appear in the **Test Devices** selector during A/B test setup.

## Step 2: Assign Test Devices to Variants

Once you’ve registered test devices:

1. Open an A/B test under **Product Experiences → A/B Tests**.
2. Go to the **Variables** tab and click the **+ Add Segment** icon.
3. In the segment list, choose **Test Devices → Registered Test Devices**.
4. Select your desired test devices and associate them with a variant.
5. Click **Save** to confirm the configuration.

This allows different devices under the same profile to preview distinct variants, such as:

* **Variant A** on the _Home screen_ of an iPhone
* **Variant B** on the _Settings screen_ of a Pixel device

## Step 3: Enable Preview and Test Mode

After assigning variants:

1. In the **A/B Tests** list, click **Preview and Test** for your chosen test.
2. The status updates to **Test Mode**, visible beside the test name.
3. Launch your app on a registered test device to preview assigned variants in real time.

> **Tip:**
> You can now enable _Test Mode_ for **multiple A/B tests simultaneously**, making parallel QA testing possible across teams.

## Step 4: View and Manage Active Tests

The **Device Previews** section lets you view and control all your ongoing test sessions.

<Image alt="Screenshot showing Device Previews table with test profiles, active preview status, and variants" border={false} src="/mnt/data/0cd34e63-1709-465e-bbb0-f6fb809a782e.png" />

Each entry shows:

* **Test User or Profile Name**
* **Preview Status** (Active or Inactive)
* **Preview Devices** (number of devices linked)
* **Variant** assigned to that device

Use this panel to:

* Start or stop previews
* Deselect or clear specific devices
* Quickly compare variant performance in real-time environments

## Step 5: Stop or Update a Test Session

To modify or stop an active test session:

1. Click **View Running Tests** in the A/B Test dashboard.
2. Review the profiles and devices currently in _Test Mode_.
3. Use:

   * **Update Test** – to add or remove devices.
   * **Stop Test** – to end test mode for that session.

> **Note:**
> Stopping a test only removes the device from test mode. It does not affect your published A/B test configuration.

## Troubleshooting

| Issue                          | Cause                                     | Solution                                                                            |
| ------------------------------ | ----------------------------------------- | ----------------------------------------------------------------------------------- |
| Test device not visible        | Device not registered                     | Go to **Find People**, mark the device as a test device, and refresh the dashboard. |
| Unable to start multiple tests | Another test is still in single-test mode | Ensure all tests are saved and enable _Test Mode_ for each individually.            |
| Variant not loading            | Incorrect device linkage                  | Verify the device’s variant assignment in the **Variables** tab and re-publish.     |

## FAQs

**Can I run multiple tests in Test Mode?**
Yes. You can now preview and test multiple A/B experiments simultaneously.

**Do test devices affect production users?**
No. Test Mode is isolated — only registered test devices see variant changes.

**Can I unmark a test device later?**
Yes. Click **Unmark as Test Device** on the user’s profile page at any time.

<br />
