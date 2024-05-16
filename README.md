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

{Pricing Tier} = free, s1, p1 etc. Used when there can be only one resource of certain pricing tier. This replaces environment, because freetier might be used in production also.

|Resource Type|Prefix|Name|
|---|---|---|
|Application Insights|ai-|{Customer}-ai-{App Name}-{Environment}|
|App Service (Web App)|app|{Customer}-app-{App Name}-{Environment}-{###}|
|App Service plan|plan-|{Customer}-plan-{App Name}-{Environment}|
|Azure Cognitive Search|srch-|{Customer}-srch-{App Name}-{Environment}|
|Azure SQL Database server|sql-|{Customer}-sql-{App Name}-{Environment}|
|Azure SQL database|sqldb-|{Customer}-sqldb-{Database Name}-{Environment}|
|Backup Vault|bvault-|{Customer}-bvault-{Environment}|
|Cosmos DB database|cosmos-|{Customer}-cosmos-{App Name}-{Environment}|
|Custom vision|cvision-|{customer}-cvision-{Pricing Tier}|
|Function app|func-|{Customer}-func-{App Name}-{Environment}|
|Event hub|evh-|{Customer}-evh-{App Name}-{Environment}|
|Logic Apps|logic-|{Customer}-logic-{App Name}-{Environment}|
|Open AI|openai-|{Customer}-openai-{App Name}-{Environment}|
|Recovery Services Vault|rsvault|{Customer}rsvault{Region}{Environment}|
|Resource group|rg-|{Customer}-rg-{App Name}-{Environment}|
|Service Bus|sb-|{Customer}-sb-{App Name}-{Environment}|
|Service Bus Namespace|sbns-|{Customer}-sbns-{App Name}-{Environment}|
|Service Bus queue|sbq-|sbq-{query descriptor}|
|Service Bus topic|sbt-|sbt-{query descriptor}|
|Storage account (general use)|st-|{Customer}st{storage name}{###}|
|Virtual Machine|vm|{Customer}vm{App Name}{###}|
|Virtual network|vnet|{Customer}-vnet-{App Name}-{Environment}|

## Fabric Naming Conventions
In Fabric the naming convention is driven by the size of the Fabric instance. In large instances we might want to specify role of the user (data engineer, data analyst etc.), but 
in minor instances we don't need to add it.

Recommended naming convention is {resource type}_{layer}_{usage}.
For example if we had to create a Lakehouse for raw financial data, we could call it
LH_RAW_Financial

Resource type and layer all all caps and usage/name of the component is as capitalized word.

## Common resources
|Resource Type|Prefix|
|---|---|
|Dataset|DS|
|Dataflow|DFL|
|Datamart|DM|
|Pipeline|PL|
|Dataflow|DFL|
|Lakehouse|LH|
|Notebook|NB|
|Spark Job Definition|SJ|
|Model|MDL|
|Experiment|EXP|
|Warehouse|WH|
|Database|DB|
|Queryset|QS|
|Eventstream|ES|

## Data layers
|Layer|Prefix|
|---|---|
|Raw/unmodified data|RAW|
|Modified/ready for BI usage in small instances|SILVER|
|Ready for BI usage in large instances|GOLD|


