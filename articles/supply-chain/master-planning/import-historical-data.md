---
title: 导入需求预测的历史数据
description: 若要获取准确的需求预测，您需要每个物料或物料分配参数的历史需求数据。 本主题说明如何使用数据实体从任何一个系统导入历史需求数据，以便您具有需求预测数据的更长历史记录。
author: roxanadiaconu
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
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301642"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="f3efd-104">导入需求预测的历史数据</span><span class="sxs-lookup"><span data-stu-id="f3efd-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3efd-105">为了帮助确保需求预测的准确性，您必须尽可能多地获得每个物料或物料分配参数的历史需求数据。</span><span class="sxs-lookup"><span data-stu-id="f3efd-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="f3efd-106">如果尚未导入历史需求数据，请使用 Dynamics 365 Supply Chain Management 中 **历史外部需求** (ReqDemPlanHistoricalExternalDemandEntity) 导入它。</span><span class="sxs-lookup"><span data-stu-id="f3efd-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="f3efd-107">在 **数据管理** 工作区，您可以看到实体中所有字段的概览。</span><span class="sxs-lookup"><span data-stu-id="f3efd-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="f3efd-108">打开 **数据管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="f3efd-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="f3efd-109">选择 **数据实体** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="f3efd-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="f3efd-110">搜索实体列表查找 **历史外部需求**。</span><span class="sxs-lookup"><span data-stu-id="f3efd-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="f3efd-111">选择 **目标字段**。</span><span class="sxs-lookup"><span data-stu-id="f3efd-111">Select **Target fields**.</span></span> <span data-ttu-id="f3efd-112">实体以下字段是必需的：站点 (**DeliveringSiteId**)、日期 (**DemandDate**)、数量 (**DemandQuantity**) 和物料编号 (**ItemNumber**) 或物料分配参数 (**ProductAllocationKeyId**)。</span><span class="sxs-lookup"><span data-stu-id="f3efd-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="f3efd-113">若要使用数据实体，您必须有包含历史需求数据的 Microsoft Excel 文件或逗号分隔值 (CSV) 文件。</span><span class="sxs-lookup"><span data-stu-id="f3efd-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="f3efd-114">以下示例显示如何从 CSV 文件导入数据。</span><span class="sxs-lookup"><span data-stu-id="f3efd-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="f3efd-115">有关如何导入数据（包括如何在导入后清理数据）的详细信息，请参阅[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)及其相关主题。</span><span class="sxs-lookup"><span data-stu-id="f3efd-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="f3efd-116">另请参阅[生成统计基准预测](generate-statistical-baseline-forecast.md)。</span><span class="sxs-lookup"><span data-stu-id="f3efd-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]