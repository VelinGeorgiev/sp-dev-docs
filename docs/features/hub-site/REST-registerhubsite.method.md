---
title: RegisterHubSite REST method
description: RegisterHubSite REST method
ms.date: 2/26/2018
---

# RegisterHubSite

> [!IMPORTANT]
> The hub sites feature is currently in preview and is subject to change. It is not currently supported for use in production environments.

Registers an existing site as a hub site.

## HTTP request

```
POST /_api/site/RegisterHubSite
```

## URI Parameters

None

## Request headers

| Header | Value |
|--------|-------|
|Accept|application/json;odata=verbose|
|Content-Type|application/json;odata=verbose;charset=utf-8|
|x-requestdigest|The appropriate digest for current site|

## Request body

Do not supply a request body for this method.

## Responses

| Name   | Type  | Description|
|--------|-------|------------|
|200 OK|SPHubSite |OK|
|Other Status Codes|Error|Error response describing why the operation failed.|

## Examples

### Register a marketing site as a hub site

#### Sample Request

```HTTP
POST
https://contoso.sharepoint.com/sites/marketing/_api/site/RegisterHubSite
```

#### Sample Response
**Status code:** 200

```JSON
{
	"@odata.context": "https://contoso.sharepoint.com/sites/marketing/_api/$metadata#hubsites/$entity",
	"@odata.type": "#SP.HubSite",
	"@odata.id": "https://contoso.sharepoint.com/sites/marketing/_api/site/RegisterHubSite",
	"@odata.etag": "\"1\"",
	"@odata.editLink": "site/RegisterHubSite",
	"Description": null,
	"ID": "2714709b-b5d0-4001-9d43-6a0e4d6e7a19",
	"LogoUrl": null,
	"SiteId": "2714709b-b5d0-4001-9d43-6a0e4d6e7a19",
	"SiteUrl": "https://contoso.sharepoint.com/sites/marketing",
	"Targets": null,
	"TenantInstanceId": "4aa2157b-4935-472d-8169-281c2e9d50a1",
	"Title": "Marketing site"
}
```