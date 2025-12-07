---
title: Data Types Supported for Events
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
@DOCS: SINCE THIS IS TOO SHORT OF A HACKATHON DOC, SUNIL WILL CONFIRM WHICH (DEV) DOC TO MOVE THIS TO.
[block:api-header]
{
  "title": "Overview"
}
[/block]
CleverTap only supports primitive Java data types, including:
  * String
  * Integer
  * Float
  * Boolean
  * Mixed

You can use a list or an array only with the Charged event. All others will return an incorrect data type if using a list or an array.