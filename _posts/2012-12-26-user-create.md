---
category: User
path: '/api/users'
title: 'Post a User'
type: 'POST'

layout: nil
---

This method allows users to create a new thing.

### Request

* The headers must .
* **The body can't be empty** and must include at least the name attribute, a `string` that will be used as the name of the thing.

```Authentication: bearer TOKEN```
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
