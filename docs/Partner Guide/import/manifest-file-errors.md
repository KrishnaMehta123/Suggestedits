---
title: Manifest File Errors
excerpt: Understand manifest file upload errors.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
This section explains the error messages encountered during manifest file upload and their causes.

| Error Message                                                       | Error Cause                                                                                                                                   |
| :------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------- |
| Upload mapped file in a valid JSON format.                          | Indicates that there is an error with the JSON format.                                                                                        |
| Uploaded mapped file is empty. Check and reupload file.             | Indicates that the user has uploaded an empty file.                                                                                           |
| Columns don’t match. Check and reupload mapped file.                | Indicates there are multiple mismatches in the number of columns.                                                                             |
| Column names missing. Update column names and reupload mapped file. | Indicates that the names of the columns are missing. Ensure to add all columns in the manifest file. Otherwise, you cannot save that mapping. |
| Upload mapped files with the column {{Column Name}}                 | Indicates that one particular column is missing.                                                                                              |
| Check the column {{column name}} and reupload mapped file.          | Indicates a single-column name mismatch.                                                                                                      |