---
title: Copy
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
# Overview

The Nested Objects feature allows storing and using structured JSON data inside user profiles. You can directly represent complex business entities, such as insurance policies, subscriptions, and user shopping cart details, under user properties in CleverTap without flattening the data.

> 📘 Private Beta
> 
> This feature is currently available in Private Beta for selected customers. To enable Nested Objects, contact your Customer Success Manager or raise a support ticket.

## Advantages of Nested Objects

You achieve the following benefits when you use nested objects in your CleverTap account:

**Model complex entities naturally:** Store data in its original structured format. _For example, store an insurance policy with its beneficiaries without creating multiple flat keys._

**Target users more granularly:** Segment audiences based on nested user properties. _For example, find users whose subscription plans have expired._

**Reduce engineering effort:** Send structured JSON payloads through the API without transformation logic. _For example, send order details directly without flattening each field._

### Use Cases

Businesses across industries benefit from this feature:

**Insurance:** Notify customers when a policy beneficiary has no email address.  
**E-commerce:** Offer discounts to users with a cart that includes at least one product in the _Shoes_ category.  
**Telecom:** Remind subscribers about broadband or postpaid plan renewals using plan metadata.  
**Fintech:** Trigger campaigns when a child account linked to a parent account reaches a savings milestone.  
**Media & Entertainment:** Personalize engagement based on nested content metadata such as show ID or genre.

### Manage Nested Objects Across Platforms

You can view and manage nested objects in the same areas where you use standard profile and event properties:

**Profile Page:** View structured objects stored against a user's profile.  
**Segmentation Builder:** Create conditions using nested attributes. _For example, identify policies with missing beneficiary details._

### **Example JSON Structures**

You send nested objects as JSON payloads. The following examples show how to structure nested objects in profiles and events.

**User Profile**

The following sample payload shows Nested Objects in a user profile:

```json
{
  "Name": "Jane Doe",
  "Policies": [
    {
      "PolicyID": "POL123",
      "Type": "Health",
      "PremiumAmount": 1200,
      "Beneficiaries": [
        {
          "Name": "John Doe",
          "Email": "john@example.com"
        }
      ]
    },
    {
      "PolicyID": "POL456",
      "Type": "Life",
      "PremiumAmount": 800,
      "Beneficiaries": []
    }
  ]
}
```

## Enable Nested Objects

To enable and use Nested Objects in your account, follow these steps:

1. **Send Structured Data** – Use REST API payloads to send JSON with nested fields.
2. **Define Schema** –  Open **Settings > Schema** to define field types, including arrays and objects.
3. **Build Segments** – Go to the Segmentation Builder and create filters using nested user attributes.  
   For example: _InsuranceDetails.Policies.Beneficiaries.DOB._

   The Segmentation Builder in the image shows how nested fields appear within profile data, helping you select properties such as beneficiary date of birth when creating filters.

   [block:image]{"images":[{"image":["https://files.readme.io/582aab7c426cfb8a3e87cfc84b5acbd40cfd92dec8168e7db96fbe2414465bee-image.png",null,"Nested Objects in Segment Builder"],"align":"center","border":true,"caption":"Nested Objects in Segment Builder"}]}[/block]

> 📘 Segmentation Limitations with Nested Properties
> 
> You may encounter an error showing _ Nested user property queries aren’t supported yet. Choose a segment without nested properties to proceed_. Select a segment or filter that uses standard (non-nested) user attributes to continue. This occurs when segmentation workflows (such as campaign targeting) do not support querying nested user properties.

### Best Practices

Use the following practices to maintain data quality and prevent ingestion issues:

- Keep schema definitions consistent across all integrations.
- Send only valid objects; CleverTap drops null or empty objects automatically.
- Monitor object size and array length to avoid exceeding system limits.
- Start with a test schema and validate it before rolling out to production accounts.
- Use clear and concise attribute names for easier targeting and reporting.

Also, review the following areas to troubleshoot issues:

- **Schema Mismatch:** Verify that the schema matches your payload in **Settings > Schema**.
- **Oversized Payload:** Reduce nesting, limit array size, or split data across events.
- **Dropped Fields:** Check if the number of keys or nesting depth exceeds supported limits.
- **Slow Queries:** Simplify filters and reduce nested field conditions for faster segmentation.

### Limitations

CleverTap enforces limits to ensure performance and stability when you use nested objects.

| Limit Type                   | Maximum Value                             |
| ---------------------------- | ----------------------------------------- |
| Nesting depth                | 3 levels                                  |
| Payload size                 | 128 KB per profile or event               |
| Object or array keys at root | 5                                         |
| Reserved fields              | `identity`, `email`, and `ts` remain flat |

When you exceed a limit, CleverTap processes your data by dropping extra elements or raising an error.

# FAQs

### Can I use nested objects in SDK, CSV, or SFTP uploads?

No. Nested objects are supported only through the REST API.

### What happens if I exceed the payload size or nesting limits?

CleverTap automatically drops extra elements or converts invalid data into strings. Errors appear in the error stream for review.

### Can I query deeply nested fields in segmentation?

Yes, you can query up to three levels.

### Are nested objects included in exports?

No, nested objects are not exported through API-based data exports.

### Do reserved system fields support nesting?

No. Fields such as `identity`, `email`, and `ts` remain flat for consistency and stability.

### Does this feature impact performance?

Nested Objects feature does not affect overall system performance when you stay within limits. However, queries with multiple nested conditions may take longer to process.