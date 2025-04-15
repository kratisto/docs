---
title: User creation
excerpt: This guide shows you how to create a new user
updated: 2025-04-16
---

## Using web interface

> [!primary]
>
> Using web interface is the easiest way to create a user.
>

First, log into your [OVHcloud customer area](/links/manager) and go to the [Bare Metal Cloud](https://www.ovh.com/manager/#/dedicated/configuration){.external} section at the top. Once on the page, click on the `Platforms and services`{.action} heading and then on the `ceph-cluster`{.action} service.

![Ceph users](images/create_a_user_1.png){.thumbnail}

Enter a username.

> [!warning]
>
> Your username needs at least three characters.
>

![Ceph user creation](images/create_a_user_2.png){.thumbnail}

Once the user has been created, you're returned to the manager, and the user has been created.

![Ceph user creation](images/create_a_user_3.png){.thumbnail}

## Using API

You can create a user using this API route:

> [!api]
>
> @api {v1} /dedicated/ceph POST /dedicated/ceph/{serviceName}/user
>

serviceName is the fsid of your cluster.

You can also check user creation by creating a list of users.

```bash
GET /dedicated/ceph/98d166d8-7c88-47b7-9cb6-63acd5a59c15/user
[
  {
    mdsCaps: ""
    monCaps: "allow r"
    serviceName: "98d166d8-7c88-47b7-9cb6-63acd5a59c15"
    name: "myuser"
    osdCaps: "allow class-read object_prefix rbd_children"
    key: "AQA9KpdXoBrDNhAAFCM7m/XOtmWh3LMSNlHVqw=="
  }
]
```

## Go further

Visit our dedicated Discord channel: <https://discord.gg/ovhcloud>. Ask questions, provide feedback and interact directly with the team that builds our Storage and Backup services.

If you need training or technical assistance to implement our solutions, contact your sales representative or click on [this link](https://www.ovhcloud.com/en-gb/professional-services/) to get a quote and ask our Professional Services experts for assisting you on your specific use case of your project.

Join our community of users on <https://community.ovh.com/en/>.
