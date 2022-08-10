This document contains Azure Naming Conventions used by [Adafy](https://adafy.com).

## Guidelines

We use Microsoft's [recommended naming conventions](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/naming-and-tagging).

Some of the resources have special naming conventions. Always check the guideline before applying name.

## Resource Naming Pattern

{customer}-{resource type}-{app name}-{environment}

For resources that does not support hyphens in names, just leave the hyphens out.

Here are some examples:

#### App service

contoso-app-portal-test

#### SQL database

contoso-sqldb-users-prod

#### Virtual network naming

contoso-vnet-app-prod
contoso-vnet-portal-test

## Resource Tagging

The following tagging patterns are used:

### GDPR

Resources that contains GDPR related customer data, must be marked with gdpr tag.

Example: Key: GDPR, Value: GDPR/True

### Owner

User who created (or owns) the resource, must be marked with Owner tag with the value of email address.​

Example: Key: Owner, Value: xxx.yyy@adafy.com

## Common resources

Following table contains most common resources, their prefixes and examples.
{###} = number starting from 001.

{Customer} = customer short name without spaces. For example contoso.

{App Name} = Application/project name without spaces.

{Environment} = dev,test,qa,stage or prod.

{Region} = wus (west us), eus2 (east us2), we (west europe), ugov (usgovia)

|Resource Type|Prefix|Name|
|---|---|---|
|App Service (Web App)|app|{Customer}-app-{App Name}-{Environment}-{###}|
|App Service plan|plan-|{Customer}-plan-{App Name}-{Environment}|
|Azure Cognitive Search|srch-|{Customer}-srch-{App Name}-{Environment}|
|Azure SQL Database server|sql-|{Customer}-sql-{App Name}-{Environment}|
|Azure SQL database|sqldb-|{Customer}-sqldb-{Database Name}-{Environment}|
|Backup Vault|bvault-|{Customer}-bvault-{Environment}|
|Cosmos DB database|cosmos-|{Customer}-cosmos-{App Name}-{Environment}|
|Function app|func-|{Customer}-func-{App Name}-{Environment}|
|Event hub|evh-|{Customer}-evh-{App Name}-{Environment}|
|Recovery Services Vault|rsvault|{Customer}rsvault{Region}{Environment}|
|Resource group|rg-|{Customer}-rg-{App Name}-{Environment}|
|Service Bus|sb-|{Customer}-sb-{App Name}-{Environment}|
|Service Bus Namespace|sbns-|{Customer}-sbns-{App Name}-{Environment}|
|Service Bus queue|sbq-|sbq-{query descriptor}|
|Service Bus topic|sbt-|sbt-{query descriptor}|
|Storage account (general use)|st-|{Customer}st{storage name}{###}|
|Virtual Machine|vm|{Customer}vm{App Name}{###}|
|Virtual network|vnet|{Customer}-vnet-{App Name}-{Environment}|
