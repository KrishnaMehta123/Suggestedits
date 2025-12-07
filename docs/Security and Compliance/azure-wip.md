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

* [Create an application](https://docs.clevertap.com/docs/azure-wip#create-an-application).
* [Map the attributes.](https://docs.clevertap.com/docs/azure-wip#map-attributes)
* [Assign the CleverTap application to the user](https://docs.clevertap.com/docs/azure-wip#assign-clevertap-application-to-user).

### Create an Application

1. Start the setup by signing up and creating a CleverTap app on the [Azure Portal ](https://portal.azure.com/)
2. From the left navigation panel, select *Azure Active Directory.*

<Image title="a1.png" alt={1734} align="center" className="border" border={true} src="https://files.readme.io/b1b6307-a1.png" />

3. Select *Enterprise applications* from the *Azure Active Directory* pane.
4. Click *+ Add*  > *Enterprise application*

<Image title="az1.png" alt={1890} align="center" className="border" border={true} src="https://files.readme.io/2981515-az1.png" />

5. Click *Create your own application*
6. Enter the name of the application > Select the *Non-gallery application* option as shown in the image below and click on the "Add "button. 

<Image title="image (4).png" alt={2816} align="center" className="border" border={true} src="https://files.readme.io/7dcdffd-image_4.png" />

5. Further, navigate to **Setup Single sign-on** . 

<Image title="image (5).png" alt={2282} align="center" className="border" border={true} src="https://files.readme.io/2a58404-image_5.png" />

6. The next screen presents the options for configuring single sign-on. Click on *SAML*.

<Image title="saml.png" alt={2864} align="center" className="border" border={true} src="https://files.readme.io/0286a85-saml.png" />

7. Now, click the *Edit* option available next to *Basic SAML configuration*

<Image title="SAML1.png" alt={1794} align="center" className="border" border={true} src="https://files.readme.io/3e3ae05-SAML1.png" />

8. Add the *ACS* and *Entity ID*. (You can find these credentials on the Create SAML connection page on CleverTap). To get these credentials, navigate to CleverTap dashboard > Organization > SSO. Copy the *Entity ID* and *Assertion Consumer Service URL*>*Create SAML Connection*.
9. Paste the respective values into the SAML configuration section as shown in the screenshot below and click *Save*.

<Image align="center" className="border" border={true} src="https://files.readme.io/06684f2-SAML_Configuration_Azure.png" />

### Map Attributes

In continuation to the above configuration, ensure that the correct values are passed to CleverTap:

1. In the *Attribute & Claims* section, you need to map two attributes - name and email appropriately and click *Save*. Refer to the image below:

<Image align="center" className="border" border={true} src="https://files.readme.io/1d6b809-small-Azure_Attributes.png" />

> 📘 Note
>
> If you proceed further with the [recommended method](https://docs.clevertap.com/docs/single-sign-on-sso#add-a-list-of-names-and-emails-only-recommended), you need not add any custom attributes and hence you must skip step 2.

2. Refer to this [Azure support document](https://learn.microsoft.com/en-us/azure/active-directory/hybrid/how-to-connect-sync-feature-directory-extensions) to create `accountList` custom attribute.

### Assign CleverTap Application to User

To assign your CleverTap application to users,

1. Navigate to the *Azure Active Directory* > *Enterprise applications* > Select CleverTap application.

<Image align="center" className="border" border={true} src="https://files.readme.io/7ea3826-Enterprise_applications.png" />

<Image align="center" className="border" border={true} src="https://files.readme.io/11871d8-Azure_CleverTap_Applications.png" />

2. Select *Users and groups*.

<Image align="center" className="border" border={true} src="https://files.readme.io/3c11bf9-User.png" />

3. Click *+Add user/group* and assign the respective User and groups to the application using the options available at the top of the screen.

<Image align="center" className="border" border={true} src="https://files.readme.io/3c3992a-Users_and_Groups.png" />

4. Select the appropriate user and click *Select* button. 

<Image align="center" className="border" border={true} src="https://files.readme.io/e0b8cde-Select_user_to_assign.png" />

5. Further, click the *Assign* button to assign that user or group to the SAML application as shown below.

<Image align="center" className="border" border={true} src="https://files.readme.io/7af340b-Assign_application.png" />

To find the credentials for setting up SAML connection on the CleverTap dashboard:

1. Navigate to the *Azure Active Directory* > *Enterprise applications* > Select CleverTap application.
2. Select *Single Sign On.*
3. Download the Certificate (Base64) or extract the certificate from the Federation Metadata XML from the *SAML Certificates* section, and copy the *Login URL*(also known as the Sign-in URL) from the *Set up CleverTap* section.

<Image align="center" className="border" border={true} src="https://files.readme.io/faa0f0e-small-Azure_SAML_connection.png" />

4. Use these credentials to create a SAML connection on the CleverTap dashboard.
