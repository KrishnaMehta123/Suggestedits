---
title: Single Sign On (SSO) - Live page copy
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
## Overview

You can use Single Sign-On (SSO) to access your CleverTap dashboard. You use an identity provider or a custom SAML implementation in order to use SSO with CleverTap.

> 📘 Account Admin User
> 
> You need to be an account admin to set up an SSO.

# Set Up SSO Configuration on CleverTap

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/14d6c04-SSO_Nav.png",
        "SSO Nav.png",
        2532
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

## Access Setup Page

As an admin user, from the CleverTap dashboard, navigate to _Organization_ > _SSO_. You will be directed to the SSO setup page.

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
        1999
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

2. Validate the Signature hash algorithm and binding to ensure they are the same in the Idp.

- Signature Hash Algorithm: SHA-256
- Binding: HTTP POST

3. Provide XML metadata to CleverTap. You can copy the XML MetaData and paste it or upload the file.

CleverTap supports dynamic configuration which requires you to enter the IdP MetaData. This IdP MetaData is provided by your identity provider and will look similar to the screenshot shown below in XML format.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02c38b1-image11.png",
        "image11.png",
        1999
      ],
      "align": "center",
      "border": true
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
        1999
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

4. Set your unique domain URL.  
   A CleverTap domain, unique to your CleverTap application needs to be provided so that it can be used to authenticate your CleverTap account.

> 📘 Name Selection
> 
> Please use an easy name to remember as this will be used by your team to log in to the CleverTap account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d6b7fc3-image12.png",
        "image12.png",
        1999
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

This completes your basic setup of SAML SSO. You can test the SSO setup from the CleverTap dashboard to be sure if the setup is done correctly.

## Additional Settings

This section covers additional settings.

### Login with SSO only

Under the _Settings_ > _SSO_,  you can find the setting _Require all users to login using SSO_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/849cfd8-image9.png",
        "image9.png",
        1330
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

If you select this option, your team members will not be able to log in to CleverTap directly. They will be forced to log in via the SSO option only.

> 🚧 Authentication Settings Considerations
> 
> Use this option if your entire team has your domain email id and is set up on your IdP.
> 
> If you have outsourced teams who do not have an email address in your domain, do not select this option as they will not be able to log in to CleverTap.
> 
> If you select this option, you will not be able to create a user from the CleverTap dashboard or assign a role to the user, this will have to manage via the Identity Provider.

### Bind Existing Users

Some things to consider:

- If you already have a user setup on CleverTap and want to migrate them to SSO along with their CleverTap roles and account access, select this option.
- This gives you the option to download the users list by copying these user settings and paste them in the custom attributes in your IdP (More on how to set up custom attributes is given below).
- This ensures that all users who are currently on CleverTap’s authentication and authorization will be seamlessly migrated to the IdPs authentication and authorization.
- If you want to assign a custom role, use the below syntax to assign a custom role with SSO.  
  {"customRoles":["CampaignCreator"]}. In this case, CampaignCreator is a custom role name.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/16cd66a-image3.png",
        "image3.png",
        1460
      ],
      "align": "center",
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
        "https://files.readme.io/817ce89-Screenshot_2020-03-19_at_2.44.15_PM.png",
        "Screenshot 2020-03-19 at 2.44.15 PM.png",
        912
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

> 📘 IdP Setup
> 
> Below, you will be able to see how to set up access for the following IdPs:
> 
> 1. Okta
> 2. OneLogin
> 3. Azure
> 4. Gsuite
> 
> Other IdPs follow similar instructions.

# Identity Provider Set Up

Identity Provider (IdP) is the authority that verifies and asserts a user's identity and access to a requested resource (the "Service Provider").

Some examples of IdPs are Okta and GSuite.

## Okta Setup

This section covers the Okta setup.

### Create an Application

All IdPs allow you to create an app that you want to access using SSO. Start the setup by creating a CleverTap app in your IdP setup.

The example below is for setting up an app with Okta.

Under _Platform_, select _Web_ and under _Sign on method_, select _SAML 2.0_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2c851bc-image5.png",
        "image5.png",
        1604
      ],
      "align": "center",
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
        "https://files.readme.io/a1f27ba-image10.png",
        "image10.png",
        1999
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

### Validate Settings

Validate the Signature hash algorithm and binding to ensure they are the same in the IdP:

- Signature Hash Algorithm: SHA-256
- Binding: HTTP POST

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a77e184-Screenshot_2020-03-24_at_1.12.46_PM.png",
        "Screenshot 2020-03-24 at 1.12.46 PM.png",
        1508
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

### Attribute Mapping

You have to add some attributes for SSO to work. Attributes for name and email are compulsory in the format given in the screenshot. You need to add an attribute for each accountid you have in CleverTap.

You can then select for each account what role you want to give the users access to at a granular level.

Navigate to _Applications_ > Select your application > General > Configure SAML.

The following attributes are mandatory.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5932ccc-Screenshot_2020-03-12_at_3.53.39_PM.png",
        "Screenshot 2020-03-12 at 3.53.39 PM.png",
        1440
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

Now if you have two accounts on Clevertap, you need to add the two AcccountId's in the following way:  
You can name them as appuser.\[Identifier}. As examples, we have used appuser.MainAccRole and appuser.MaiAccRole1.

This tells CleverTap which account a user should have access to. Click on **Next** and **Finish** to complete the process.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8eea100-Screenshot_2020-03-12_at_3.55.31_PM.png",
        "Screenshot 2020-03-12 at 3.55.31 PM.png",
        1440
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

### Assign User Roles

Now, we need to define what role the user should have for each account.

1. Navigate to _Directory_ > _Profile Editor_.
2. Hover on your app and select _Profile_.
3. Add and define what you want to call these attributes and what roles these attributes can get.
4. Click on **Add attribute**.
5. Name the _Variable_ as "Your Account Name" to ensure that when assigning a name you can understand what account you are assigning the user to.
6. Ensure you add the Name in Variable as you did earlier for AccountID as MainAccRole and MainAccRole1 from our previous examples above.
7. Click the checkbox for an enumerated list and add all combinations of roles that you can possibly want to assign your user (you can get these combinations from the SSO Settings in the CleverTap dashboard as a CSV and copy-paste. For defining custom roles, refer to [Bind existing users](https://docs.clevertap.com/docs/single-sign-on-sso#bind-existing-users).

> 📘 No Access
> 
> It is important that you always add an attribute member "NoAccess" and provide it with an empty "{}", so that you can select this value when you do not want to give the user access to this account.

8. Click **Save**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5e4a74f-Screenshot_2020-07-21_at_7.59.17_PM.png",
        "Screenshot 2020-07-21 at 7.59.17 PM.png",
        1444
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

To ensure the correct values are passed to CleverTap, map the attributes correct by performing the following steps:

1. Navigate to _Directory_ > _Profile Editor_.
2. Click on **Profile** (For your App) > _Mappings_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea10dd0-Screenshot_2020-07-21_at_8.03.41_PM.png",
        "Screenshot 2020-07-21 at 8.03.41 PM.png",
        2122
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

Now, you need to assign users to your application:

1. Navigate to _Applications_ > Select your application > _Assignments_.
2. Select the user and what role you want to give to the user for each account. If you do not want to give the user access to the account, select _noaccess_.
3. Click **Save**.

![](https://files.readme.io/373db05-Screenshot_2020-03-12_at_4.16.31_PM.png "Screenshot 2020-03-12 at 4.16.31 PM.png")

### IdP Metadata

- Navigate to _Applications_ > Select your application > _Sign On_
- Click on _View Setup Instruction_ and from the optional section copy the IDP metadata.

![](https://files.readme.io/740efa2-IDP1.png "IDP1.png")

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d86184e-idp_2.png",
        "idp 2.png",
        1058
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

This is the XML Metadata that you need to upload from the CleverTap dashboard by navigating to _Settings > SSO Settings > Upload XML Metadata._

## OneLogin Setup

This section will cover the Onelogin setup.

### Create an Application

1. From the Applications tab, select _Applications_ from the menu bar.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/721b11f-Screenshot_2021-10-20_at_8.05.02_PM.png",
        "Screenshot 2021-10-20 at 8.05.02 PM.png",
        1474
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

2. Click **Add App**.
3. Search for _SAML Custom Connector (Advance)_ in the search bar.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7d69db6-1.png",
        "1.png",
        1566
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

4. Select **SAML Custom Connector (Advance)** and give \*Display Name.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c039dd3-2.png",
        "2.png",
        832
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

5. Click **Save**.

### Application configuration

1. Navigate to the _Configuration_ section and enter the _ACS (Consumer) URL_ and_ Audience (EntityID). _

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/61ffd10-SSO_CTD.png",
        "SSO CTD.png",
        2614
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

> 📘 Note
> 
> You’ll find the ACS (Consumer) URL and Audience (EntityID) by navigating to Organizations -> SSO in the CleverTap dashboard.

### Attribute Mapping

You have to add some attributes for SSO to work. **Name and email are mandatory attributes**. You need to add an attribute for each accountID you have in CleverTap.  
You can then select for each account what role you want to give the users access to at a granular level.

You can then select the type of role you want to assign to your users.

1. Navigate to the _Parameter_ section and click the** ‘+’** sign to add new fields and also ensure that the Configured by admin button is selected.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c4a4768-4.png",
        "4.png",
        1848
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

2. Add Name and Email fields and ensure that _Include in SAML assertion_ checkbox is selected. Now, click **Save.**

3. Add value as _FirstName_ and _Email_ for Name and Email respectively and **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/505e81b-5.png",
        "5.png",
        568
      ],
      "align": "center",
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
        570
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

4. For each account you have in CleverTap, you should add the AccountID as name, and in the value dropdown select _Macro_ and then add value attribute, here we have two accounts Account-1 and Account-2.

This tells CleverTap which account a user should have access to.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4858a50-7.png",
        "7.png",
        570
      ],
      "align": "center",
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
        1345
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

5. Navigate to the _SSO_ section and select **SHA-256** from the SAML Signature Algorithm drop-down list and click **Save**.

### Assign User Roles

1. Navigate to _Users_ (from the top menu) > Users and select the user you want to give access to. On selecting a specific user, the user profile is displayed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e27e88b-9.png",
        "9.png",
        1753
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

2. Navigate to _Applications_ and add the app which we have created by clicking on the plus sign.
3. Define the role for each account for this user by clicking on the app (we have Test).

For defining custom roles, refer to [Bind existing users](https://docs.clevertap.com/docs/single-sign-on-sso#bind-existing-users).

- Take the role map JSON that is available in the CSV download (Dashboard > Settings > SSO) for the user-account combination and paste it into the respective attributes for each account.

> 📘 Restricting Access
> 
> If you do not want to give a user access to the account, define an empty JSON { } that indicates that the user has no access to this account. Refer to the image below for a better understanding.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/21c1acd-11.png",
        "11.png",
        643
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

- **Save** the user.

### IdP Metadata

Navigate to _Applications_-> Applications then select your app go to _More Actions_ dropdown and click _SAML metadata._

This will download an XML metadata file that you need to upload to the CleverTap dashboard by navigating to _Organizations -> SSO -> Upload XML metadata _

## Azure Setup

This section will cover the Azure setup.

### Creating an Application

1. Start the setup by signing up and creating a CleverTap app on the [Azure Portal ](https://portal.azure.com/)
2. From the left navigation panel, select _Azure Active Directory._

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1b6307-a1.png",
        "a1.png",
        1734
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

3. Select _Enterprise applications_ from the _Azure Active Directory_ pane.
4. Click _+ Add_  > _Enterprise application_

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2981515-az1.png",
        "az1.png",
        1890
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

5. Enter the name of the application > Select the _Non-gallery application_ option as shown in the image below and click on the "Add "button. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7dcdffd-image_4.png",
        "image (4).png",
        2816
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

5. Further, navigate to ** Setup Single sign-on**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2a58404-image_5.png",
        "image (5).png",
        2282
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

6. The next screen presents the options for configuring single sign-on. Click on _SAML_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0286a85-saml.png",
        "saml.png",
        2864
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

7. Now, click the _Edit_ option available next to _Basic SAML configuration_

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3e3ae05-SAML1.png",
        "SAML1.png",
        1794
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

8. For Basic SAML configuration you need to get the **Entity ID** and **Assertion Consumer Service URL** from CleverTap dashboard.
9. To get these credentials, navigate to CleverTap dashboard > Organization > SSO. Copy the _Entity ID_ and _Assertion Consumer Service URL_.
10. Paste the respective values into the SAML configuration section as shown in the screenshot below and click _Save_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/408dc55-image_6.png",
        "image (6).png",
        2500
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

### Attribute Mapping

Navigate to the _Attributes & Claims_ section under the _Attributes_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d1a187c-ATTR.png",
        "ATTR.png",
        1558
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

Add the following attributes for the SSO to work:

- Name and email attributes are mandatory.

- You need to add an attribute for each Account ID you have in CleverTap. This allows you to assign the appropriate role for each account. For example, if you have two Accounts in Clevertap, you need to add both the Account Ids in the following way:

- You can name them as user.**attribute1 **and user.**attribute2**. Here, we have used user.jobtitle as an example. This helps indicate the account to which the user should have access.

### Assign User Roles

> 📘 Note
> 
> As a security measure, Azure AD does not issue a token to the user unless it grants access to the user.

1. Click _User and groups_ from the left navigation of the application. A list of already existing users/groups will be displayed.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a01f83-image_15.png",
        "image (15).png",
        2848
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

2. Click \_+Add user \_and Assign the respective User and groups to the application using the options available at the top of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/35588fa-assign.png",
        "assign.png",
        2872
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

3. Select the appropriate user and click _Select_ button. 
4. Further, click the _Assign_ button to assign that user or group to the SAML application.
5. You can explicitly edit the attributes or add roles you want to assign to the users. You can create custom attributes for your setup where you can define specific roles ( for example, {"role: "Admin"} ) as shown in the image below. For defining custom roles, refer to [Bind existing users](https://docs.clevertap.com/docs/single-sign-on-sso#bind-existing-users).

![](https://files.readme.io/7263f25-ss.png "ss.png")

6. To map the existing user's data with Azure IdP, select the _Bind user's data with your IDP_ option available in the CleverTap dashboard (navigate to _Organization > SSO > select the Bind user's data with your IDP_ checkbox). Click the _Download Users and Roles_ link to download the CSV file containing user data. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/890e99f-bind1.png",
        "bind1.png",
        1230
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

### IdP Metadata

1. Download the _Federation Metadata XML_ file available under _SAML Signing Certificate_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8e97c9f-image_16.png",
        "image (16).png",
        1608
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

2. Navigate to CleverTap Dashboard > _Organization_ > _SSO_ and upload the CSV file under _MetaData XML_ as shown below:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/78fc2d6-xml.png",
        "xml.png",
        1578
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

3. Once done, set a domain URL unique to your CleverTap application so that it can be used to authenticate your CleverTap account.

> 🚧 Note
> 
> Use a name that is easy to remember as this will be used by your team to log in to the CleverTap account.

4. Click _Test SSO_ button and if the configuration is properly done, then you will get the following response:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7da272e-ssos.png",
        "ssos.png",
        648
      ],
      "align": "center",
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]

## GSuite Setup

Log in to <https://admin.google.com/> and login as Admin for your app.

### Attributes

Navigate to _Users_ > Click on **More** > Manage Custom Attributes > Add Custom Attributes.

1. You can give a category and description as per your naming policies, a recommendation is that names should be such that you can identify these custom attributes are for your CleverTap SSO setup.
2. For each account you have with CleverTap, create an equivalent entry here with the name of your account. For example, our app has two accounts and the account names are Account_1 and Account_2. 
3. Ensure these attributes are set to _Single value_.
4. Click **Save**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c045e8f-Screenshot_2020-03-24_at_11.44.42_AM.png",
        "Screenshot 2020-03-24 at 11.44.42 AM.png",
        2798
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

### Create an SAML App

To create an SAML app, perform the following steps:

1. Navigate to _Apps_ > _SAML Apps_.
2. Click on the **+** sign to create your new CleverTap SAML App.
3. Add the ACS URL and Entity ID. 
4. Select the checkbox for Signed Response.
5. Name ID as _Basic Information_ and _Primary Email_ and Name ID format as _Email_. 

> 📘 Signed Response
> 
> Ensure the checkbox for Signed Response is selected before proceeding.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/81c7366-Screenshot_2020-03-24_at_11.35.13_AM.png",
        "Screenshot 2020-03-24 at 11.35.13 AM.png",
        1740
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

### Attribute Mapping

To map attributes, perform the following steps:

1. Name and email mapping as depicted in the screenshot are compulsory.
2. For each account you have in CleverTap, you should add the AccountID and select the respective attribute created for this account in the previous step when you created Attributes.
3. Click **Save**.

> 📘 AccountID
> 
> Admins can find all AccountID's in the CleverTap dashboard under _Settings_ > _Account_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/71265c2-Screenshot_2020-03-24_at_12.00.33_PM.png",
        "Screenshot 2020-03-24 at 12.00.33 PM.png",
        1778
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

### Assign to Users and Roles

To assign to user and roles, perform the following steps:

1. Navigate to _Apps_ > _SAML Apps_. 
2. Turn the app _ON for everyone_.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1eb85a-Screenshot_2020-03-24_at_12.17.02_PM.png",
        "Screenshot 2020-03-24 at 12.17.02 PM.png",
        2880
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

3. Navigate to _Users_ and click on a user you want to give access to. You need to navigate to _Custom Attributes_ and define the role for each account for this user.
4. Take the roleMap JSON that is available in the CSV download (Dashboard > Settings > SSO) for the user-account combination and paste it into the respective attributes for each account.
5. If you do not want to give user access to the account, define an empty JSON { } which indicates that the user has no access to this account.

For defining custom roles, refer to [Bind existing users](https://docs.clevertap.com/docs/single-sign-on-sso#bind-existing-users).

> 📘 Restrict User Access
> 
> If you do want to give users access to an account, you need to define an empty JSON which just empty curly braces such as { }.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/12efc07-Screenshot_2020-03-24_at_12.55.03_PM.png",
        "Screenshot 2020-03-24 at 12.55.03 PM.png",
        2164
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

### IdP Metadata

Now that the setup is done, under _Service Provider Details_:

1. Click **Manage Certificates**.
2. Download the IdP Metadata.

This is the XML Metadata file that you need to upload from the CleverTap dashboard by navigating to _Settings_ > _SSO Settings_ > _Upload XML Metadata_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/55d7a57-Screenshot_2020-03-24_at_12.06.41_PM.png",
        "Screenshot 2020-03-24 at 12.06.41 PM.png",
        1778
      ],
      "align": "center",
      "border": true
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
        "https://files.readme.io/21cef6a-sso1.png",
        "sso1.png",
        2704
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

## Login

Once your SSO is set up, you can log in to CleverTap using the login with the SSO option.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f54a459-sso2.png",
        "sso2.png",
        2674
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]

Once you click on **Continue**, you will be redirected to your IdP login page. Once you log in from the IdP, you will be redirected back to your CleverTap dashboard.