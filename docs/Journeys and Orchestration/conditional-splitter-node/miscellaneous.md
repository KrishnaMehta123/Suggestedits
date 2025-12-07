---
title: Miscellaneous
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
## IntelliNODE

The Conditional Split Node cannot be connected directly after an IntelliNode. For example, a product marketer sets up an A/B test using an IntelliNODE to test different onboarding messages. They then try to insert a Conditional Splitter Node after the IntelliNODE to route users based on their subscription plan. CleverTap shows an error message that the Conditional Split must be placed before the IntelliNODE. IntelliNODES are used for experimentation, that is, they randomly split users into different variants to measure performance. Allowing further logical branching (such as Conditional Split) immediately afterward would make attribution ambiguous. Therefore, path-based logic such as Conditional Splits must be defined before users reach the IntelliNODE.

If personalization is required based on user properties (for example, `plan_type` or `region`), the correct approach is:

* Use the Splitter to divide users based on logic (for example, Premium vs. Free)
* Attach separate IntelliNODES for each branch, if experimentation is still needed within those segments

(@Amrita to add graphics here)

## Error Scenarios

* Conditional Splitter nodes will reset to an ideal state (that is, lose all path logic) in the following cases:
  * Event Change: If the event in the connected Action node is changed after the Splitter was configured, all event-property-based logic is invalidated.
  * Delay > 24 Hours: If an Action node delay is updated to more than 24 hours and the Conditional Split node uses event properties or Advanced filters, it resets.
* If the node preceding the Conditional Split node is deleted, the conditional split node resets to its default state and must be reconfigured.
* If a non-supported data type (such as array, number, and so on) is selected, the system throws a validation error.
