---
layout: page
title: "fs"
tagline: "Simple file storage"
---

# fs

FS is a simple file storage with simple rest api.

## Access

Endpoint: `https://apps.moinz.de/fs/fs.php`. See the [API](/fs/api.html) page for details.

## Authorization

Access to paths can be finely tuned by an admin (TBD: provide an iam api). Policies can control access to various resources based on username, action and paths.

The [authorization guide](https://github.com/zeisss/fs-php/blob/master/Docs/Configuration.md#policies) documents the Policy concept.

## Clients

* [fs.bash](https://raw.githubusercontent.com/zeisss/fs-php/master/fs.bash) - Small bash wrapper around curl.