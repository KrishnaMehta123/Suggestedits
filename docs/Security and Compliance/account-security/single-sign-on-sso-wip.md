---
title: Single Sign On (SSO) WIP
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
[block:api-header]
{
  "title": "Overview"
}
[/block]
You can use Single Sign-On (SSO) to access your CleverTap dashboard. You must be on a CleverTap for Enterprises plan and use an identity provider or a custom SAML implementation in order to use SSO with CleverTap.
[block:callout]
{
  "type": "info",
  "body": "You need to be an account admin to set up an SSO.",
  "title": "Account Admin User"
}
[/block]
# Set Up SSO Configuration on CleverTap
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f060048-SSO_setup.png",
        "SSO_setup.png",
        1151,
        687,
        "#fafafb"
      ]
    }
  ]
}
[/block]
## Access Setup Page
As an admin user, from the CleverTap dashboard, navigate to *Organization* > *SSO*. You will be directed to the SSO setup page.

## Configure SAML
To configure SAML, perform the following steps:
1. Copy the entity ID and Assertion Consumer service URL from the CleverTap and paste it in the IdP in Audience URI and Single sign-on URL respectively as shown below.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/89d232f-image8.png",
        "image8.png",
        1999,
        540,
        "#fbfbfc"
      ]
    }
  ]
}
[/block]
2. Validate the Signature hash algorithm and binding to ensure they are the same in the Idp.
  * Signature Hash Algorithm: SHA-256
  * Binding: HTTP POST

3. Provide XML metadata to CleverTap. You can copy the XML MetaData and paste it or upload the file.

CleverTap supports dynamic configuration which requires you to enter the IdP MetaData. This IdP MetaData is provided by your identity provider and will look similar to the screenshot shown below in XML format.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02c38b1-image11.png",
        "image11.png",
        1999,
        655,
        "#fafafa"
      ]
    }
  ]
}
[/block]
This IdP MetaData is provided by your identity provider and will look similar to the screenshot shown below in XML format.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bd84fde-image2.png",
        "image2.png",
        1999,
        715,
        "#efeef0"
      ]
    }
  ]
}
[/block]
4. Set your unique domain URL.
A CleverTap domain, unique to your CleverTap application needs to be provided so that it can be used to authenticate your CleverTap account.
[block:callout]
{
  "type": "info",
  "body": "Please use an easy name to remember as this will be used by your team to log in to the CleverTap account.",
  "title": "Name Selection"
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d6b7fc3-image12.png",
        "image12.png",
        1999,
        296,
        "#fafafb"
      ]
    }
  ]
}
[/block]
This completes your basic setup of SAML SSO. You can test the SSO setup from the CleverTap dashboard to be sure if the setup is done correctly.

## Additional Settings
This section covers additional settings.

### Login with SSO only
Under the *Settings* > *SSO*,  you can find the setting *Require all users to login using SSO*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/849cfd8-image9.png",
        "image9.png",
        1330,
        192,
        "#fafafa"
      ]
    }
  ]
}
[/block]
If you select this option, your team members will not be able to log in to CleverTap directly. They will be forced to log in via the SSO option only.
[block:callout]
{
  "type": "warning",
  "body": "Use this option if your entire team has your domain email id and is set up on your IdP.\n\nIf you have outsourced teams who do not have an email address in your domain, do not select this option as they will not be able to log in to CleverTap.\n\nIf you select this option, you will not be able to create a user from the CleverTap dashboard or assign a role to the user, this will have to manage via the Identity Provider.",
  "title": "Authentication Settings Considerations"
}
[/block]
### Bind Existing Users
Some things to consider:
* If you already have a user setup on CleverTap and want to migrate them to SSO along with their CleverTap roles and account access, select this option.
* This gives you the option to download the users list by copying these user settings and paste them in the custom attributes in your IdP (More on how to set up custom attributes is given below).
* This ensures that all users who are currently on CleverTap’s authentication and authorization will be seamlessly migrated to the IdPs authentication and authorization.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/16cd66a-image3.png",
        "image3.png",
        1460,
        214,
        "#f4f5f7"
      ]
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/817ce89-Screenshot_2020-03-19_at_2.44.15_PM.png",
        "Screenshot 2020-03-19 at 2.44.15 PM.png",
        912,
        738,
        "#dcdcdd"
      ]
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "IdP Setup",
  "body": "Below, you will be able to see how to set up access for the following IdPs:\n1. Okta\n2. OneLogin\n3. Azure\n4. Gsuite\n\nOther IdPs follow similar instructions."
}
[/block]
# Identity Provider Set Up
Identity Provider (IdP) is the authority that verifies and asserts a user's identity and access to a requested resource (the "Service Provider").

Some examples of IdPs are Okta and GSuite.


## Okta Setup

This section covers the Okta setup.

### Create an Application
All IdPs allow you to create an app that you want to access using SSO. Start the setup by creating a CleverTap app in your IdP setup.

The example below is for setting up an app with Okta.

Under *Platform*, select *Web* and under *Sign on method*, select *SAML 2.0*.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2c851bc-image5.png",
        "image5.png",
        1604,
        944,
        "#dee7ee"
      ]
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1f27ba-image10.png",
        "image10.png",
        1999,
        1163,
        "#f9fafa"
      ]
    }
  ]
}
[/block]
### Validate Settings
Validate the Signature hash algorithm and binding to ensure they are the same in the IdP:
  * Signature Hash Algorithm: SHA-256
  * Binding: HTTP POST

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a77e184-Screenshot_2020-03-24_at_1.12.46_PM.png",
        "Screenshot 2020-03-24 at 1.12.46 PM.png",
        1508,
        992,
        "#f6f6f6"
      ]
    }
  ]
}
[/block]
### Attributes 
You have to add some attributes for SSO to work. Attributes for name and email are compulsory in the format given in the screenshot. You need to add an attribute for each accountid you have in CleverTap.

You can then select for each account what role you want to give the users access to at a granular level.

Navigate to *Applications* > Select your application > General > Configure SAML.

The following attributes are mandatory.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5932ccc-Screenshot_2020-03-12_at_3.53.39_PM.png",
        "Screenshot 2020-03-12 at 3.53.39 PM.png",
        1440,
        398,
        "#f6f7f7"
      ]
    }
  ]
}
[/block]
Now if you have two accounts on Clevertap, you need to add the two AcccountId's in the following way:
You can name them as appuser.[Identifier}. As examples, we have used appuser.MainAccRole and appuser.MaiAccRole1.

This tells CleverTap which account a user should have access to. Click on **Next** and **Finish** to complete the process.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8eea100-Screenshot_2020-03-12_at_3.55.31_PM.png",
        "Screenshot 2020-03-12 at 3.55.31 PM.png",
        1440,
        630,
        "#f6f6f6"
      ]
    }
  ]
}
[/block]
Now, we need to define what role the user shoud have for each account.

1. Navigate to *Directory* > *Profile Editor*.
2. Hover on your app and select *Profile*.
3. Add and define what you want to call these attributes and what roles these attributes can get.
4. Click on **Add attribute**.
5. Name the *Variable* as "Your Account Name" to ensure that when assigning a name you can understand what account you are assigning the user to.
6. Ensure you add the Name in Variable as you did earlier for AccountID as MainAccRole and MainAccRole1 from our previous examples above.
7. Click the checkbox for an enumerated list and add all combinations of roles that you can possibly want to assign your user (you can get these combinations from the SSO Settings in the CleverTap dashboard as a CSV and copy-paste. 
[block:callout]
{
  "type": "info",
  "body": "It is important that you always add an attribute member \"NoAccess\" and provide it with an empty \"{}\", so that you can select this value when you do not want to give the user access to this account.",
  "title": "No Access"
}
[/block]
8. Click **Save**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5e4a74f-Screenshot_2020-07-21_at_7.59.17_PM.png",
        "Screenshot 2020-07-21 at 7.59.17 PM.png",
        1444,
        1316,
        "#e2e9ee"
      ]
    }
  ]
}
[/block]
To ensure the correct values are passed to CleverTap, map the attributes correct by performing the following steps:
 
1. Navigate to *Directory* > *Profile Editor*.
2. Click on **Profile** (For your App) > *Mappings*. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea10dd0-Screenshot_2020-07-21_at_8.03.41_PM.png",
        "Screenshot 2020-07-21 at 8.03.41 PM.png",
        2122,
        1330,
        "#eaf0f5"
      ]
    }
  ]
}
[/block]
Now, you need to assign users to your application:
1. Navigate to *Applications* > Select your application > *Assignments*.
2. Select the user and what role you want to give to the user for each account. If you do not want to give the user access to the account, select *noaccess*.
3. Click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/373db05-Screenshot_2020-03-12_at_4.16.31_PM.png",
        "Screenshot 2020-03-12 at 4.16.31 PM.png",
        1392,
        718,
        "#d6e2eb"
      ]
    }
  ]
}
[/block]
###IdP Metadata

* Navigate to *Applications* > Select your application > *Sign On*
* Click on *View Setup Instruction* and from the optional section copy the IDP metadata.

This is the XML Metadata file that you need to upload from the CleverTap dashboard by navigating to *Settings > SSO Settings > Upload XML Metadata.*

## OneLogin Setup

This section will cover the Onelogin setup.

### Create an Application

1. From the Applications tab, select *Applications* from the menu bar.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/721b11f-Screenshot_2021-10-20_at_8.05.02_PM.png",
        "Screenshot 2021-10-20 at 8.05.02 PM.png",
        1474,
        784,
        "#a5a6a7"
      ],
      "border": true
    }
  ]
}
[/block]
2. Click **Add App**.
3. Search for *SAML Custom Connector (Advance)* in the search bar.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7d69db6-1.png",
        "1.png",
        1566,
        271,
        "#cfd1d3"
      ],
      "border": true
    }
  ]
}
[/block]
4. Select **SAML Custom Connector (Advance)** and give *Display Name.  
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c039dd3-2.png",
        "2.png",
        832,
        346,
        "#f1f4f4"
      ],
      "border": true
    }
  ]
}
[/block]
5. Click **Save**.

### Application configuration

1. Navigate to the *Configuration* section and enter the *ACS (Consumer) URL* and* Audience (EntityID). *

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/61ffd10-SSO_CTD.png",
        "SSO CTD.png",
        2614,
        1504,
        "#e6e8e9"
      ]
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Note",
  "body": "You’ll find the ACS (Consumer) URL and Audience (EntityID) by navigating to Organizations -> SSO in the CleverTap dashboard."
}
[/block]

### Attributes

You have to add some attributes for SSO to work. **Name and email are mandatory attributes**. You need to add an attribute for each accountID you have in CleverTap.
You can then select for each account what role you want to give the users access to at a granular level.

You can then select the type of role you want to assign to your users.

1. Navigate to the *Parameter* section and click the** ‘+’** sign to add new fields and also ensure that the Configured by admin button is selected.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c4a4768-4.png",
        "4.png",
        1848,
        244,
        "#f8f9fa"
      ],
      "border": true
    }
  ]
}
[/block]
2. Add Name and Email fields and ensure that *Include in SAML assertion* checkbox is selected. Now, click **Save.**

3. Add value as *FirstName* and *Email* for Name and Email respectively and **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/505e81b-5.png",
        "5.png",
        568,
        460,
        "#f2f5f6"
      ],
      "border": true
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b8607e4-6.png",
        "6.png",
        570,
        480,
        "#f2f4f5"
      ],
      "border": true
    }
  ]
}
[/block]
4. For each account you have in CleverTap, you should add the AccountID as name, and in the value dropdown select *Macro* and then add value attribute, here we have two accounts Account-1 and Account-2.

This tells CleverTap which account a user should have access to.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4858a50-7.png",
        "7.png",
        570,
        523,
        "#f4f6f7"
      ],
      "border": true
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e164c15-8..png",
        "8..png",
        1345,
        526,
        "#fafbfb"
      ],
      "border": true
    }
  ]
}
[/block]
5. Navigate to the *SSO* section and select **SHA-256** from the SAML Signature Algorithm drop-down list and click **Save**.


### Assign Users and Roles

1. Navigate to *Users* (from the top menu) > Users and select the user you want to give access to. On selecting a specific user, the user profile is displayed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e27e88b-9.png",
        "9.png",
        1753,
        305,
        "#d0d3d4"
      ],
      "border": true
    }
  ]
}
[/block]
2. Navigate to *Applications* and add the app which we have created by clicking on the plus sign.
[block:image]
{
  "images": [
    {
      "image": []
    }
  ]
}
[/block]
 
3. Define the role for each account for this user by clicking on the app (we have Test).

* Take the role map JSON that is available in the CSV download (Dashboard > Settings > SSO) for the user-account combination and paste it into the respective attributes for each account.
[block:callout]
{
  "type": "info",
  "title": "Restricting Access",
  "body": "If you do not want to give a user access to the account, define an empty JSON { } that indicates that the user has no access to this account. Refer to the image below for a better understanding."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/21c1acd-11.png",
        "11.png",
        643,
        834,
        "#f6f7f8"
      ],
      "border": true
    }
  ]
}
[/block]
* **Save** the user.


### IdP Metadata
Navigate to *Applications*-> Applications then select your app go to *More Actions* dropdown and click *SAML metadata.*

This will download an XML metadata file that you need to upload to the CleverTap dashboard by navigating to *Organizations -> SSO -> Upload XML metadata *

## Azure Setup

This section covers the Azure setup.

### Create an Application

1. Sign up and create a CleverTap app on the [Azure Portal ](https://portal.azure.com/)
2. From the left navigation panel, select *Azure Active Directory*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1b6307-a1.png",
        "a1.png",
        1734,
        1290,
        "#e5eef4"
      ],
      "border": true
    }
  ]
}
[/block]
3. Select *Overview* from the left menu of *Azure Active Directory* pane.
4. Click **+ Add*  and then select *Enterprise application*.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2981515-az1.png",
        "az1.png",
        1890,
        1250,
        "#eef3f6"
      ],
      "border": true
    }
  ]
}
[/block]
  The Enterprise applications window displays.
5. Click **+Create your own application**. The Create your own application window opens on the right side of the screen.
6. Enter the name of the application and then select the *Integrate any other application you don't find in the gallery (Non-gallery)* option as shown in the following image. 
7. Click **Add** to integrate the application. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7dcdffd-image_4.png",
        "image (4).png",
        2816,
        1140,
        "#f2f0f1"
      ],
      "border": true
    }
  ]
}
[/block]
5. Further, navigate to *Set up single sign on*. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2a58404-image_5.png",
        "image (5).png",
        2282,
        1116,
        "#f9f8f8"
      ],
      "border": true
    }
  ]
}
[/block]
The Single sign-on screen displays the options for configuring single sign-on. 
6. Click **SAML**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0286a85-saml.png",
        "saml.png",
        2864,
        1364,
        "#f7f6f6"
      ],
      "border": true
    }
  ]
}
[/block]
7. Click **Edit**, available next to *Basic SAML Configuration*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3e3ae05-SAML1.png",
        "SAML1.png",
        1794,
        896,
        "#f8f4f4"
      ],
      "border": true
    }
  ]
}
[/block]
  For Basic SAML configuration, you need to get the **Entity ID** and **Assertion Consumer Service URL** from CleverTap dashboard.
9. To get these credentials, navigate to Organization > SSO in the CleverTap dashboard. 
10. Copy *Entity ID* and *Assertion Consumer Service URL* and paste the respective values into the SAML configuration section as shown in the following figure and then click **Save**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/408dc55-image_6.png",
        "image (6).png",
        2500,
        1360,
        "#f8f5f5"
      ],
      "border": true
    }
  ]
}
[/block]
### Map Attributes

To map the attributes:

1. Navigate to the *Attributes & Claims* section under the *Attributes* tab.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d1a187c-ATTR.png",
        "ATTR.png",
        1558,
        364,
        "#fafafa"
      ],
      "border": true
    }
  ]
}
[/block]
2. Add the following attributes for the SSO to work:
* Name and email attributes are mandatory.
* You need to add an attribute for each Account ID you have in CleverTap. 
  This allows you to assign the appropriate role for each account. For example, if you have two Accounts in Clevertap, you need to add both the Account Ids in the following way:

  * You can name them as user.**attribute1 **and user.**attribute2**. Here, we have used *user.jobtitl*e as an example. This helps indicate the account to which the user should have access.

### Assign User Roles
[block:callout]
{
  "type": "info",
  "title": "Note",
  "body": "As a security measure, Azure AD does not issue a token to the user unless it grants access to the user."
}
[/block]
1. Click *User and groups* from the left navigation of the application. A list of already existing users/groups displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a01f83-image_15.png",
        "image (15).png",
        2848,
        1478,
        "#f9f9fa"
      ],
      "border": true
    }
  ]
}
[/block]
2. Click **+Add user** and assign the respective User and groups to the application using the options available at the top of the screen.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/35588fa-assign.png",
        "assign.png",
        2872,
        828,
        "#f9f9f9"
      ],
      "border": true
    }
  ]
}
[/block]
3. Select the appropriate user and click **Select**. 
4. Click **Assign** to assign that user or group to the SAML application.
5. Edit the attributes explicitly or add roles that you want to assign to the users by selecting the specific user profiles. You can also find t (this statement is incomplete)
6. To map the existing user's data with Azure IdP, select the *Bind user's data with your IDP* checkbox available by navigating to *Organization > SSO. 

You can also download the CSV file containing user data by clicking the *Download Users and Roles*.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/890e99f-bind1.png",
        "bind1.png",
        1230,
        300,
        "#f4f5f9"
      ],
      "border": true
    }
  ]
}
[/block]
### IdP Metadata 

1. Download the *Federation Metadata XML* file available under *SAML Signing Certificate* section.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8e97c9f-image_16.png",
        "image (16).png",
        1608,
        528,
        "#f6f2f2"
      ],
      "border": true
    }
  ]
}
[/block]
2. Navigate to CleverTap Dashboard > *Organization* > *SSO* and upload the CSV file under *MetaData XML* as shown in the following figure:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/78fc2d6-xml.png",
        "xml.png",
        1578,
        526,
        "#f9f8f9"
      ],
      "border": true
    }
  ]
}
[/block]
3. After uploading, set a domain URL unique to your CleverTap application to authenticate your CleverTap account.
[block:callout]
{
  "type": "warning",
  "title": "Application Name",
  "body": "Use a name that is easy to remember, as this will be used by your team to log in to the CleverTap account."
}
[/block]
4. Click **Test SSO**. You will get the following response if the configuration is successful:


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7da272e-ssos.png",
        "ssos.png",
        648,
        382,
        "#eceded"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]
## GSuite Setup
Log in to https://admin.google.com/ and login as Admin for your app.

### Attributes
Navigate to *Users* > Click on **More** > Manage Custom Attributes > Add Custom Attributes.

1. You can give a category and description as per your naming policies, a recommendation is that names should be such that you can identify these custom attributes are for your CleverTap SSO setup.
2. For each account you have with CleverTap, create an equivalent entry here with the name of your account. For example, our app has two accounts and the account names are Account_1 and Account_2. 
3. Ensure these attributes are set to *Single value*.
4. Click **Save**. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c045e8f-Screenshot_2020-03-24_at_11.44.42_AM.png",
        "Screenshot 2020-03-24 at 11.44.42 AM.png",
        2798,
        1006,
        "#fcfcfc"
      ]
    }
  ]
}
[/block]
### Create an SAML App
To create an SAML app, perform the following steps:
1. Navigate to *Apps* > *SAML Apps*.
2. Click on the **+** sign to create your new CleverTap SAML App.
3. Add the ACS URL and Entity ID. 
4. Select the checkbox for Signed Response.
5. Name ID as *Basic Information* and *Primary Email* and Name ID format as *Email*. 
[block:callout]
{
  "type": "info",
  "title": "Signed Response",
  "body": "Ensure the checkbox for Signed Response is selected before proceeding."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/81c7366-Screenshot_2020-03-24_at_11.35.13_AM.png",
        "Screenshot 2020-03-24 at 11.35.13 AM.png",
        1740,
        1006,
        "#f4f4f4"
      ]
    }
  ]
}
[/block]
### Attribute Mapping
To map attributes, perform the following steps:
1.  Name and email mapping as depicted in the screenshot are compulsory.
2. For each account you have in CleverTap, you should add the AccountID and select the respective attribute created for this account in the previous step when you created Attributes.
3. Click **Save**.
[block:callout]
{
  "type": "info",
  "title": "AccountID",
  "body": "Admins can find all AccountID's in the CleverTap dashboard under *Settings* > *Account*."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/71265c2-Screenshot_2020-03-24_at_12.00.33_PM.png",
        "Screenshot 2020-03-24 at 12.00.33 PM.png",
        1778,
        1006,
        "#f3f3f3"
      ]
    }
  ]
}
[/block]
### Assign to Users and Roles
To assign to user and roles, perform the following steps:
1. Navigate to *Apps* > *SAML Apps*. 
2. Turn the app *ON for everyone*.  
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1eb85a-Screenshot_2020-03-24_at_12.17.02_PM.png",
        "Screenshot 2020-03-24 at 12.17.02 PM.png",
        2880,
        706,
        "#dee4f4"
      ]
    }
  ]
}
[/block]
3. Navigate to *Users* and click on a user you want to give access to. You need to navigate to *Custom Attributes* and define the role for each account for this user.
4. Take the roleMap JSON that is available in the CSV download (Dashboard > Settings > SSO) for the user-account combination and paste it into the respective attributes for each account.
5. If you do not want to give user access to the account, define an empty JSON { } which indicates that the user has no access for this account.
[block:callout]
{
  "type": "info",
  "title": "Restrict User Access",
  "body": "If you do want to give users access to an account, you need to define an empty JSON which just empty curly braces such as { }."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/12efc07-Screenshot_2020-03-24_at_12.55.03_PM.png",
        "Screenshot 2020-03-24 at 12.55.03 PM.png",
        2164,
        554,
        "#f6f8fb"
      ]
    }
  ]
}
[/block]
### IdP Metadata
Now that the setup is done, under *Service Provider Details*:
1. Click **Manage Certificates**.
2. Download the IdP Metadata.

This is the XML Metadata file that you need to upload from the CleverTap dashboard by navigating to *Settings* > *SSO Settings* > *Upload XML Metadata*.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/55d7a57-Screenshot_2020-03-24_at_12.06.41_PM.png",
        "Screenshot 2020-03-24 at 12.06.41 PM.png",
        1778,
        1148,
        "#f4f4f4"
      ]
    }
  ]
}
[/block]
# Sign In Using SSO
Once you have completed the setup, you can save the settings. Once you have saved the settings, your login via SSO is complete. On the next login, your SSO will be activated.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/314aae0-image6.png",
        "image6.png",
        1999,
        1066,
        "#eef1fa"
      ]
    }
  ]
}
[/block]
## Login
Once your SSO is setup, you can log in to CleverTap using the login with the SSO option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6521ec4-image1.png",
        "image1.png",
        1999,
        978,
        "#eff1fa"
      ]
    }
  ]
}
[/block]
Once you click on **Continue**, you will be redirected to your IdP login page. Once you log in from the IdP, you will be redirected back to your CleverTap dashboard.