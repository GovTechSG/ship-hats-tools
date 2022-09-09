# Provision Purple Hats

## Prerequisites

Ensure the following requirements are met:
- **Node.js version to be version 15.10.0 and above.**
- If you do not have node, or if there is a need to manage your node versions, you can consider using [Node Version Manager (NVM)](https://github.com/nvm-sh/nvm).
- Make sure NVM is pointing to a node version >= 15.10.0. Refer to [Node Version Manager (NVM)](#node-version-manager-(NVM))
- Install the required NPM packages with `npm install`.

### Node Version Manager (NVM)
```shell
# If have not installed a version >= v15, install NodeJs version with NVM
nvm install <nodejs_version_greater_than_15>

# For subsequent use, you will need to run the command below as time you open a new terminal
nvm use <nodejs_version_greater_than_15>
```

## Provision

### To provision Purple Hats, onboard and dedicate HATS Linux Elastic Agent

- **Existing user:** If you have onboarded SHIP-HATS previously, you would have a dedicated Linux elastic agent to perform the security scans with Fortify and/or SonarQube. You can use the same Linux agent for Purple HATS scan as well.

- **New user:** If you are a new user, raise a [HATS service request](https://go.gov.sg/hats-ssd) or [raise a service request](https://jira.ship.gov.sg/servicedesk/customer/portal/11/group/57) to request for dedicated elastic agent. Include information on Bamboo build project/build plan for your project.

## Local Installation
If users have not subscribed with us, following technology stack is required to run Purple Hats:
- [Apify SDK](https://sdk.apify.com/)
- [Axe-core](https://github.com/dequelabs/axe-core)
- [Node.js](https://Node.js.org/en/)

<!--
You can provision GitLab by:
- [Adding GitLab tool to a project](https://docs.developer.tech.gov.sg/docs/ship-hats-portal/#/manage-tools)  
  -or-
- [Adding project tool with customised project key](https://docs.developer.tech.gov.sg/docs/ship-hats-portal/#/manage-tools?id=create-project-tool-with-customised-project-key)

-->