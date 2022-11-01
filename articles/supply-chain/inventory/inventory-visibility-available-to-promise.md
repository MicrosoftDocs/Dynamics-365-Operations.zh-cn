---
title: 库存可见性现有库存更改计划与可承诺
description: 本文介绍如何计划未来的现有库存更改以及如何计算可承诺 (ATP) 数量。
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: f831c5d5719bbbd72c7cff37b8b35826f48ce6e4
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719283"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>库存可见性现有库存更改计划与可承诺

[!include [banner](../includes/banner.md)]

本文介绍如何设置 *现有库存更改计划* 功能来计划未来的现有库存更改并计算可承诺 (ATP) 数量。 ATP 是可用的并且可以在下一个期间向客户承诺的物料数量。 使用此计算可以大大提高您的订单履行能力。

对于很多制造商、零售商或经销商来说，仅仅知道目前的现有库存是不够的。 他们必须对未来的可用性具有完全的可见性。 未来可用性应考虑未来的供给、未来的需求和 ATP。

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a>启用和设置功能

您必须设置一个或多个计算度量值来计算 ATP 数量，然后才能够使用 ATP。 您还必须启用功能并在 Microsoft Power Apps 中配置 ATP 设置。

### <a name="set-up-calculated-measures-for-atp-quantities"></a>为 ATP 数量设置计算度量值

*ATP 计算度量值* 是一个预定义的计算度量值，通常用于查找当前可用的现有库存数量。 *供应数量* 是修饰符类型为 *添加* 的那些实际度量的数量总和，而 *需求数量* 是修饰符类型为 *减法* 的那些实际度量的数量总和。

您可以添加多个计算度量值来计算多个 ATP 数量。 但是，所有 ATP 计算度量值的不同实际度量总数应小于 9。

> [!IMPORTANT]
> 计算的度量是实际度量的构成部分。 其公式只能包含不重复的实际度量，而不能包含计算的度量。

例如，您设置以下计算度量值：

**On-hand-available** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

总和 (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) 代表供应，总和 (*ReservPhysical* + *SoftReservePhysical* + *Outbound*) 代表需求。 因此，计算度量值可以这样理解：

**On-hand-available** = *供应* – *需求*

您可以添加另一个计算度量以计算 **现有实际** ATP 数量。

**On-hand-physical** = (*PhysicalInvent* + *OnHand* + *Unrestricted* + *QualityInspection* + *Inbound*) – (*Outbound*)

在这两个 ATP 计算度量中存在八种不同的物理度量：*PhysicalInvent*、*OnHand*、*Unrestricted*、*QualityInspection*、*Inbound*、*ReservPhysical*、*SoftReservePhysical* 和 *Outbound*。

有关计算度量值的详细信息，请参阅[计算度量值](inventory-visibility-configuration.md#calculated-measures)。

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>启用现有库存更改计划功能并配置 ATP 设置

按照以下步骤在 Power Apps 中启用 *现有库存更改计划* 功能并配置 ATP 设置。

1. 登录 Power Apps，打开库存可见性。
1. 打开 **管理** 页面。
1. 在 **功能管理** 选项卡上，打开 *OnhandChangeSchedule* 功能。
1. 选择 **ATP 设置** 选项卡。
1. 当您查询库存可见性时，它将提供一个包含您在此处添加的每个 ATP 计算度量值的结果。 选择 **添加** 可为 ATP 添加新的计算度量值。
1. 设置以下字段：

    - **数据源** – 选择与计算度量值关联的数据源。
    - **计算度量值** – 选择与所选数据源关联的您要用于查找当前可用现有库存数量的计算度量值。
    - **计划期间** – 输入用户在使用所选计算度量值时可以查看和提交计划现有库存更改的天数。 查询存货信息的用户将从当前日期开始，获取此期间中每天的现有库存数量、计划现有库存更改和 ATP。 选择 1 到 7 之间的一个整数。

    > [!IMPORTANT]
    > 计划期间包括当前日期。 因此，用户可以计划从当前日期（提交更改的日期）到（计划期间 - 1）天之间的任何时间发生的现有库存更改。

1. 选择 **保存**。
1. 重复步骤 5 到 7，直到您添加了 ATP 所需的所有计算度量值。
1. 完成配置所有必需设置后，选择 **更新配置**。

有关详细信息，请参阅[完成和更新配置](inventory-visibility-configuration.md)。

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>现有库存更改计划和 ATP 计算的工作原理

*现有库存更改计划* 确定计划现有库存更改的预期日期和数量。 您可以向库存可见性提交现有更改库存计划，前提是日期在 **计划期间** 设置定义的时间段内（请参阅[启用和设置功能](#setup)一节）。 查询存货信息的用户将获取该期间中每天的现有库存数量、计划现有库存更改和 ATP。

计划更改最初不会提交，因此不会影响系统中的实际现有库存数量。 要提交更改，您必须提交 *现有库存更改事件*，该事件将更新实际可用的现有库存数量。 然后，您必须通过提交匹配的负数量的现有库存更改计划来还原计划更改。

例如，您下了一个购买 10 辆自行车的订单，预期明天到达。 因此，您提交现有库存更改计划，入站数量为 10，日期为明天。 第二天订单到达时，您将自行车添加到实际现有库存中。 然后，您必须向系统提交此更改以更新实际现有库存数量。 要提交更改，您提交一个入站数量为 10 的现有库存更改事件。 然后，您通过提交入站数量为 -10 的现有库存更改计划来还原计划更改。

当您在库存可见性中查询现有库存数量和 ATP 数量时，将返回计划期间中每天的以下信息：

- **日期** – 将应用结果的日期。 时区为协调世界时 (UTC)。
- **现有库存数量** – 指定日期的实际现有库存数量。 此计算根据为库存可见性配置的 ATP 计算度量值进行。
- **计划供应** – 截至指定日期尚未实际可供立即消耗或装运的所有计划入站数量的总和。
- **计划需求** – 截至指定日期尚未消耗或装运的所有计划出站数量的总和。
- **ATP 数量** – 从指定日期到计划期间结束这段时间内可用的预计的最小现有库存数量。 此数量包括所有计划的数量调整。 这是可在当前日期承诺的可在当天交货或消耗的的最大数量。

例如，如果当前日期为 2022 年 2 月 1 日，计划期间为 7，用户可以提交预计从 2022 年 2 月 1 日到 2 月 7 日之间发生的计划现有库存更改。 举例来说，在这种情况下，2 月 3 日的 ATP 数量是根据该日的现有库存数量以及从 2 月 3 日到 2 月 7 日的计划数量计算的。

## <a name="example"></a>示例

以下示例显示一系列计划数量更改如何影响库存可见性报告的现有库存数量和 ATP 数量。 另外还显示了如何提交计划更改、承诺计划更改如何影响结果，以及如果未提交计划更改可能会发生的情况。

此示例中的结果显示 *预计的现有库存* 值。 此值包含用于说明目的但在查询库存可见性时实际并未报告的所有计划更新。

1. 在 Power Apps 中的 **ATP 设置** 页面上为您的系统配置了以下设置：

    - **ATP 计算度量值** – 您具有名为 *现有库存* 的计算度量值。 此值计算为 *现有库存 = 供应 – 需求*。 您在此处选择该度量值。
    - **计划期间** – 您选择 *7*。

1. 下列情况也适用：

    - 当前日期是 2022 年 2 月 1 日。
    - 当前的现有库存数量为 20。

1. 对于当前日期（2022 年 2 月 1 日），您将计划需求数量 3 提交到库存可见性。 因此，预计的现有库存数量是 17。 下表显示了结果。

    | 日期 | 现有量 | 计划供应 | 计划需求 | 预计现有库存 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | | | 17 | 17 |
    | 2022-02-04 | 20 | | | 17 | 17 |
    | 2022-02-05 | 20 | | | 17 | 17 |
    | 2022-02-06 | 20 | | | 17 | 17 |
    | 2022-02-07 | 20 | | | 17 | 17 |

1. 在当前日期（2022 年 2 月 1 日），您为 2022 年 2 月 3 日提交计划供应数量 10。 下表显示了结果。

    | 日期 | 现有量 | 计划供应 | 计划需求 | 预计现有库存 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | 10 | | 27 | 27 |
    | 2022-02-04 | 20 | | | 27 | 27 |
    | 2022-02-05 | 20 | | | 27 | 27 |
    | 2022-02-06 | 20 | | | 27 | 27 |
    | 2022-02-07 | 20 | | | 27 | 27 |

1. 在当前日期（2022 年 2 月 1 日），您提交以下计划数量更改：

    - 2022 年 2 月 4 日的需求数量为 15
    - 2022 年 2 月 5 日的供应数量为 1
    - 2022 年 2 月 6 日的供应数量为 3

    下表显示了结果。

    | 日期 | 现有量 | 计划供应 | 计划需求 | 预计现有库存 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 12 |
    | 2022-02-02 | 20 | | | 17 | 12 |
    | 2022-02-03 | 20 | 10 | | 27 | 12 |
    | 2022-02-04 | 20 | | 15 | 12 | 12 |
    | 2022-02-05 | 20 | 1 | | 13 | 13 |
    | 2022-02-06 | 20 | 3 | | 16 | 16 |
    | 2022-02-07 | 20 | | | 16 | 16 |

1. 在当前日期（2022 年 2 月 1 日），您装运计划需求数量 3。 因此，您必须提交此更改，让它反映在实际现有库存数量中。 要提交更改，您提交一个出站数量为 3 的现有库存更改事件。 然后，您通过提交出站数量为 -3 的现有库存更改计划来还原计划更改。 下表显示了结果。

    | 日期 | 现有量 | 计划供应 | 计划需求 | 预计现有库存 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 17 | | 0 | 17 | 12 |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |

1. 第二天（2022 年 2 月 2 日），计划期间前移一天。 下表显示了结果。

    | 日期 | 现有量 | 计划供应 | 计划需求 | 预计现有库存 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |
    | 2022-02-08 | 17 | | | 16 | 16 |

1. 但是，两天后（2022 年 2 月 4 日），为 2 月 3 日计划的供应数量 10 仍未到达。 下表显示了结果。

    | 日期 | 现有量 | 计划供应 | 计划需求 | 预计现有库存 | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-04 | 17 | | 15 | 2 | 2 |
    | 2022-02-05 | 17 | 1 | | 3 | 3 |
    | 2022-02-06 | 17 | 3 | | 6 | 6 |
    | 2022-02-07 | 17 | | | 6 | 6 |
    | 2022-02-08 | 17 | | | 6 | 6 |
    | 2022-02-09 | 17 | | | 6 | 6 |
    | 2022-02-10 | 17 | | | 6 | 6 |

    如您所见，计划（但不承诺）现有库存更改不会影响实际现有库存数量。

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a>通过 API 提交更改计划、更改事件和 ATP 查询

您可以使用以下应用程序编程接口 (API) URL 提交现有库存更改计划、更改事件和查询。

| 路径 | 方法 | Description |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | 创建一个计划现有库存更改。 |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | 创建多个计划现有库存更改。 |
| `/api/environment/{environmentId}/onhand` | `POST` | 创建一个现有库存更改事件。 |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | 创建多个更改事件。 |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | 使用 `POST` 方法查询。 |
| `/api/environment/{environmentId}/onhand` | `GET` | 使用 `GET` 方法查询。 |
| `/api/environment/{environmentId}/onhand/exactquery` | `POST` | 使用 `POST` 方法进行精确查询。 |

有关详细信息，请参阅[库存可见性公共 API](inventory-visibility-api.md)。

### <a name="create-one-on-hand-change-schedule"></a>创建一个现有库存更改计划

通过向相关库存可见性服务 URL 提交 `POST` 请求来创建现有库存更改计划（请参阅[通过 API 提交更改计划、更改事件和 ATP 查询](#api-urls)）。 您还可以提交批量请求。

仅当计划日期在当前日期和当前计划期间结束日期之间时，才可以创建现有库存更改计划。 日期/时间格式应为 *年-月-日*（例如 **2022-02-01**）。 时间格式必须只精确到天。

此 API 用于创建一个现有库存更改计划。

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
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
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

以下示例显示不带 `dimensionDataSource` 的示例正文内容。

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>创建多个现有库存更改计划

此 API 可以同时创建多个记录。 此 API 和单事件 API 的唯二差异是 `Path` 和 `Body` 值。 对于此 API，`Body` 提供一组记录。 最大记录数为 512。 因此，现有库存更改计划批量 API 一次最多可以支持 512 项计划更改。

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
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
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
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
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>创建现有库存更改事件

通过向相关库存可见性服务 URL 提交 `POST` 请求来建立现有库存更改事件（请参阅[通过 API 提交更改计划、更改事件和 ATP 查询](#api-urls)）。 您还可以提交批量请求。

> [!NOTE]
> 现有更改事件不是 ATP 功能独有的，而是标准库存可见性 API 的一部分。 之所以包含此示例，是因为在您使用 ATP 时事件是相关的。 现有库存更改事件类似于现有库存更改预留，但事件消息必须发送到不同的 API URL，并且事件在消息正文中使用 `quantities` 而不是 `quantityByDate`。 有关库存可见性 API 的现有库存更改事件和其他功能的详细信息，请参阅[库存可见性公共 API](inventory-visibility-api.md#create-one-onhand-change-event)。

以下示例显示包含单个现有库存更改事件的请求正文。

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>查询计划现有库存更改和 ATP 结果

您可以通过向适当的 API URL 提交 `POST` 请求或 `GET` 请求来查询计划现有库存更改和 ATP 结果（请参阅[通过 API 提交更改计划、更改事件和 ATP 查询](#api-urls)一节）。

如果您想要查询计划现有库存更改和 ATP 结果，在您的请求中将 `QueryATP` 设置为 *true*。

- 如果您使用 `GET` 方法提交请求，请在 URL 中设置此参数。
- 如果您使用 `POST` 方法提交请求，请在请求正文中设置此参数。

> [!NOTE]
> 无论请求正文中的 `returnNegative` 参数是设置为 *true* 还是 *false*，当您查询计划现有库存更改和 ATP 时，结果都将包含负值。 将包括这些负值，因为如果仅计划需求订单，或者如果供应数量小于需求数量，计划现有库存更改数量将为负数。 如果不包括负值，结果会令人困惑。 有关此选项以及它如何适用于其他类型的查询的详细信息，请参阅[库存可见性公共 API](inventory-visibility-api.md#query-with-post-method)。

### <a name="query-by-using-the-post-method"></a>使用 POST 方法查询

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

以下示例显示如何使用 `POST` 方法创建可以提交到库存可见性的索引查询请求正文。

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "SiteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-by-using-the-get-method"></a>使用 GET 方法查询

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

以下示例显示如何作为 `GET` 请求创建索引查询请求 URL。

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

此 `GET` 请求的结果与上一示例中 `POST` 请求的结果完全相同。

### <a name="exact-query-by-using-the-post-method"></a>使用 POST 方法进行精确查询

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

以下示例显示如何使用 `POST` 方法创建可以提交到库存可见性的精确查询请求正文。

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "dimensions": ["SiteId", "LocationId"],
        "values": [
            ["1", "11"]
        ]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="query-result-example"></a>查询结果示例

前面的任何查询示例都可能生成以下回复。 对于此示例，系统配置了以下设置：

- **ATP 计算度量值**：*iv.onhand = pos.inbound – pos.outbound*
- **计划期间**：*7*

以下是一个回复正文的示例。

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
