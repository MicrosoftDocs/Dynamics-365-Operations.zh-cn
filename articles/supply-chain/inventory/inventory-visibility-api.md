---
title: 库存可见性公共 API
description: 本主题介绍库存可见性提供的公共 API。
author: yufeihuang
ms.date: 12/09/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f74bb4bd4ed66520c04261bd9f82faad7775817e
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062103"
---
# <a name="inventory-visibility-public-apis"></a>库存可见性公共 API

[!include [banner](../includes/banner.md)]


本主题介绍库存可见性提供的公共 API。

库存可见性加载项的公共 REST API 为集成提供几个特定终结点。 它支持四种主要交互类型：

- 从外部系统发布对加载项的现有库存量更改
- 从外部系统设置或覆盖加载项中的现有库存数量
- 从外部系统将预留事件过帐到加载项
- 从外部系统查询当前的现有数量

下表列出了当前可用的 API：

| 路径 | 方法 | 说明 |
|---|---|---|
| /api/environment/{environmentId}/onhand | 过帐 | [创建一个现有库存更改事件](#create-one-onhand-change-event) |
| /api/environment/{environmentId}/onhand/bulk | 过帐 | [创建多个更改事件](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | 过帐 | [设置/覆盖现有库存数量](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | 过帐 | [创建一个预留事件](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | 过帐 | [创建多个预留事件](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/indexquery | 过帐 | [使用过帐方法查询](#query-with-post-method) |
| /api/environment/{environmentId}/onhand | 获取 | [使用获取方法查询](#query-with-get-method) |

Microsoft 提供了现成的 *Postman* 请求集合。 可以使用以下共享链接将此集合导入到 *Postman* 软件中：<https://www.getpostman.com/collections/90bd57f36a789e1f8d4c>。

> [!NOTE]
> 此路径的 {environmentId} 部分是 Microsoft Dynamics Lifecycle Services (LCS) 中的环境 ID。
> 
> 批量 API 最多可为每个请求返回 512 条记录。

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a>根据 Lifecycle Services 环境查找终结点

多个地理区域和多个区域中 Microsoft Azure Service Fabric 已部署了库存可见性微服务。 目前没有可将您的请求自动重定向到相应地理区域和区域的中央终结点。 因此，必须使用以下模式将信息段编排到 URL 中：

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

可以在 Microsoft Dynamics Lifecycle Services (LCS) 环境中找到区域短名称。 下表列出了当前可用的区域。

| Azure 区域        | 区域短名称 |
| ------------------- | ----------------- |
| 澳大利亚东部      | eau               |
| 澳大利亚东南部 | seau              |
| 加拿大中部      | cca               |
| 加拿大东部         | eca               |
| 欧洲北部        | neu               |
| 西欧         | weu               |
| 美国东部             | eus               |
| 美国西部             | wus               |
| 英国南部            | suk               |
| 英国西部             | wuk               |
| 日本东部          | ejp               |
| 日本西部          | wjp               |
| 巴西南部        | sbr               |
| 美国中南部    | scus              |

岛编号是 Service Fabric 中部署 LCS 环境的位置。 现在无法从用户端获取此信息。

Microsoft 已在 Power Apps 中内置了用户接口 (UI)，供您获取微服务的完整终结点。 有关详细信息，请参阅[查找服务终结点](inventory-visibility-configuration.md#get-service-endpoint)。

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>身份验证

平台安全令牌用于调用库存可见性公共 API。 因此，您必须使用Azure AD 应用程序生成 _Azure Active Directory (Azure AD) 令牌_。 然后，必须使用 Azure AD 令牌从安全服务获取 _访问令牌_。

Microsoft 提供了现成的 *Postman* 获取令牌集合。 可以使用以下共享链接将此集合导入到 *Postman* 软件中：<https://www.getpostman.com/collections/496645018f96b3f0455e>。

若要获取安全服务令牌，请执行以下步骤。

1. 登录 Azure 门户，然后将其用于查找 Dynamics 365 Supply Chain Management 应用的 `clientId` 和 `clientSecret` 值。
1. 通过提交具有以下属性的 HTTP 请求来获取 Azure AD 令牌 (`aadToken`)：

   - **URL：**`https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
   - **方法：**`GET`
   - **正文内容（窗体数据）：**

     | 键           | 值                                |
     | ------------- | ------------------------------------ |
     | client_id     | ${aadAppId}                          |
     | client_secret | ${aadAppSecret}                      |
     | grant_type    | client_credentials                   |
     | resource      | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |

   您应通过响应收到一个 Azure AD 令牌 (`aadToken`)。 标签应类似于以下示例。

   ```json
   {
       "token_type": "Bearer",
       "expires_in": "3599",
       "ext_expires_in": "3599",
       "expires_on": "1610466645",
       "not_before": "1610462745",
       "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
       "access_token": "eyJ0eX...8WQ"
   }
   ```

1. 创建一个如下示例的 JavaScript 对象表示法 (JSON) 请求。

   ```json
   {
       "grant_type": "client_credentials",
       "client_assertion_type": "aad_app",
       "client_assertion": "{Your_AADToken}",
       "scope": "https://inventoryservice.operations365.dynamics.com/.default",
       "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
       "context_type": "finops-env"
   }
   ```

   请注意以下点：

   - `client_assertion` 值必须是您在上一步中收到的 Azure AD 令牌 (`aadToken`)。
   - `context` 值必须是要在其中部署加载项的 LCS 环境 ID。
   - 如示例中所示设置所有其他值。

1. 通过提交具有以下属性的 HTTP 请求来获取访问令牌 (`access_token`)：

   - **URL：**`https://securityservice.operations365.dynamics.com/token`
   - **方法：**`POST`
   - **HTTP 标题：** 包含 API 版本。 （密钥为 `Api-Version`，值为 `1.0`。）
   - **正文内容：** 包括您在上一步中创建的 JSON 请求。

   您应通过响应收到一个访问令牌 (`access_token`)。 必须将此令牌用作持有者令牌来调用库存可见性 API。 下面是一个示例。

   ```json
   {
       "access_token": "{Returned_Token}",
       "token_type": "bearer",
       "expires_in": 3600
   }
   ```

> [!IMPORTANT]
> 当您使用 *Postman* 请求集合调用库存可见性公共 API 时，您必须为每个请求添加一个持有者令牌。 若要查找您的持有者令牌，请在请求 URL 下选择 **授权** 选项卡，选择 **持有者令牌** 类型，并复制最后一步中提取的访问令牌。 在本主题的后面章节中，`$access_token` 将用于表示上一步中提取的令牌。

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>创建现有库存更改事件

有两个 API 可用于创建现有库存更改事件：

- 创建一个记录：`/api/environment/{environmentId}/onhand`
- 创建多个记录：`/api/environment/{environmentId}/onhand/bulk`

下表汇总了 JSON 正文中各字段的含义。

| 字段 ID | 说明 |
|---|---|
| `id` | 特定更改事件的唯一 ID。 此 ID 用于确保如果在发布过程中与服务的通信失败，重新提交事件不会导致同一事件在系统中算作两次。 |
| `organizationId` | 链接到事件的组织的标识符。 此值将在 Supply Chain Management 中映射到组织或数据区域 ID。 |
| `productId` | 产品的标识符。 |
| `quantities` | 必须充当现有库存数量的更改量的数量。 例如，如果将 10 本新帐簿添加到货位，则此值将为 `quantities:{ shelf:{ received: 10 }}`。 如果从货位中移除或出售了三本帐簿，则此值将为 `quantities:{ shelf:{ sold: 3 }}`。 |
| `dimensionDataSource` | 在发布更改事件和查询中使用的维度的数据源。 如果指定数据源，您可以使用来自指定数据源的自定义维度。 库存可见性可使用维度配置将自定义维度映射到常规默认维度。 如果未指定 `dimensionDataSource` 值，则只能在查询中使用常规[基础维度](inventory-visibility-configuration.md#data-source-configuration-dimension)。 |
| `dimensions` | 动态键-值对。 这些值将映射到 Supply Chain Management 中的某些维度。 但是，也可以添加自定义维度（例如，_来源_）以指示事件来自 Supply Chain Management 还是外部系统。 |

> [!NOTE]
> `SiteId` 和 `LocationId` 参数构造[分区配置](inventory-visibility-configuration.md#partition-configuration)。 因此，在创建现有库存更改事件时，必须在维度中指定这些参数，设置或覆盖现有库存数量，或创建预留事件。

### <a name="create-one-on-hand-change-event"></a><a name="create-one-onhand-change-event"></a>创建一个现有库存更改事件

此 API 用于创建一个现有库存更改事件。

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # Optional
        dimensions: {
            [key:string]: string,
        },
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
    }
```

以下示例显示示例正文内容。 在此示例中，您将发布 *T 恤杉* 产品的更改事件。 此事件来自销售点 (POS) 系统，客户将一件红色 T 恤杉退回给了您的商店。 此事件将使 *T 恤杉* 产品的数量加 1。

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "PosMachineId": "0001",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

以下示例显示不带 `dimensionDataSource` 的示例正文内容。 在此示例中，`dimensions` 将为[基础维度](inventory-visibility-configuration.md#data-source-configuration-dimension)。 如果设置 `dimensionDataSource`，`dimensions` 可以是数据源维度或基础维度。

```json
{
    "id": "123456",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>创建多个更改事件

此 API 可以同时创建多个记录。 此 API 和[单事件 API](#create-one-onhand-change-event) 的唯二差异是 `Path` 和 `Body`值。 对于此 API，`Body` 提供一组记录。 最大记录数为 512，这意味着现有库存更改批量 API 一次最多可支持 512 个更改事件。

```txt
Path:
    /api/environment/{environmentId}/onhand/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
        ...
    ]
```

以下示例显示示例正文内容。

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId&quot;: &quot;0001"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "654321",
        "organizationId": "usmf",
        "productId": "Pants",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>设置/覆盖现有库存数量

_设置现有库存_ API 覆盖指定产品的当前数据。

```txt
Path:
    /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string, # Optional
            dimensions: {
                [key:string]: string,
            },
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifiedDateTimeUTC: datetime,
        },
        ...
    ]
```

以下示例显示示例正文内容。 此 API 的行为与本主题前面的[创建现有库存更改事件](#create-onhand-change-event)部分中介绍的 API 的行为不同。 在此示例中，将把 *T 恤杉* 产品的数量设置为 1。

```json
[
    {
        "id": "123456",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
             "PosSiteId": "1",
            "PosLocationId": "11",
            "PosMachineId": "0001"
        },
        "quantities": {
            "pos": {
                "inbound": 1
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>创建预留事件

若要使用 *预留* API，必须开启预留功能并完成预留配置。 有关详细信息，请参阅[预留配置（可选）](inventory-visibility-configuration.md#reservation-configuration)。

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>创建一个预留事件

可以针对不同数据源设置进行预留。 若要配置这种类型的预留，请先在 `dimensionDataSource` 参数中指定数据源。 然后，在 `dimensions` 参数中根据目标数据源中的维度设置指定维度。

调用预留 API 时，可以通过在请求正文中指定 `ifCheckAvailForReserv` 布尔值参数来控制预留验证。 值为 `True` 表示需要验证，而值为 `False` 则表示不需要验证。 默认值为 `True`。

如果要取消预留或撤消指定的库存数量，请将数量设置为负数，然后将 `ifCheckAvailForReserv` 参数设置为 `False` 以跳过验证。

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string,
        dimensions: {
            [key:string]: string,
        },
        quantityDataSource: string, # optional
        quantities: {
            [dataSourceName:string]: {
                [key:string]: number,
            },
        },
        modifier: string,
        quantity: number,
        ifCheckAvailForReserv: boolean,
    }
```

以下示例显示示例正文内容。

```json
{
    "id": "reserve-0",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softreservordered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    }
}
```

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>创建多个预留事件

此 API 是[单事件 API](#create-one-reservation-event) 的批量版本。

```txt
Path:
    /api/environment/{environmentId}/onhand/reserve/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantities: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
            modifier: string,
            quantity: number,
            ifCheckAvailForReserv: boolean,
        },
        ...
    ]
```

## <a name="query-on-hand"></a>查询现有库存

使用 _查询现有库存_ API 提取产品的当前现有库存数据。 API 当前最多支持按 `ProductID` 值查询 100 个单个项。 也可以在每个查询中指定多个 `SiteID` 值和 `LocationID` 值。 最大限制定义为 `NumOf(SiteID) * NumOf(LocationID) <= 100`。

### <a name="query-by-using-the-post-method"></a><a name="query-with-post-method"></a>使用过帐方法查询

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

在此请求的正文部分中，`dimensionDataSource` 仍是可选参数。 如果未设置此参数，将把 `filters` 视为 *基础维度*。 `filters` 有四个必填字段：`organizationId`、`productId`、`siteId` 和 `locationId`。

- `organizationId` 中应仅包含一个值，但它仍然是数组。
- `productId` 中可以包含一个或多个值。 如果它是空数组，将返回所有产品。
- `siteId` 和 `locationId` 用于在库存可见性中分区。 您可以在 *查询现有库存* 请求中指定多个 `siteId` 和 `locationId` 值。 在当前版本中，必须同时指定 `siteId` 和 `locationId` 值。

`groupByValues` 参数应遵循您的索引配置。 有关详细信息，请参阅[产品索引层次结构配置](./inventory-visibility-configuration.md#index-configuration)。

`returnNegative` 参数控制结果中是否包含负条目。

以下示例显示示例正文内容。

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "LocationId": ["11"],
        "ColorId": ["Red"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

以下示例显示如何查询特定站点和位置中的所有产品。

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": [],
        "siteId": ["1"],
        "LocationId": ["11"],
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true
}
```

### <a name="query-by-using-the-get-method"></a><a name="query-with-get-method"></a>使用获取方法查询

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

下面是示例获取 URL。 此获取请求与前面提供的过帐示例完全相同。

```txt
/api/environment/{environmentId}/onhand?organizationId=usmf&productId=T-shirt&SiteId=1&LocationId=11&ColorId=Red&groupBy=ColorId,SizeId&returnNegative=true
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
