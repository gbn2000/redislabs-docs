---
Title: Create roles
linkTitle: Create roles
description: Create access control roles.
weight: 20
alwaysopen: false
categories: ["RS"]
aliases: ["/rs/security/access-control/create-roles/"]
---

From **access control** > **roles**, you can configure user roles with:

- [**Management roles**](#default-management-roles) - Management roles define user access to the cluster's admin console and API.
- **Data access controls** - Data access controls define the permissions each role has for each database in the cluster.

## Default management roles

Redis Enterprise Software includes five predefined roles that determine a user's level of access to the admin console and [REST API]({{<relref "/rs/references/rest-api">}}).

1. **None** - Cannot access the admin console or use the REST API
1. **DB Viewer** - Read database settings
1. **DB Member** - Administer databases
1. **Cluster Viewer** - Read cluster settings
1. **Cluster Member** - Administer the cluster
1. **Admin** - Full cluster access

For more details about the privileges granted by each of these roles, see [admin console permissions]({{<relref "/rs/security/access-control/admin-console-access#admin-console-permissions">}}) or [REST API permissions]({{<relref "/rs/references/rest-api/permissions">}}).

## Create roles for database access {#create-db-role}

To create a role that grants database access to users but blocks access to the Redis Enterprise admin console and REST API, set the **Cluster management role** to **None**.

To define a role for database access:

1. From **access control** > **roles**, you can either:

    - Point to a role and select ![Edit](/images/rc/icon_edit.png#no-click "Edit") to edit an existing role.

    - Select ![Add](/images/rs/icon_add.png#no-click "Add") to create a new role.

1. Enter a descriptive name for the role. This will be used to reference the role when configuring users.

1. Select a **Cluster management role**. The default is **None**.

1. Select **Add** under **Redis ACLs** ![Add](/images/rs/icon_add.png#no-click "Add").

1. Select the databases the role applies to.

1. Select the Redis ACL to apply to the role.

1. Select the save icon.

1. Select **Save**.

{{< video "/images/rs/new-redis-role.mp4" "Create a new Redis Role" >}}

## Next steps

- [Assign the role to a user]({{<relref "/rs/security/access-control/rbac/assign-user-role">}}).