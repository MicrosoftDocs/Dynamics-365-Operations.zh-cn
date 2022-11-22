---
title: Inventory Visibility 公共 API
description: 本文介绍库存可见性提供的公共 API。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8b0b8ca261237fbb2190f2a94cc11b816ae05af5
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762826"
---
# <a name="inventory-visibility-public-apis"></a>Inventory Visibility 公共 API

[!include [banner](../includes/banner.md)]

本文介绍库存可见性提供的公共 API。

库存可见性加载项的公共 REST API 为集成提供几个特定终结点。 它支持四种主要交互类型：

- 从外部系统发布对加载项的现有库存量更改
- 从外部系统设置或覆盖加载项中的现有库存数量
- 从外部系统将预留事件过帐到加载项
- 从外部系统查询当前的现有数量

下表列出了当前可用的 API：

| 路径 | 方法 | 说明 |
|---|---|---|
| /api/environment/{environmentId}/onhand | 过帐 | [创建一个现有库存更改事件](#create-one-onhand-change-event)|
| /api/environment/{environmentId}/onhand/bulk | 过帐 | [创建多个更改事件](#create-multiple-onhand-change-events) |
| /api/environment/{environmentId}/setonhand/{inventorySystem}/bulk | 过帐 | [设置/覆盖现有库存数量](#set-onhand-quantities) |
| /api/environment/{environmentId}/onhand/reserve | 过帐 | [创建一个软预留事件](#create-one-reservation-event) |
| /api/environment/{environmentId}/onhand/reserve/bulk | 过帐 | [创建多个软预留事件](#create-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/unreserve | 过帐 | [撤销一个软预留事件](#reverse-one-reservation-event) |
| /api/environment/{environmentId}/onhand/unreserve/bulk | 过帐 | [撤销多个软预留事件](#reverse-multiple-reservation-events) |
| /api/environment/{environmentId}/onhand/changeschedule | 过帐 | [创建一个计划现有库存更改](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/changeschedule/bulk | 过帐 | [创建多个带日期的现有量更改](inventory-visibility-available-to-promise.md) |
| /api/environment/{environmentId}/onhand/indexquery | 过帐 | [使用 post 方法查询](#query-with-post-method)（推荐） |
| /api/environment/{environmentId}/onhand | 获取 | [使用获取方法查询](#query-with-get-method) |
| /api/environment/{environmentId}/onhand/exactquery | 过帐 | [使用 post 方法进行精确查询](#exact-query-with-post-method) |
| /api/environment/{environmentId}/allocation<wbr>/allocate | 过帐 | [创建一个分配事件](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/unallocate | 过帐 | [创建一个取消分配事件](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/reallocate | 过帐 | [创建一个重新分配事件](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/consume | 过帐 | [创建一个使用事件](inventory-visibility-allocation.md#using-allocation-api) |
| /api/environment/{environmentId}/allocation<wbr>/query | 过帐 | [查询分配结果](inventory-visibility-allocation.md#using-allocation-api) |

> [!NOTE]
> 此路径的 {environmentId} 部分是 Microsoft Dynamics Lifecycle Services 中的环境 ID。
> 
> 批量 API 最多可为每个请求返回 512 条记录。

Microsoft 提供了现成的 *Postman* 请求集合。 可以使用以下共享链接将此集合导入到 *Postman* 软件中：<https://www.getpostman.com/collections/95a57891aff1c5f2a7c2>。

## <a name="find-the-endpoint-according-to-your-lifecycle-services-environment"></a><a name = "endpoint-lcs"></a>根据 Lifecycle Services 环境查找终结点

多个地理区域和多个区域中 Microsoft Azure Service Fabric 已部署了库存可见性微服务。 目前没有可将您的请求自动重定向到相应地理区域和区域的中央终结点。 因此，必须使用以下模式将信息段编排到 URL 中：

`https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

可以在 Lifecycle Services 环境中找到区域短名称。 下表列出了当前可用的区域。

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
| 印度中部       | cin               |
| 印度南部         | sin               |
| 瑞士北部   | nch               |
| 瑞士西部    | wch               |
| 法国南部        | sfr               |
| 东亚           | eas               |
| 东南亚     | seas              |
| 阿拉伯联合酋长国北部           | nae               |
| 挪威东部         | eno               |
| 挪威西部         | wno               |
| 南非西部   | wza               |
| 南非北部  | nza               |

岛编号是 Service Fabric 中部署 Lifecycle Services 环境的位置。 现在无法从用户端获取此信息。

Microsoft 已在 Power Apps 中内置了用户接口 (UI)，供您获取微服务的完整终结点。 有关详细信息，请参阅[查找服务终结点](inventory-visibility-configuration.md#get-service-endpoint)。

## <a name="authentication"></a><a name="inventory-visibility-authentication"></a>身份验证

平台安全令牌用于调用库存可见性公共 API。 因此，您必须使用Azure AD 应用程序生成 *Azure Active Directory (Azure AD) 令牌*。 然后，必须使用 Azure AD 令牌从安全服务获取 *访问令牌*。

Microsoft 提供了现成的 *Postman* 获取令牌集合。 可以使用以下共享链接将此集合导入到 *Postman* 软件中：<https://www.getpostman.com/collections/496645018f96b3f0455e>。

若要获取安全服务令牌，请执行以下步骤。

1. 登录 Azure 门户，然后将其用于查找 Dynamics 365 Supply Chain Management 应用的 `clientId` 和 `clientSecret` 值。
1. 通过提交具有以下属性的 HTTP 请求来获取 Azure AD 令牌 (`aadToken`)：

    - **URL：**`https://login.microsoftonline.com/${aadTenantId}/oauth2/v2.0/token`
    - **方法：**`GET`
    - **正文内容（窗体数据）：**

        | 键           | 值                                            |
        | ------------- | -------------------------------------------------|
        | client_id     | ${aadAppId}                                      |
        | client_secret | ${aadAppSecret}                                  |
        | grant_type    | client_credentials                               |
        | scope         | 0cdb527f-a8d1-4bf8-9436-b352c68682b2/.default    |

    您应通过响应收到一个 Azure AD 令牌 (`aadToken`)。 标签应类似于以下示例。

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
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
        "context": "{$LCS_environment_id}",
        "context_type": "finops-env"
    }
    ```

    请注意以下点：

    - `client_assertion` 值必须是您在上一步中收到的 Azure AD 令牌 (`aadToken`)。
    - `context` 值必须是要在其中部署加载项的 Lifecycle Services 环境 ID。
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
> 当您使用 *Postman* 请求集合调用库存可见性公共 API 时，您必须为每个请求添加一个持有者令牌。 若要查找您的持有者令牌，请在请求 URL 下选择 **授权** 选项卡，选择 **持有者令牌** 类型，并复制最后一步中提取的访问令牌。 在本文的后面章节中，`$access_token` 将用于表示上一步中提取的令牌。

## <a name="create-on-hand-change-events"></a><a name="create-onhand-change-event"></a>创建现有库存更改事件

有两个 API 可用于创建现有库存更改事件：

- 创建一个记录：`/api/environment/{environmentId}/onhand`
- 创建多个记录：`/api/environment/{environmentId}/onhand/bulk`

下表汇总了 JSON 正文中各字段的含义。

| 字段 ID | Description |
|---|---|
| `id` | 特定更改事件的唯一 ID。 如果由于服务失败而导致重新提交，此 ID 用于确保同一事件不会在系统中被计算两次。 |
| `organizationId` | 链接到事件的组织的标识符。 此值将在 Supply Chain Management 中映射到组织或数据区域 ID。 |
| `productId` | 产品的标识符。 |
| `quantities` | 必须充当现有库存数量的更改量的数量。 例如，如果将 10 本新帐簿添加到货位，则此值将为 `quantities:{ shelf:{ received: 10 }}`。 如果从货位中移除或出售了三本帐簿，则此值将为 `quantities:{ shelf:{ sold: 3 }}`。 |
| `dimensionDataSource` | 在发布更改事件和查询中使用的维度的数据源。 如果指定数据源，您可以使用来自指定数据源的自定义维度。 库存可见性可使用维度配置将自定义维度映射到常规默认维度。 如果未指定 `dimensionDataSource` 值，则只能在查询中使用常规[基础维度](inventory-visibility-configuration.md#data-source-configuration-dimension)。 |
| `dimensions` | 动态键-值对。 这些值将映射到 Supply Chain Management 中的某些维度。 但是，也可以添加自定义维度（例如，*来源*）以指示事件来自 Supply Chain Management 还是外部系统。 |

> [!NOTE]
> `siteId` 和 `locationId` 参数构造[分区配置](inventory-visibility-configuration.md#partition-configuration)。 因此，在创建现有库存更改事件时，必须在维度中指定这些参数，设置或覆盖现有库存数量，或创建预留事件。

以下各小节提供了说明如何使用这些 API 的示例。

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

以下示例显示示例正文内容。 在此示例中，公司有一个销售点 (POS) 系统，用于处理店内交易，因而会处理库存变化。 客户将一件红色 T 恤退回您的商店。 为反映此变动，您为 *T 恤* 产品发布了一个更改事件。 此事件将使 *T 恤杉* 产品的数量加 1。

```json
{
    "id": "Test201",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensionDataSource": "pos",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "posMachineId": "0001",
        "colorId": "red"
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
    "id": "Test202",
    "organizationId": "usmf",
    "productId": "T-shirt",
    "dimensions": {
        "siteId": "1",
        "locationId": "11",
        "colorId": "red"
    },
    "quantities": {
        "pos": {
            "inbound": 1
        }
    }
}
```

### <a name="create-multiple-change-events"></a><a name="create-multiple-onhand-change-events"></a>创建多个更改事件

此 API 可以创建更改事件，就像[单事件 API](#create-one-onhand-change-event) 一样。 唯一的不同是此 API 可以同时创建多个记录。 因此，`Path` 和 `Body` 值不同。 对于此 API，`Body` 提供一组记录。 最大记录数为 512。 因此，现有量更改批量 API 一次最多可以支持 512 个更改事件。 

例如，零售店 POS 机处理以下两个交易：

- 一个一件红色 T 恤的退货单
- 一笔三件黑色 T 恤的销售交易

在这种情况下，您可以在一个 API 调用中同时包含两个库存更新。

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
        "id": "Test203",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "Site1",
            "LocationId": "11",
            "posMachineId&quot;: &quot;0001"
            "colorId&quot;: &quot;red"
        },
        "quantities": {
            "pos": { "inbound": 1 }
        }
    },
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensions": {
            "siteId": "1",
            "locationId": "11",
            "colorId&quot;: &quot;black"
        },
        "quantities": {
            "pos": { "outbound": 3 }
        }
    }
]
```

## <a name="setoverride-on-hand-quantities"></a><a name="set-onhand-quantities"></a>设置/覆盖现有库存数量

*设置现有库存* API 覆盖指定产品的当前数据。 此功能通常用于进行库存盘点更新。 例如，在每日库存盘点期间，商店可能会发现某种红色 T 恤的实际现有库存为 100。 因此，无论之前的数量是多少，POS 入站数量都必须更新为 100。 您可以使用此 API 替代现有值。

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

以下示例显示示例正文内容。 此 API 的行为与本文前面的[创建现有库存更改事件](#create-onhand-change-event)一节中介绍的 API 的行为不同。 在此示例中，将把 *T 恤杉* 产品的数量设置为 1。

```json
[
    {
        "id": "Test204",
        "organizationId": "usmf",
        "productId": "T-shirt",
        "dimensionDataSource": "pos",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "posMachineId": "0001"
            "colorId": "red"
        },
        "quantities": {
            "pos": {
                "inbound": 100
            }
        }
    }
]
```

## <a name="create-reservation-events"></a>创建预留事件

若要使用 *预留* API，必须开启预留功能并完成预留配置。 有关详细信息（包括数据流和示例场景），请参阅[预留配置（可选）](inventory-visibility-configuration.md#reservation-configuration)。

### <a name="create-one-reservation-event"></a><a name="create-one-reservation-event"></a>创建一个预留事件

可以针对不同数据源设置进行预留。 若要配置这种类型的预留，请先在 `dimensionDataSource` 参数中指定数据源。 然后，在 `dimensions` 参数中根据目标数据源中的维度设置指定维度。

调用预留 API 时，可以通过在请求正文中指定 `ifCheckAvailForReserv` 布尔值参数来控制预留验证。 值为 `True` 表示需要验证，而值为 `False` 则表示不需要验证。 默认值为 `True`。

如果要撤销预留或撤消指定的库存数量，请将数量设置为负数，然后将 `ifCheckAvailForReserv` 参数设置为 `False` 以跳过验证。 还有一个专用的撤消 API 也可以完成此任务。 两种方法的不同之处仅在于调用这两个 API 的方式。 将 `reservationId` 与 *撤消* API 结合使用可以更轻松地撤销特定的预留事件。 有关更多信息，请参阅[撤消一个预留事件](#reverse-reservation-events)一节。

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
    "organizationId": "SCM_IV",
    "productId": "iv_postman_product",
    "quantity": 1,
    "quantityDataSource": "iv",
    "modifier": "softReservOrdered",
    "ifCheckAvailForReserv": true,
    "dimensions": {
        "siteId": "iv_postman_site",
        "locationId": "iv_postman_location",
        "colorId": "red",
        "sizeId&quot;: &quot;small"
    }
}
```

以下示例显示了一个成功的响应。

```json
{
    "reservationId": "RESERVATION_ID",
    "id": "ohre~id-822-232959-524",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
``` 

### <a name="create-multiple-reservation-events"></a><a name="create-multiple-reservation-events"></a>创建多个预留事件

此 API 是[单事件 API](#create-reservation-events) 的批量版本。

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

## <a name="reverse-reservation-events"></a>撤销预留事件

*撤消* API 用作 [*预留*](#create-reservation-events)事件的撤销操作。 它提供了一种方法来撤销由 `reservationId` 指定的预留事件或减少预留数量。

### <a name="reverse-one-reservation-event"></a><a name="reverse-one-reservation-event"></a>撤销一个预留事件

创建预留时，`reservationId` 将包含在响应正文中。 您必须提供相同的 `reservationId` 才能取消预留，并包括用于预留 API 调用的相同 `organizationId` 和 `dimensions`。 最后，指定表示要从先前预留中释放的项目数的 `OffsetQty` 值。 预留可以完全或部分撤销，具体取决于指定的 `OffsetQty`. 例如，如果预留了 *100* 个单位的项目，您可以指定 `OffsetQty: 10` 来撤消初始预留量 *10*。

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve
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
        reservationId: string,
        dimensions: {
            [key:string]: string,
        },
        OffsetQty: number
    }
```

以下代码显示了正文内容的示例。

```json
{
    "id": "unreserve-0",
    "organizationId": "SCM_IV",
    "reservationId": "RESERVATION_ID",
    "dimensions": {
        "siteid":"iv_postman_site",
        "locationid":"iv_postman_location",
        "ColorId": "red",
        "SizeId&quot;: &quot;small"
    },
    "OffsetQty": 1
}
```

以下代码显示了成功响应正文的示例。

```json
{
    "reservationId": "RESERVATION_ID",
    "totalInvalidOffsetQtyByReservId": 0,
    "id": "ohoe~id-823-11744-883",
    "processingStatus": "success",
    "message": "",
    "statusCode": 200
}
```

> [!NOTE]
> 在响应正文中，当 `OffsetQty` 小于或等于预留数量时，`processingStatus` 将是“*success*”，`totalInvalidOffsetQtyByReservId` 将是 *0*。
>
> 如果 `OffsetQty` 大于预留量，`processingStatus` 将是“*partialSuccess*”，`totalInvalidOffsetQtyByReservId` 将是 `OffsetQty` 与预留量之间的差值。
>
>例如，如果预留的数量为 *10*，`OffsetQty` 的值为 *12*，`totalInvalidOffsetQtyByReservId` 将是 *2*。

### <a name="reverse-multiple-reservation-events"></a><a name="reverse-multiple-reservation-events"></a>撤销多个预留事件

此 API 是[单事件 API](#reverse-one-reservation-event) 的批量版本。

```txt
Path:
    /api/environment/{environmentId}/onhand/unreserve/bulk
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
            reservationId: string,
            dimensions: {
                [key:string]: string,
            },
            OffsetQty: number
        }
        ...
    ]
```

## <a name="query-on-hand"></a>查询现有库存

使用 *查询现有库存* API 提取产品的当前现有库存数据。 当您需要了解库存时，您可以使用此 API，如当您想要在电子商务网站上查看产品库存水平时，或者当您想要跨区域或在附近的商店和仓库检查产品可用性时。 API 当前最多支持按 `productID` 值查询 5000 个单个项。 也可以在每个查询中指定多个 `siteID` 值和 `locationID` 值。 最大限制由以下方程式定义：

*NumOf(SiteID) \* NumOf(LocationID) <= 100*。

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

我们建议您使用 `groupByValues` 参数来遵循您的索引配置。 有关详细信息，请参阅[产品索引层次结构配置](./inventory-visibility-configuration.md#index-configuration)。

`returnNegative` 参数控制结果中是否包含负条目。

> [!NOTE]
> 如果您启用了现有库存更改计划和可承诺 (ATP) 功能，您的查询还可以包含 `QueryATP` 布尔参数，该参数控制查询结果是否包含 ATP 信息。 有关详细信息和示例，请参阅[库存可见性现有库存更改计划与可承诺](inventory-visibility-available-to-promise.md)。

以下示例显示示例正文内容。 它显示您可以从多个位置（仓库）查询现有库存。

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["T-shirt"],
        "siteId": ["1"],
        "locationId": ["11","12","13"],
        "colorId": ["red"]
    },
    "groupByValues": ["colorId", "sizeId"],
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
        "locationId": ["11"],
    },
    "groupByValues": ["colorId", "sizeId"],
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
/api/environment/{environmentId}/onhand?organizationId=SCM_IV&productId=iv_postman_product&siteId=iv_postman_site&locationId=iv_postman_location&colorId=red&groupBy=colorId,sizeId&returnNegative=true
```

## <a name="on-hand-exact-query"></a><a name="exact-query-with-post-method"></a>现有量准确查询

现有量准确查询类似于常规现有量查询，但允许您指定站点和位置之间的映射层次结构。 例如，您有以下两个站点：

- 站点 1，映射到位置 A
- 站点 2，映射到位置 B

对于常规现有量查询，如果指定 `"siteId": ["1","2"]` 和 `"locationId": ["A","B"]`，库存可见性将自动查询以下站点和位置的结果：

- 站点 1，位置 A
- 站点 1，位置 B
- 站点 2，位置 A
- 站点 2，位置 B

如您所见，常规现有量查询无法识别位置 A 仅存在于站点 1，位置 B 仅存在于站点 2。 因此，它会进行冗余查询。 为了适应这种分层映射，您可以使用现有量准确查询，在查询正文中指定位置映射。 在这种情况下，您将查询并收到仅站点 1、位置 A 和站点 2、位置 B 的结果。

### <a name="exact-query-by-using-the-post-method"></a><a name="exact-query-with-post-method"></a>使用 post 方法进行精确查询

```txt
Path:
    /api/environment/{environmentId}/onhand/exactquery
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
            dimensions: string[],
            values: string[][],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

在此请求的正文部分中，`dimensionDataSource` 是可选参数。 如果未设置此参数，会将 `filters` 中的 `dimensions` 视为 *基础维度*。 `filters` 有四个必填字段：`organizationId`、`productId`、`dimensions` 和 `values`。

- `organizationId` 中应仅包含一个值，但它仍然是数组。
- `productId` 中可以包含一个或多个值。 如果它是空数组，将返回所有产品。
- 在 `dimensions` 数组中，`siteId` 和 `locationId` 是必需的，但可以按任何顺序与其他元素一起出现。
- `values` 可以包含与 `dimensions` 对应的一个或多个不同的值元组。

`filters` 中的 `dimensions` 将被自动添加到 `groupByValues`。

`returnNegative` 参数控制结果中是否包含负条目。

以下示例显示示例正文内容。

```json
{
    "dimensionDataSource": "pos",
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": ["iv_postman_product"],
        "dimensions": ["siteId", "locationId", "colorId"],
        "values" : [
            ["iv_postman_site", "iv_postman_location", "red"],
            ["iv_postman_site", "iv_postman_location", "blue"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

以下示例显示如何查询多个站点和位置的所有产品。

```json
{
    "filters": {
        "organizationId": ["SCM_IV"],
        "productId": [],
        "dimensions": ["siteId", "locationId"],
        "values" : [
            ["iv_postman_site_1", "iv_postman_location_1"],
            ["iv_postman_site_2", "iv_postman_location_2"],
        ]
    },
    "groupByValues": ["colorId", "sizeId"],
    "returnNegative": true
}
```

## <a name="available-to-promise"></a>可承诺

您可以设置库存可见性，以可以计划将来的现有库存更改并计算 ATP 数量。 ATP 是可用的并且可以在下一个期间向客户承诺的物料数量。 使用 ATP 计算可以大大提高您的订单履行能力。 有关如何启用此功能以及如何在启用此功能后通过 API 与库存可见性交互的信息，请参阅[库存可见性现有库存更改计划与可承诺](inventory-visibility-available-to-promise.md#api-urls)。

## <a name="allocation"></a>分配

与分配相关的 API 位于[库存可见性分配](inventory-visibility-allocation.md#using-allocation-api)中。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
