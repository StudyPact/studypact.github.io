---
category: User
path: '/api/users'
title: 'Post a User'
type: 'POST'

layout: nil
---

This method allows users to create a new User.

### Request

* The headers must .
* **The body can't be empty** and must include at least a password and the email attribute.
* **no authentication token required**.

```{
    email: 'toby@studypact.com',
    password: 'secret password'
}```

### Response

**If succeeds**, returns the created User.

```Status: 201 Created```
```{
    id: $ID,
    email: 'toby@studypact.com',
    ...
}```

For errors responses, see the [response status codes documentation](#response-status-codes).
