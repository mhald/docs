+++
date = "2016-07-03T04:02:20Z"
title = "Upgrading Replicated"
description = "The process for end customers to update Replicated services to access the latest improvements to the underlying system since their installation."
weight = "320"
categories = [ "Distributing" ]

[menu.main]
Name       = "Upgrading Replicated"
identifier = "upgrading-replicated"
parent     = "/distributing-an-application"
url        = "/docs/distributing-an-application/upgrading"
+++

{{< note title="Replicated 2.0" >}}
The content in this document is specific to updating an existing easy install script installed
Replicated instance. If you are looking for the
Replicated 1.2 version of this document it is available at
<a href="distributing-an-application/upgrading-1.2/">{{< baseurl >}}distributing-an-application/upgrading-1.2/</a>
{{< /note >}}

You can update all Replicated component versions to latest by re-running the installation
script.

```shell
curl -sSL https://get.replicated.com/docker | sudo bash
```

If you have additional nodes you will independently need to run the following on each of them.

```shell
curl -sSL https://get.replicated.com/operator | sudo bash
```

## Migrating from Replicated v1 to v2
Replicated provides a one line migration script to upgrade your v1 installation to v2. The script will first stop your app 
and backup all Replicated data in case there is a need for a restore. To invoke the migration script all you have to do 
is run the script below and follow the prompts.

```shell
curl -sSL https://get.replicated.com/migrate-v2 | sudo bash
```

{{< warning title="Warning" >}}
To prevent loss of data, backing up your server is highly recommended before performing a migration.
{{< /warning >}}
