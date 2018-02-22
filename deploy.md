---
title: "deploy"
layout: "page"
---

Deploys code. Into folders. From artifacts. Like Crazy. So much wow.

_Deployer_ is a service to deploy artifacts from a local fs-php repository. It currently only supports extracting tarballs at the moment

## Features

* Supports different target sites
* Sites can have a different setup
* Sites can optionally include a separate configuration tarball
* Installation into sibling folder and moving in place for atomic updates via symlink rename (simple blue/green)

## Usage

After installing, have your deployment script publish your artifact as a tarball to [fs](fs.html) and then perform a `POST` request to `deploy.php` with a `site` and `desired_version` parameter.