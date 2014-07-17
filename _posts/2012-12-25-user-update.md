---
category: User
path: '/api/users/me'
title: 'Update a User'
type: 'PUT'

layout: nil
---

This method allows the user to update his data. Alternatively call PUT on **`/api/users/:id`**

### Request

* **`:id`** is the id the user to update. (optional)
* The headers must include a **valid authentication token**.
* **Not every field on the user can be updated**. 

```Authentication: bearer h0ajDmWeN6fULyNpjKO9cTAtijZ8pNh1AWz6IZ9jLKXDjfGF4vzAN92cMs7xazIw```
```{
  email: "$EMAIL",
  paypal_email: "$EMAIL", 
  password: "$PASS,
  holiday: false,
  payout_request: false,
  pact_duration: 120, //minutes
  pact_stakes: 5, //full dollar
  language: "en_US",
  timezone: "UTC",
  displayname: {
    first: String,
    last: String
  },
  payment_status: ["GOOD_PAYMENT", "BAD_PAYMENT", "NO_PAYMENT"] //default: NO_PAYMENT
}```

### Response

Sends back the updated user.

```Status: 200 OK```
```{
  "_id": “$ID”,
  "created": ISODate("2014-02-09T15:21:05.072Z"),
  "email": "$EMAIL",
  "paypal_email": "$EMAIL", 
  "password": “$PASS,
  "scope": ["user"],
  "holiday": false,
  "has_payment": false, //indicates if a valid payment option exists for the user
  “verified_email”: true/false
  "payout_request": false,
  "current_earnings": 0,
  "current_bonus": 0, //earned via referrals,
  “referrer_code”: //each user has a referral code to invite friends
  “invitation_code”: //only exists if a user was invited
  “successful_referral_count”:0, //how many referrals finished 1 pact
  “paid_referral_count”: 0, // how many referrals are already paid to the user
  “pact_duration”: 120, //minutes
  “pact_stakes”: 5, //full dollar
  "totals": {
    "money": 0,
    "time": 0
  },
  "language": "en_US",
  "timezone": "UTC",
  "picture": {
    "normal": "/images/head.png",
    "small": "/images/head.png"
  },
  displayname: {
    first: String,
    last: String
  },
  payment_status: [“GOOD_PAYMENT”, "BAD_PAYMENT", "NO_PAYMENT"] //default: NO_PAYMENT
}```

For errors responses, see the [response status codes documentation](#response-status-codes).