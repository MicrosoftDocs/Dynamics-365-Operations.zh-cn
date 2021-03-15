---
title: 库存可见性加载项
description: 本主题介绍如何为 Dynamics 365 Supply Chain Management 安装和配置库存可见性加载项。
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114662"
---
# <a name="inventory-visibility-add-in"></a>库存可见性加载项

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

库存可见性加载项是一项独立且高度可扩展的微服务，可实现实时现有库存跟踪，并提供库存可见性的全局视图。

通过低级别 SQL 集成，准实时地将与现有库存相关的所有信息导出到服务中。 外部系统通过 RESTful API 访问服务，以查询有关给定维度集的现有信息，从而检索可用现有位置的列表。

库存可见性是基于 Microsoft Dataverse 生成的微服务，这意味着您可以通过生成 Power Apps 和应用 Power BI 来扩展它，从而提供自定义功能以满足您的业务需求。 也可以升级索引以进行库存查询。

库存可见性提供配置选项，使其可以与多个第三方系统集成。 它支持标准化的库存维度、自定义的可扩展性以及标准化的可配置的计算数量。

本主题介绍如何为 Dynamics 365 Supply Chain Management 安装和配置库存可见性加载项，以及如何使用其应用程序编程接口 (API)。

## <a name="install-the-inventory-visibility-add-in"></a>安装库存可见性加载项

您需要使用 Microsoft Dynamics Lifecycle Services (LCS) 安装库存可见性加载项。 LCS 是一个协作门户，可提供环境和一组定期更新的服务，以帮助您管理 Dynamics 365 Finance and Operations 应用的应用程序生命周期。

有关详细信息，请参阅 [Lifecycle Services 资源](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs)。

### <a name="prerequisites"></a>先决条件

在安装库存可见性加载项之前，您必须执行以下操作：

- 获取至少部署了一个环境的 LCS 实施项目。
- 在 LCS 中为您的产品/服务生成测试密钥。
- 在 LCS 中为您的用户启用产品/服务的测试密钥。
- 请与 Microsoft 库存可见性产品团队联系，并提供要在其中部署库存可见性加载项的环境 ID。

如果您对这些先决条件有任何疑问，请与库存可视性产品团队联系。

### <a name="install-the-add-in"></a><a name="install-add-in"></a>安装加载项

若要安装库存可见性加载项，请执行以下操作：

1. 登录到 [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) 门户。
1. 在主页上，选择在其中部署环境的项目。
1. 在项目页面上，选择要在其中安装加载项的环境。
1. 在环境页面上，向下滚动，直到看到 **环境加载项** 部分。 如果看不到该部分，请确保已完全处理必备的测试密钥。
1. 在 **环境加载项** 部分中，选择 **安装新加载项**。
    ![LCS 中的环境页面](media/inventory-visibility-environment.png "LCS 中的环境页面")
1. 选择 **安装新加载项** 链接。 将打开可用加载项的列表。
1. 从列表中选择 **库存服务**。 （请注意，这现在可能作为 **Dynamics 365 Supply Chain Management 的库存可见性加载项** 列出。）
1. 为您的环境输入以下字段的值：

    - **AAD 应用程序 ID**
    - **AAD 租户 ID**

    ![加载项设置页面](media/inventory-visibility-setup.png "加载项设置页面")

1. 通过选中 **条款和条件** 复选框同意条款和条件。
1. 选择 **安装**。 加载项的状态将显示为 **正在安装**。 完成后，刷新页面以查看状态更改为 **已安装**。

### <a name="get-a-security-service-token"></a>获取安全服务令牌

通过执行以下操作获取安全服务令牌：

1. 登录到 Azure 门户，使用它为您的 Supply Chain Management 应用程序查找 `clientId` 和 `clientSecret`。
1. 通过提交包含以下属性的 HTTP 请求来获取 Azure Active Directory 令牌 (`aadToken`)：
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **方法** - `GET`
    - **正文内容（窗体数据）**：

        | 键 | 值 |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | resource | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. 您应该会在响应中收到一个 `aadToken`，类似于以下示例。

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

1. 创建一个类似于以下请求的 JSON 请求：

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    其中：
    - `client_assertion` 值必须是您在上一步中收到的 `aadToken`。
    - `context` 值必须是要在其中部署加载项的环境 ID。
    - 如示例中所示设置所有其他值。

1. 提交包含以下属性的 HTTP 请求：
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **方法** - `POST`
    - **HTTP 标题** - 包含 API 版本（键为 `Api-Version`，值为 `1.0`）
    - **正文内容** - 包括您在上一步中创建的 JSON 请求。

1. 您将获得 `access_token` 作为回应。 您需要使用它作为持有者令牌来调用库存可见性 API。 下面是一个示例。

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a>卸载加载项

若要卸载加载项，请选择 **卸载**。 刷新 LCS，库存可见性加载项将会删除。 卸载流程将删除加载项注册，还将启动作业以清理存储在服务中的所有业务数据。

## <a name="inventory-visibility-add-in-public-api"></a>库存可见性加载项公共 API

库存可见性加载项的公共 REST API 提供集成的几个特定终结点。 它支持三种主要交互类型：

- 从外部系统发布对加载项的现有更改。
- 从外部系统查询当前的现有数量。
- 自动与现有 Supply Chain Management 同步。

自动同步不是公共 API 的一部分，而是在启用了库存可见性加载项的环境中在后台处理。

### <a name="authentication"></a>身份验证

平台安全令牌用于调用库存可见性加载项，因此您必须使用 Azure Active Directory 应用程序生成 Azure Active Directory 令牌。

有关如何获取安全令牌的详细信息，请参阅[安装库存可见性加载项](#install-add-in)。

### <a name="configure-the-inventory-visibility-api"></a>配置库存可见性 API

使用该服务之前，必须完成以下子部分中所述的配置。 配置因您的环境的详细信息而异。 它主要包括四个部分：

- [分区](#partitioning)
- [维度配置](#dimension-configurations)
- [正在索引](#indexing)
- [自定义度量](#custom-measurement)

#### <a name="partitioning"></a>分区

分区会显著影响库存可见性 API 的性能。 最好定义一个方案，允许将数据进行小规模分组，同时仍然允许有意义的数据查询。

`organizationId`（Supply Chain Management 中的 `dataAreaId`）将始终是分区的一部分，并且默认情况下，库存可见性按维度（*站点 + 库位*）设置为分区。 这意味着必须始终使用在筛选器上定义的这些维度来查询服务。

> [!NOTE]
> *站点* 和 *库位* 是库存可见性中的两个常规默认维度。 在 Supply Chain Management 中，这些维度称为 *站点* (`InventSiteId`) 和 *仓库* (`InventLocationId`)

### <a name="dimension-configurations"></a>维度配置

库存可见性将提供常规默认维度的列表，以启用多源系统集成。

下表列出了库存维度，它们将是库存可见性中的默认维度名称。

| 维度类型 | 维度名称 |
|---|---|
| 产品 | `ColorId` |
| 产品 | `SizeId` |
| 产品 | `StyleId` |
| 产品 | `ConfigId` |
| 跟踪 | `BatchId` |
| 跟踪 | `SerialId` |
| 库位 | `LocationId` |
| 库位 | `SiteId` |
| 库存状态 | `StatusId` |
| 仓库特定 | `WMSLocationId` |
| 仓库特定 | `WMSPalletId` |
| 仓库特定 | `LicensePlateId` |

> [!NOTE]
> 上表中列出的维度类型仅供参考。 您无需在库存可见性中定义维度类型。

如果自定义维度已存在，并且在由库存可见性使用时需要流入默认值，可以在库存可见性中配置 **自定义维度** 名称。

外部系统通过 RESTful API 访问库存可见性，这些 API 可以查询给定维度集上的现有信息。 对于集成，库存可见性使您能够在库存可见性中将 *外部通道数据源* 以及来源维度配置为 *目标维度*。

目标维度应为以下维度之一：

- 库存可见性中的默认维度
- 自定义维度

维度配置的目的是标准化维度查询和维度发布事件的多系统集成。

#### <a name="indexing"></a>正在索引

在大多数情况下，库存现有查询不仅会处于最高的“总计”级别，而且您可能希望查看基于库存维度汇总的结果。

库存可视性通过允许您设置基于维度或维度组合的索引来提供灵活性。

> [!NOTE]
> 当前，您最多只能配置五个索引。 您需要在实施之前仔细考虑将使用哪个维度或维度组合，以确保它可以满足您的业务需求。 例如，如果要查询产品，如下所示：

- 按 *颜色* 和 *尺寸* 维度查询汇总的现有产品。
- 在某些情况下，您只想查询全部产品。

您将有两个定义如下的索引：

- `["ColorId", "SizeId"]`
- `[]`

空括号将基于分区内的产品 ID 进行汇总。

索引定义如何基于 `groupBy` 查询设置对结果进行分组。 在这种情况下，如果您未定义任何 `groupBy` 值，您将按 `productid` 获得总计。 否则，如果您将 `groupBy` 定义为 `groupBy=ColorId&groupBy=SizeId`，将基于系统中的不同颜色和尺寸组合返回多行。

您可以将查询条件放入请求正文中。

下面是有关具有颜色和尺寸组合的产品的示例查询。

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="custom-measurement"></a>自定义度量

默认度量数量将链接到 Supply Chain Management，但是您可能希望拥有由默认度量组合组成的数量。 为此，您可以配置自定义数量，它们将添加到现有查询的输出中。

该功能仅允许您定义一组要添加的度量，和/或一组要减去的度量，以便形成自定义度量。

例如，在以下查询条件下，您将自定义度量数量配置为由消耗系统消耗的 `MyCustomAvailableforReservation`。

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| 消耗系统 | 计算的度量 | 数据源 | 修饰符 | 修饰符计算类型 |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | 增加额 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | 增加额 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | 减 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | 增加额 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | 减 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | 增加额 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | 增加额 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | 减 |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | 减 |

这样，对自定义度量数量的查询将返回以下输出。

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

`MyCustomAvailableforReservation` 输出基于自定义度量中的计算设置，如下所示：  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>发布现有更改

该事件将发布到的确切 URL 将取决于您的地理区域。 它将采用以下形式：

`https://{serviceURL}/api/environment/{environmentId}/onhand`

经过身份验证后，此 URL 可以与 HTTP `POST` 方法一起使用以将现有更改事件发送到服务。

特殊标题用于通过 HTTP 请求与 Dynamics 365 服务通信，表示数据链接到的 Supply Chain Management 实例的环境 ID。 例如:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>发布现有更改查询示例 1

本示例显示将在 Power Apps 中设置维度配置的场景。

使用以下查询在以 Power Apps 中配置维度映射：

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

现在，您可以指定 `dimensionDataSource` 并在查询中使用自定义维度。 系统会自动将自定义维度转换为基本维度。

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>发布现有更改查询示例 2

本示例显示不在 Power Apps 中为维度配置设置映射，因此发布还应该使用基本维度的场景。 当 `dimensionDataSource` 字段为 null、空或空白时，所有维度都必须是基本维度。

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON 文档字段属性

先前提供的 JSON 查询示例中的字段具有下表中列出的属性。

| 字段 ID | 说明 |
|---|---|
| `id` | 特定更改事件的唯一 ID。 此 ID 用于确保如果在发布过程中与服务的通信失败，重新提交事件不会导致同一事件在系统中计入两次。 |
| `organizationId` | 链接到事件的组织的标识符。 这将映射到 Supply Chain Management 组织或数据区域 ID。 |
| `productId` | 所讨论的订单的标识符。 |
| `quantity` | 需要更改现有量所依据的数量。 例如，如果将 10 个新的百吉饼添加到货位上，该值将为 10。 然后，如果将 3 个百吉饼从货位中下架或出售，则该值将为 -3。 |
| `dimensionDataSource` | 在发布更改事件和查询中使用的维度的数据源。 如果指定数据源，您可以使用来自指定数据源的自定义维度。 使用维度配置，库存可见性可以将自定义维度映射到常规默认维度。 如果未指定 `dimensionDataSource`，只能在查询中使用常规默认维度。   |
| `dimensions` | 键/值对的动态包。 这些将映射到 Supply Chain Management 中的某些维度，但是您也可以添加自定义维度（例如 *源*），这可以表示事件是来自 Supply Chain Management 还是外部系统。 |

### <a name="querying-current-on-hand"></a>查询当前现有量

用于查询当前现有量的终结点将具有类似的 URL：

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

将使用 HTTP `POST` 方法查询它。

#### <a name="current-on-hand-query-example-1"></a>当前现有查询示例 1

本示例显示已在 Power Apps 中完成维度配置的场景。

使用以下查询在以 Power Apps 中配置维度映射：

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

现在，您可以指定 `dimensionDataSource` 并在查询中使用自定义维度。 系统会自动将自定义维度转换为基本维度。 您可以在 `filters` 中指定 `DimensionDataSource`，并在 `filters` 和 `groupByValues` 中指定自定义维度。 系统会自动将自定义维度转换为基本维度。

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>当前现有查询示例 2

本示例显示不在 Power Apps 中为维度配置设置映射，因此发布还应该使用基本维度的场景。 当在 `filters` 下 `dimensionDataSource` 字段为 null、空或空白时，所有维度都必须是基本维度。

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>返回结果示例

前面示例中显示的查询可能返回如下结果。

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

请注意，数量字段将构造为度量及其相关值的字典。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]