This document contains Azure Naming Conventions used by [Adafy](https://adafy.com).

## Guidelines

We use Microsoft's [recommended naming conventions](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/naming-and-tagging).

Some of the resources have special naming conventions. Always check the guideline before applying name.

## Resource Naming Pattern

{customer}-{resource type}-{app name}-{environment}

Here are some examples:

#### App service

contoso-app-portal-test

#### SQL database

contoso-sqldb-users-prod

#### Virtual network naming

contoso-vnet-prod-westeu-001

## Resource Tagging

The following tagging patterns are used:

### GDPR

Resources that contains GDPR related customer data, must be marked with gdpr tag.

Example: Key: GDPR, Value: GDPR/True

### Owner

User who created (or owns) the resource, must be marked with Owner tag with the value of email address.​

Example: Key: Owner, Value: xxx.yyy@adafy.com
