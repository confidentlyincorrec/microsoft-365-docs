---
title: Get exposure score
description: Retrieves the organizational exposure score.
ms.service: defender-endpoint
author: siosulli
ms.author: siosulli
ms.localizationpriority: medium
manager: deniseb
audience: ITPro
ms.collection: 
- m365-security
- tier3
- must-keep
ms.topic: reference
ms.subservice: reference
ms.custom: api
search.appverid: met150
ms.date: 04/17/2024
---

# Get exposure score

[!INCLUDE [Microsoft Defender XDR rebranding](../../../includes/microsoft-defender.md)]

**Applies to:**

- [Microsoft Defender for Endpoint Plan 1](https://go.microsoft.com/fwlink/?linkid=2154037)
- [Microsoft Defender for Endpoint Plan 2](https://go.microsoft.com/fwlink/?linkid=2154037)
- [Microsoft Defender XDR](https://go.microsoft.com/fwlink/?linkid=2118804)

> Want to experience Microsoft Defender for Endpoint? [Sign up for a free trial.](https://signup.microsoft.com/create-account/signup?products=7f379fee-c4f9-4278-b0a1-e4c8c2fcdf7e&ru=https://aka.ms/MDEp2OpenTrial?ocid=docs-wdatp-exposedapis-abovefoldlink)

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../../includes/improve-request-performance.md)]

[!include[Prerelease information](../../../includes/prerelease.md)]

Retrieves the organizational exposure score.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md)

Permission type|Permission|Permission display name
---|---|---
Application|Score.Read.All|'Read Threat and Vulnerability Management score'
Delegated (work or school account)|Score.Read|'Read Threat and Vulnerability Management score'

## HTTP request

```http
GET /api/exposureScore
```

## Request headers

Name|Type|Description
---|---|---
Authorization|String|Bearer {token}. **Required**.

## Request body

Empty

## Response

If successful, this method returns 200 OK, with the exposure data in the response body.

## Example

### Request

Here is an example of the request.

```http
GET https://api.security.microsoft.com/api/exposureScore
```

### Response

Here is an example of the response.

> [!NOTE]
> The response list shown here may be truncated for brevity.

```json
{
    "@odata.context": "https://api.security.microsoft.com/api/$metadata#ExposureScore/$entity",
    "time": "2019-12-03T07:23:53.280499Z",
    "score": 33.491554051195706
}
```

## See also

- [Microsoft Defender Vulnerability Management](/microsoft-365/security/defender-endpoint/next-gen-threat-and-vuln-mgt)
- [Defender Vulnerability Management exposure score](/microsoft-365/security/defender-endpoint/tvm-exposure-score)
[!INCLUDE [Microsoft Defender for Endpoint Tech Community](../../../includes/defender-mde-techcommunity.md)]
