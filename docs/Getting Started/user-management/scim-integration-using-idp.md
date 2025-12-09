---
title: SCIM Integration using IdP
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

CleverTap supports SCIM-based provisioning through dedicated endpoints, applying and validating access details sent from your IDP. The SCIM token determines which endpoint to use and is generated with the appropriate configuration for IDP-based flows.

* IDP-enabled tokens use: `/scim/v2/idp/users`
* Non-IDP tokens use: `/scim/v2/users`

When regenerating a token, update it wherever it is configured.

## Apply Required Fields for SCIM Provisioning

Review the mandatory fields your IDP must include in each SCIM request. CleverTap validates these fields before applying access changes.

A valid SCIM request must include:

* `userName` (email)
* `name.givenName` and `name.familyName`
* `active` set to `true` for new users
* `accounts[]` containing valid account details
* `invitedBy` referencing an admin user
* Roles and teams that exist for the account
* Account IDs that belong to the associated parent–child structure

## Provision Users Through IDP Without SSO

Use this flow when your IDP handles provisioning but authentication does not rely on SSO. CleverTap applies access based on the SCIM request, and the user completes authentication separately.

* The IDP sends SCIM provisioning requests to CleverTap.
* CleverTap creates or updates the user.
* No invite email is sent during provisioning.
* The user completes authentication according to your setup.
* If using Auth0, the user must set their password via the reset flow.
* Roles, teams, and statuses must be valid for the account.

### Supported Operations

CleverTap supports four SCIM operations:

* POST (create user)
* PUT (update user)
* DELETE (remove access)
* GET (retrieve user)

### Use This Flow When

* Your IDP manages provisioning only.
* SSO is not used for authentication.

## Provision Users Through IDP With SSO

Use this flow when the IDP provisions users, and authentication occurs through SSO. CleverTap applies the access details received from SCIM, while login is handled outside CleverTap.

* The token must be created with the IDP flag enabled.
* Use the endpoint `/scim/v2/idp/users`.
* The IDP manages identity and access attributes.
* Users authenticate entirely through SSO.
* No invite email is issued.
* CleverTap applies the access attributes as provided.

### Behavior

* Provisioned users appear in the CleverTap Users section.
* Authentication is delegated to the SSO provider.
* CleverTap does not store or generate passwords for SSO users.
* Only admin users may appear in `invitedBy`.

### **Use This Flow When**

* Your organization uses SSO for login.
* The IDP is the single source of truth for identity and attributes.

## Use SCIM Through Direct API Requests (Non-IDP Mode)

Use this mode when you want to manage provisioning without an IDP. This approach suits internal automation tools or custom provisioning systems.

* Generate the token without the IDP flag.
* Use the endpoint `/scim/v2/users`.
* Follow the SCIM-compatible structure required for API requests.
* All validation rules from the transcript apply to this flow.

## Payload for IDP Provisioning

Use this structure when constructing IDP-originated provisioning requests. CleverTap validates the full request before applying access changes.

```json
{
  "userName": "<email>",
  "name": {
    "givenName": "<firstName>",
    "familyName": "<lastName>"
  },
  "active": true,
  "accounts": [
    {
      "accountId": "<encodedAccountId>",
      "teams": "TeamA,TeamB",
      "roles": "roleA,roleB",
      "status": "active"
    }
  ],
  "invitedBy": "<adminEmail>"
}
```

### Validation Rules 

* Missing fields produce explicit errors.
* Invalid roles or teams return validation errors.
* Status must be `active`, `revoke`, or `delete`.
* At least one `accounts[]` entry must be `active`.
* Account hierarchy rules apply.
* `invitedBy` must reference an admin user.

SCIM provisioning does not trigger an invite email. Users complete authentication through your chosen identity method.

## Manage Password Handling for Non-SSO Users

Use this section to understand how CleverTap handles passwords in IDP-based flows where SSO is not used.

* If Auth0 is used, CleverTap generates a random password internally.
* Users must set their password using the “Forgot Password” flow.
* CleverTap does not display or store the generated password.

## Troubleshooting

Use this section to identify common issues encountered during SCIM provisioning and understand their likely causes.

### **Provisioning Errors**

* Invalid role or team
* Unsupported or incorrect account ID
* Missing required fields
* Non-admin specified in `invitedBy`
* Unsupported status value

### **Authentication Issues**

* Missing token in the request
* Token expired or not updated in the IDP configuration

### **User Not Appearing in Dashboard**

* Required fields missing from the payload
* Status not set to `active` on creation
* Account does not belong to the parent–child structure

## Best Practices for IDP-Based Provisioning

Use these recommendations to ensure reliable, predictable SCIM integration.

* Use a dedicated SCIM token for IDP provisioning.
* Update the token in the IDP only when it is regenerated.
* Ensure `invitedBy` always references an admin user.
* Validate roles and teams in CleverTap before mapping them in your IDP.
* Test provisioning using a non-production account first.

<br />

***

# Overview

This guide explains how to integrate CleverTap SCIM provisioning with an identity provider. It describes how SCIM behaves when an IDP manages provisioning, how token configuration determines the required endpoint, and how provisioning flows operate for accounts with and without SSO.

CleverTap supports SCIM provisioning through dedicated endpoints that accept SCIM-compatible requests from your IDP.

To integrate SCIM with an IDP, generate a SCIM token in the CleverTap dashboard.
When generating the token, select whether provisioning is used with an IDP.

The token determines the SCIM mode:

* IDP-enabled token uses `/scim/v2/idp/users`
* Non-IDP token uses `/scim/v2/users`

Regenerate the token only when necessary, and update it in the IDP configuration accordingly.

## How SCIM Works With IDPs

When an IDP provisions a user, it sends SCIM-formatted requests to the CleverTap SCIM endpoint. CleverTap validates the request, processes the provisioning action, and applies user access based on the request payload.

The request must include:

* A valid `userName` (email)
* `name.givenName` and `name.familyName`
* `active` set to `true` when creating a user
* An `accounts[]` list with valid account details
* A valid `invitedBy` field referencing an admin user
* Roles and teams that exist in the specified account
* Account IDs that belong to the parent or child account structure associated with the token

Your IDP must pass these fields as required.

# IDP Without SSO

In this flow, the IDP provisions users through SCIM, and authentication is handled fully by the organization’s SSO provider. CleverTap applies the roles and access details in the SCIM request, while login occurs outside CleverTap.

Key characteristics:

* The IDP sends SCIM provisioning requests to CleverTap.
* SCIM provisioning creates or updates the user in the CleverTap dashboard.
* CleverTap does not send an invite email during provisioning.
* The user completes authentication setup separately based on the organization’s configuration.
* If Auth0 is used, the user sets their password using the Auth0 reset process.
* Roles, teams, and statuses must be valid for the specified account.

## Supported Operations

CleverTap supports:

* Create user (POST)
* Update user (PUT)
* Delete or revoke access (DELETE)
* Retrieve user (GET)

## When to Use This Flow

* The organization uses an IDP only for provisioning.
* Dashboard access does not rely on SSO authentication.

# IDP With SSO

In this flow, the IDP provisions users through SCIM, and the organization’s SSO provider handles authentication. CleverTap applies the access details from the SCIM request, and user login is managed outside CleverTap.

* The token must be created with the IDP flag enabled.
* The endpoint must use `/scim/v2/idp/users`.
* The IDP manages user identity and provisioning.
* Users authenticate through SSO.
* CleverTap does not send an invite email.
* Roles, teams, and statuses come from the SCIM request.

## Behavior

* Provisioned users appear in the CleverTap Users section.
* Authentication is delegated to the SSO provider.
* CleverTap does not generate or store passwords for SSO users.
* Only admin-level users may appear in the `invitedBy` field.

## When to Use This Flow

* SSO manages organization-wide login.
* The IDP is the single source of truth for identity and attributes.

# Direct API Requests (Non-IDP Mode)

SCIM can operate without an IDP by calling CleverTap SCIM endpoints directly. This mode works for teams that manage provisioning through internal scripts or automation instead of an external IDP.

Key characteristics:

* The token must be generated without the IDP flag.
* The endpoint must be `/scim/v2/users`.
* Requests must follow the required SCIM-like structure.
* This mode is suitable for internal automation or custom provisioning tools.

# Payload Requirements for IDP Provisioning

A valid IDP-originated request uses the following structure:

```
{
  "userName": "<email>",
  "name": {
    "givenName": "<firstName>",
    "familyName": "<lastName>"
  },
  "active": true,
  "accounts": [
    {
      "accountId": "<encodedAccountId>",
      "teams": "TeamA,TeamB",
      "roles": "roleA,roleB",
      "status": "active"
    }
  ],
  "invitedBy": "<adminEmail>"
}
```

## Validation Behavior

* Missing fields return explicit errors, such as “username is empty or null”.
* Invalid teams or roles return validation messages.
* Status must be `active`, `revoke`, or `delete`.
* At least one `accounts[]` entry must have `status: active`.
* Account hierarchy is enforced.
* A non-admin in `invitedBy` results in a permission error.

SCIM provisioning does not send an invite email. Users complete authentication based on the organization’s identity configuration.

## Password Handling

* If using Auth0, CleverTap creates a random password internally.
* Users must use the “Forgot Password” flow to set their password.
* CleverTap does not expose the generated password.

# Troubleshooting

The following issues may occur during IDP-based provisioning.

## Provisioning Errors

* Invalid role or team
* Unsupported or incorrect account ID
* Missing mandatory fields
* Non-admin in `invitedBy`
* Invalid status value

## Authentication Issues

* Token missing in the request
* Token expired or regenerated without updating the IDP

## User Not Appearing in Dashboard

* Required attributes missing from the payload
* Status not set to `active` at creation
* Account hierarchy mismatch

# Best Practices for IDP Integration

* Use a dedicated SCIM token for IDP provisioning.
* Update the token in the IDP only when regenerated.
* Ensure `invitedBy` always references an admin user.
* Validate roles and teams in the CleverTap dashboard before mapping them in the IDP.
* Test provisioning with a non-production account first.
