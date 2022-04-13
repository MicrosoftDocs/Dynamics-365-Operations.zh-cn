---
title: 导入需求预测的历史数据
description: 若要获取准确的需求预测，您需要每个物料或物料分配参数的历史需求数据。 本主题说明如何使用数据实体从任何一个系统导入历史需求数据，以便您具有需求预测数据的更长历史记录。
author: t-benebo
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c52d27d6e3aa8a20d6cc1dc81e4ade981c6a8091
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470392"
---
# <a name="import-historical-data-for-demand-forecasts"></a>导入需求预测的历史数据

[!include [banner](../includes/banner.md)]

为了帮助确保需求预测的准确性，您必须尽可能多地获得每个物料或物料分配参数的历史需求数据。 如果尚未导入历史需求数据，请使用 Dynamics 365 Supply Chain Management 中 **历史外部需求** (ReqDemPlanHistoricalExternalDemandEntity) 导入它。

在 **数据管理** 工作区，您可以看到实体中所有字段的概览。

1. 打开 **数据管理** 工作区。
2. 选择 **数据实体** 磁贴。
3. 搜索实体列表查找 **历史外部需求**。
4. 选择 **目标字段**。 实体以下字段是必需的：站点 (**DeliveringSiteId**)、日期 (**DemandDate**)、数量 (**DemandQuantity**) 和物料编号 (**ItemNumber**) 或物料分配参数 (**ProductAllocationKeyId**)。

若要使用数据实体，您必须有包含历史需求数据的 Microsoft Excel 文件或逗号分隔值 (CSV) 文件。 以下示例显示如何从 CSV 文件导入数据。

有关如何导入数据（包括如何在导入后清理数据）的详细信息，请参阅[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)及其相关主题。

另请参阅[生成统计基准预测](generate-statistical-baseline-forecast.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]