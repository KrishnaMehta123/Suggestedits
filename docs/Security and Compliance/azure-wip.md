---
title: Azure (WIP)
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
## Azure Setup

This section provides information about the Azure setup. The process involves the following major steps:

- [Create an application](https://docs.clevertap.com/docs/azure-wip#create-an-application).
- [Map the attributes.](https://docs.clevertap.com/docs/azure-wip#map-attributes)
- [Assign the CleverTap application to the user](https://docs.clevertap.com/docs/azure-wip#assign-clevertap-application-to-user).

### Create an Application

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



5. Click _Create your own application _
6. Enter the name of the application > Select the _Non-gallery application_ option as shown in the image below and click on the "Add "button. 

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



8. Add the _ACS_ and _Entity ID_. (You can find these credentials on the Create SAML connection page on CleverTap). To get these credentials, navigate to CleverTap dashboard > Organization > SSO. Copy the _Entity ID_ and _Assertion Consumer Service URL_>_Create SAML Connection_.
9. Paste the respective values into the SAML configuration section as shown in the screenshot below and click _Save_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06684f2-SAML_Configuration_Azure.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



### Map Attributes

In continuation to the above configuration, ensure that the correct values are passed to CleverTap:

1. In the _Attribute & Claims_ section, you need to map two attributes - name and email appropriately and click _Save_. Refer to the image below:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1d6b809-small-Azure_Attributes.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



> 📘 Note
> 
> If you proceed further with the [recommended method](https://docs.clevertap.com/docs/single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), you need not add any custom attributes and hence you must skip step 2.

2. Refer to this [Azure support document](https://learn.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sync-feature-directory-extensions) to create `accountList` custom attribute.

### Assign CleverTap Application to User

To assign your CleverTap application to users,

1. Navigate to the _Azure Active Directory_ > _Enterprise applications_ > Select CleverTap application.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7ea3826-Enterprise_applications.png",
        null,
        ""
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
        "https://files.readme.io/11871d8-Azure_CleverTap_Applications.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



2. Select _Users and groups_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c11bf9-User.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



3. Click _+Add user/group_ and assign the respective User and groups to the application using the options available at the top of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c3992a-Users_and_Groups.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



4. Select the appropriate user and click _Select_ button. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e0b8cde-Select_user_to_assign.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



5. Further, click the _Assign_ button to assign that user or group to the SAML application as shown below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7af340b-Assign_application.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



To find the credentials for setting up SAML connection on the CleverTap dashboard:

1. Navigate to the _Azure Active Directory_ > _Enterprise applications_ > Select CleverTap application.
2. Select _Single Sign On._
3. Download the Certificate (Base64) or extract the certificate from the Federation Metadata XML from the _SAML Certificates_ section, and copy the _Login URL_(also known as the Sign-in URL) from the _Set up CleverTap_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/faa0f0e-small-Azure_SAML_connection.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



4. Use these credentials to create a SAML connection on the CleverTap dashboard.