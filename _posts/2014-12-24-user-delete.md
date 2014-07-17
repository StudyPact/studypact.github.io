---
category: User
path: '/api/users/me'
title: 'Delete a User'
type: 'DELETE'

layout: nil
---

This method allows the user to delete himself. Alternatively call DELETE on **`/api/users/:id`**

### Request

* **`:id`** is the id the user to delete. (optional)
* The headers must include a **valid authentication token**.
* **The body is omitted**.

```Authentication: bearer h0ajDmWeN6fULyNpjKO9cTAtijZ8pNh1AWz6IZ9jLKXDjfGF4vzAN92cMs7xazIw```

### Response

```Status: 204 Deleted```

For errors responses, see the [response status codes documentation](#response-status-codes).