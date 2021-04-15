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
ms.openlocfilehash: 9bb3c178a698bdcd46e7c596247360ba9233b398
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816476"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="ec10b-104">导入需求预测的历史数据</span><span class="sxs-lookup"><span data-stu-id="ec10b-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec10b-105">为了帮助确保需求预测的准确性，您必须尽可能多地获得每个物料或物料分配参数的历史需求数据。</span><span class="sxs-lookup"><span data-stu-id="ec10b-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="ec10b-106">如果尚未导入历史需求数据，请使用 Dynamics 365 Supply Chain Management 中 **历史外部需求** (ReqDemPlanHistoricalExternalDemandEntity) 导入它。</span><span class="sxs-lookup"><span data-stu-id="ec10b-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="ec10b-107">在 **数据管理** 工作区，您可以看到实体中所有字段的概览。</span><span class="sxs-lookup"><span data-stu-id="ec10b-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="ec10b-108">打开 **数据管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="ec10b-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="ec10b-109">选择 **数据实体** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="ec10b-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="ec10b-110">搜索实体列表查找 **历史外部需求**。</span><span class="sxs-lookup"><span data-stu-id="ec10b-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="ec10b-111">选择 **目标字段**。</span><span class="sxs-lookup"><span data-stu-id="ec10b-111">Select **Target fields**.</span></span> <span data-ttu-id="ec10b-112">实体以下字段是必需的：站点 (**DeliveringSiteId**)、日期 (**DemandDate**)、数量 (**DemandQuantity**) 和物料编号 (**ItemNumber**) 或物料分配参数 (**ProductAllocationKeyId**)。</span><span class="sxs-lookup"><span data-stu-id="ec10b-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="ec10b-113">若要使用数据实体，您必须有包含历史需求数据的 Microsoft Excel 文件或逗号分隔值 (CSV) 文件。</span><span class="sxs-lookup"><span data-stu-id="ec10b-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="ec10b-114">以下示例显示如何从 CSV 文件导入数据。</span><span class="sxs-lookup"><span data-stu-id="ec10b-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="ec10b-115">有关如何导入数据（包括如何在导入后清理数据）的详细信息，请参阅[数据导入和导出作业概述](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)及其相关主题。</span><span class="sxs-lookup"><span data-stu-id="ec10b-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="ec10b-116">示例</span><span class="sxs-lookup"><span data-stu-id="ec10b-116">Example</span></span>

<span data-ttu-id="ec10b-117">您可以使用以下文件作为示例。</span><span class="sxs-lookup"><span data-stu-id="ec10b-117">You can use the following file as an example.</span></span> <span data-ttu-id="ec10b-118">下载 [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/)。</span><span class="sxs-lookup"><span data-stu-id="ec10b-118">Download the [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/).</span></span> <span data-ttu-id="ec10b-119">此文件包含物料 D0001 的历史需求数据。</span><span class="sxs-lookup"><span data-stu-id="ec10b-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="ec10b-120">它仅包含以下必填字段：站点、数量和需求日期。</span><span class="sxs-lookup"><span data-stu-id="ec10b-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="ec10b-121">选择历史需求数据要导入到的公司。</span><span class="sxs-lookup"><span data-stu-id="ec10b-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="ec10b-122">打开 **数据管理** 工作区。</span><span class="sxs-lookup"><span data-stu-id="ec10b-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="ec10b-123">选择 **导入** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="ec10b-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="ec10b-124">为导入项目输入一个名称，如 **导入物料 D0001 的历史需求**。</span><span class="sxs-lookup"><span data-stu-id="ec10b-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="ec10b-125">在 **源数据格式** 字段中，选择您导入的文件的文件格式。</span><span class="sxs-lookup"><span data-stu-id="ec10b-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="ec10b-126">若要导入此示例的 HistoricalDemandData 文件，选择 **CSV**。</span><span class="sxs-lookup"><span data-stu-id="ec10b-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="ec10b-127">在 **实体名称** 字段，选择 **历史外部需求**。</span><span class="sxs-lookup"><span data-stu-id="ec10b-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="ec10b-128">将文件保存到您的计算机，然后上载。</span><span class="sxs-lookup"><span data-stu-id="ec10b-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="ec10b-129">选择 **导入**。</span><span class="sxs-lookup"><span data-stu-id="ec10b-129">Select **Import**.</span></span>
9. <span data-ttu-id="ec10b-130">**执行汇总** 页自动打开。</span><span class="sxs-lookup"><span data-stu-id="ec10b-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="ec10b-131">验证页面上导入的数据。</span><span class="sxs-lookup"><span data-stu-id="ec10b-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="ec10b-132">在您导入历史需求数据后，可以生成需求预测。</span><span class="sxs-lookup"><span data-stu-id="ec10b-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec10b-133">其他资源</span><span class="sxs-lookup"><span data-stu-id="ec10b-133">Additional resources</span></span>

[<span data-ttu-id="ec10b-134">生成统计基准预测</span><span class="sxs-lookup"><span data-stu-id="ec10b-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="ec10b-135">数据导入和导出作业概览</span><span class="sxs-lookup"><span data-stu-id="ec10b-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]