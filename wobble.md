---
title: "wobble"
tagline: "Google Wave at home"
layout: page
---

Wobble is a Google Wave look-a-like based with a JSON-RPC protocol.

## Signup

User registration is open at [wobble.moinz.de](https://wobble.moinz.de).

## API Endpoint

The JSON-RPC endpoint is reachable at `https://wobble.moinz.de/api/endpoint.php`:

```
$ curl https://wobble.moinz.de/api/endpoint.php -d '{"jsonrpc":"2.0", "id": 1, "method": "system.listMethods", "params":["foo"]}' | jq .
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   658    0   582  100    76   3967    518 --:--:-- --:--:-- --:--:--  3986
{
  "jsonrpc": "2.0",
  "result": [
    "system.listMethods",
    "echo",
    "wobble.api_version",
    "user_register",
    "user_get",
    "user_get_id",
    "user_change_name",
    "user_change_password",
    "user_login",
    "user_signout",
    "topics_list",
    "topics_search",
    "topics_create",
    "topic_get_details",
    "topic_add_user",
    "topic_remove_user",
    "topic_set_archived",
    "topic_remove_message",
    "topic_change_read",
    "post_create",
    "post_edit",
    "post_delete",
    "post_change_read",
    "post_change_lock",
    "get_notifications",
    "contacts.list",
    "contacts.add",
    "contacts.remove",
    "user_get_contacts",
    "user_add_contact",
    "user_remove_contact",
    "post_read"
  ],
  "id": 1
}
```

