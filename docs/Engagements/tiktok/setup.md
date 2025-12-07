---
title: Setup
excerpt: >-
  Learn how to connect, reconnect, or delete your TikTok Ad account with
  CleverTap
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Connecting your TikTok ad account to CleverTap is essential for leveraging your TikTok audiences effectively. By linking your account, you can segment your TikTok users within CleverTap and seamlessly export these segments back to TikTok for targeted advertising and retargeting.

# Connect TikTok Ad Account

To connect your TikTok ad account and start leveraging its advertising features, follow these steps on the CleverTap dashboard.

1. Navigate to *Settings* > *Remarketing* > *Tiktok*.

<Image alt="Tiktok Remarketing - Settings" align="center" border={true} src="https://files.readme.io/449247c6e207c1026a59f0e14098f16c93cbee18b9c68f809e35e86ce6b0db20-TikTok_1.png">
  Tiktok Remarketing - Settings
</Image>

2. Click **Connect Ad Account** > **Authorize Credentials**.

<Image alt="TikTok Remarketing - Create Ad Account" align="center" border={true} src="https://files.readme.io/143dcb505c9314d123a8ab6fe7d52ac173f09b3e675b1f0c0a00bc8e7df3a2b1-2024-09-17_11-21-20_1.gif">
  TikTok Remarketing - Create Ad Account
</Image>

3. Enter your Tiktok Ad account credentials and click **Login**.
4. Authorize CleverTap to manage your TikTok Ad account.

<Image alt="Authorize Ad account" align="center" width="70% " border={true} src="https://files.readme.io/52b5911347360a17a666fc0e3f74da047a179f9d1fa7769239ac2bf9672c95cb-Screenshot_2024-09-19_at_3.24.35_PM.png">
  Authorize Ad account
</Image>

5. Select the accounts you want to add or import.

<Image alt="Select Account to Connect" align="center" border={true} src="https://files.readme.io/b2b8a8babd29309b164a4845d9564c4a7f46f8dee32c82c37d63a1a765a08d41-TikTok_connect_account.png">
  Select Account to Connect
</Image>

After successfully implementing the steps, your TikTok ad account will be integrated into CleverTap.

## Map Properties

After you connect your TikTok account, configure the mapping between TikTok’s export attributes and your CleverTap user properties. Mapping ensures that the correct profile data is exported to TikTok when creating a remarketing audience. If an attribute is not mapped to a CleverTap user property, its column will be blank in the exported audience file, and the option will appear disabled in the campaign setup flow. 

<Image alt="Map Properties - TikTok" align="center" border={true} src="https://files.readme.io/967de81a36a456c72a13d2280a05748e7d5fc9de689ede898bae7b4238974ec0-map_properties_tiktok.png">
  Map Properties - TikTok
</Image>

### Assign User Properties

This section assigns CleverTap user properties to TikTok’s export attributes so that the correct data is included when creating audiences.

1. Click **Map Properties**.
2. For each export attribute, open the drop-down in the **Mapped User Property** column and select the CleverTap user property that contains the relevant data. You can choose from system properties or any custom properties already available in your CleverTap account.
3. Click **Save**.

<Image alt="Property List" align="center" width="50% " border={true} src="https://files.readme.io/1e76cfd348917f0e9078e0af713cee61c0cd595684579a67cc6048ddeba19ab9-property_list_tiktok.png">
  Property List
</Image>

Mapped properties will be available for selection in the What section when you [create a TikTok remarketing campaign](doc:create-remarketing-campaign). Unmapped properties will appear disabled in the campaign setup flow.

### Supported Attributes for TikTok

The following table lists all export attributes supported by TikTok and their descriptions. Use it as a reference when selecting which CleverTap user properties to map.

| Export Attribute           | Description                                                                 |
| -------------------------- | --------------------------------------------------------------------------- |
| Email                      | User’s email address                                                        |
| Phone                      | User’s phone number                                                         |
| First Name                 | User’s first name                                                           |
| Last Name                  | User’s last name                                                            |
| First Name Initial         | First letter of the user’s first name                                       |
| Gender                     | User’s gender                                                               |
| Date of Birth (DOB)        | User’s full date of birth                                                   |
| City                       | User’s city name                                                            |
| State                      | User’s state name                                                           |
| Country                    | User’s country (ISO 3166-1 alpha-2 code)                                    |
| ZIP                        | User’s postal or ZIP code                                                   |
| Google Advertising ID      | Unique, resettable identifier assigned to a device for advertising purposes |
| Identifier for Advertisers | Unique identifier assigned to a device for advertising purposes             |

## Reconnect Ad Account

A **token expiration** occurs when the authentication token that allows your account to connect with CleverTap reaches its validity limit. Tokens are designed to be temporary for security reasons; once expired, they can no longer be used to access the account. This helps protect your data from unauthorized access.

If the token expires, your account may become disconnected, and the status column on the CleverTap dashboard will show *Disconnected*. When you hover over this status, a *Refresh* option will appear. Click **Refresh** to reconnect your account.

## Delete an Account

To delete a TikTok account:

1. Navigate to *Settings* > *Remarketing* > *Tiktok*.
2. Click the Trash icon adjacent to the account you want to delete.

   <Image alt="Delete Ad Account" align="center" border={true} src="https://files.readme.io/249915fe90fbf5ac6041a00b8ebeeefc51ca4ccc28bcbac5e4471cb644ece134-tiktok_delete_account.png">
     Delete Ad Account
   </Image>
3. Click **Delete** on the confirmation dialog box.
