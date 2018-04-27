---
title: "导入需求预测的历史数据"
description: "若要获取准确的需求预测，您需要每个物料或物料分配参数的历史需求数据。 本主题说明如何使用数据实体从任何一个系统导入历史需求数据，以便您具有需求预测数据的更长历史记录。"
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 02daa312d74311432c0c468e3e691637dcf94157
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="import-historical-data-for-demand-forecasts"></a>导入需求预测的历史数据

[!INCLUDE [banner](../includes/banner.md)]

为了帮助确保需求预测的准确性，您必须尽可能多地获得每个物料或物料分配参数的历史需求数据。 如果尚未导入历史需求数据，请使用 Microsoft Dynamics 365 for Finance and Operations 中**历史外部需求** (ReqDemPlanHistoricalExternalDemandEntity) 导入它。

在**数据管理**工作区，您可以看到实体中所有字段的概览。

1. 打开**数据管理**工作区。
2. 单击**数据实体**磁贴。
3. 搜索实体列表查找**历史外部需求**。
4. 单击**目标字段**。 实体以下字段是必需的：站点 (**DeliveringSiteId**)、日期 (**DemandDate**)、数量 (**DemandQuantity**) 和物料编号 (**ItemNumber**) 或物料分配参数 (**ProductAllocationKeyId**)。

若要使用数据实体，您必须有包含历史需求数据的 Microsoft Excel 文件或逗号分隔值 (CSV) 文件。 以下示例显示如何从 CSV 文件导入数据。

## <a name="example"></a>示例

您可以使用以下文件作为示例。 下载 [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast)。 此文件包含物料 D0001 的历史需求数据。 它仅包含以下必填字段：站点、数量和需求日期。

1. 选择历史需求数据要导入到的公司。
2. 打开**数据管理**工作区。
3. 单击**导入**磁贴。
4. 为导入项目输入一个名称，如**导入物料 D0001 的历史需求**。
5. 在**源数据格式**字段中，选择您导入的文件的文件格式。 若要导入此示例的 HistoricalDemandData 文件，选择 **CSV**。
6. 在**实体名称**字段，选择**历史外部需求**。
7. 将文件保存到您的计算机，然后上载。
8. 单击**导入**。
9. **执行汇总**页自动打开。 验证页面上导入的数据。

在您导入历史需求数据后，可以生成需求预测。

## <a name="see-also"></a>请参阅

[生成统计基准预测](generate-statistical-baseline-forecast.md)

