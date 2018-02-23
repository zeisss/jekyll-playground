---
title: "deploy"
layout: "page"
---

> Deploys code. Into folders. From artifacts. Like Crazy. So much wow.

**Deploy** is a service to deploy static or php websites.

## Features

* Supports different target sites
* Sites can have a different setup
* Sites can optionally include a separate configuration tarball
* Installation into sibling folder and moving in place for atomic updates via symlink rename (simple blue/green)

## Limitations

* Currently only supports deployments from [fs](/fs/)
* Currently only supports tar.gz artifacts
* Sites for deployment must be predefined by an admin

## Endpoint

The API endpoint is at `https://apps.moinz.de/deployer/deploy.php`. A valid `bearer` authorization header is required. 

## Usage

After installing, have your deployment script publish your artifact as a tarball to [fs](fs.html) and then perform a `POST` request to `deploy.php` with a `site` and `desired_version` parameter.

```
curl -XPOST https://apps.moinz.de/deployer/deploy.php \
	-d site=help.moinz.de \
	-d desired_version=master-12314556789123
```