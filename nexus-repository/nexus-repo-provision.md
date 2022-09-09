# Provision Nexus repo

### To provision or create Nexus repo

1. Raise a [service request](https://jira.ship.gov.sg/servicedesk/customer/portal/11/create/152).

1. Provide information in the following fields:

    |Field|Description|
    |---|---|
    **Summary**|Provide the issue title
    **Description**|Provide description for the nexus repository
    **Nexus Repository Type**|Select the type of repository required for your team
    **Nexus Repository Name**|Select a unique name for your repository
    **Nexus Repository Users and Permissions (only 3 users)**|Provide a list of users or groups that require access to the project, along with the required permissions. Use the following template to indicate the list of users or groups and permissions for nexus repository: <br> **upload permission for:** - group-one - group-two - user-one <br>**read permission for:** - group-three - group-two - user-four <br>**delete permission for:** - group-one - group-two - user-five - user-six<br> **admin permission for:** - group-seven - user-five - user-six 
    **Nexus Repository Group (optional)**|If you are creating a repository group, provide the existing repository name
    **Nexus Proxy Remote Storage URL (optional)**|If you are creating a repository proxy, provide the remote storage url
    **Project Name**|Provide a name for your project
    **Project Owner Name**|Provide the name of  project owner
    **Reporting Agency**|Provide the name of your agency
1. Click **Create**.