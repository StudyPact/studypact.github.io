---
category: StudyApps
path: '/api/studyapps'
title: 'Get Studyapps'
type: 'GET'

layout: nil
---

This method retrieves all studyapps.

### Request

* **no authentication token required**.

### Response

Sends back a collection of studyapps.

```Status: 200 OK```
```{
      {
    "_id": "52fa23b18b479837a70001b0",
    "flags": {
      "promoted": true
    },
    "android_app_url": "com.ichi2.anki",
    "picture_url": "https://lh6.ggpht.com/F7sTnXdaaU5fpLvcAuX1X1JyjVgyLgInjKVUnisUeYvzLHsR_xX50gEi0Jn3AXb1wuc=w300-rw",
    "description": "Awesome Flashcard App",
    "name": "Anki",
    "created": "2014-07-16T07:16:23.251Z"
  },
  ...
}```

For errors responses, see the [response status codes documentation](#response-status-codes).