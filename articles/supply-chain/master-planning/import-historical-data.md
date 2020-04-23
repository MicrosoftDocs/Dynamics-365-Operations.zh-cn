---
title: 导入需求预测的历史数据
description: 若要获取准确的需求预测，您需要每个物料或物料分配参数的历史需求数据。 本主题说明如何使用数据实体从任何一个系统导入历史需求数据，以便您具有需求预测数据的更长历史记录。
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97e84b478b8fd65313d8c3be5c9a50756d8b4924
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213829"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="d401a-104">导入需求预测的历史数据</span><span class="sxs-lookup"><span data-stu-id="d401a-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d401a-105">为了帮助确保需求预测的准确性，您必须尽可能多地获得每个物料或物料分配参数的历史需求数据。</span><span class="sxs-lookup"><span data-stu-id="d401a-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="d401a-106">如果尚未导入历史需求数据，请使用 Dynamics 365 Supply Chain Management 中**历史外部需求** (ReqDemPlanHistoricalExternalDemandEntity) 导入它。</span><span class="sxs-lookup"><span data-stu-id="d401a-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="d401a-107">在**数据管理**工作区，您可以看到实体中所有字段的概览。</span><span class="sxs-lookup"><span data-stu-id="d401a-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="d401a-108">打开**数据管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="d401a-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="d401a-109">单击**数据实体**磁贴。</span><span class="sxs-lookup"><span data-stu-id="d401a-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="d401a-110">搜索实体列表查找**历史外部需求**。</span><span class="sxs-lookup"><span data-stu-id="d401a-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="d401a-111">单击**目标字段**。</span><span class="sxs-lookup"><span data-stu-id="d401a-111">Click **Target fields**.</span></span> <span data-ttu-id="d401a-112">实体以下字段是必需的：站点 (**DeliveringSiteId**)、日期 (**DemandDate**)、数量 (**DemandQuantity**) 和物料编号 (**ItemNumber**) 或物料分配参数 (**ProductAllocationKeyId**)。</span><span class="sxs-lookup"><span data-stu-id="d401a-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="d401a-113">若要使用数据实体，您必须有包含历史需求数据的 Microsoft Excel 文件或逗号分隔值 (CSV) 文件。</span><span class="sxs-lookup"><span data-stu-id="d401a-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="d401a-114">以下示例显示如何从 CSV 文件导入数据。</span><span class="sxs-lookup"><span data-stu-id="d401a-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="d401a-115">示例</span><span class="sxs-lookup"><span data-stu-id="d401a-115">Example</span></span>

<span data-ttu-id="d401a-116">您可以使用以下文件作为示例。</span><span class="sxs-lookup"><span data-stu-id="d401a-116">You can use the following file as an example.</span></span> <span data-ttu-id="d401a-117">下载 [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast)。</span><span class="sxs-lookup"><span data-stu-id="d401a-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="d401a-118">此文件包含物料 D0001 的历史需求数据。</span><span class="sxs-lookup"><span data-stu-id="d401a-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="d401a-119">它仅包含以下必填字段：站点、数量和需求日期。</span><span class="sxs-lookup"><span data-stu-id="d401a-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="d401a-120">选择历史需求数据要导入到的公司。</span><span class="sxs-lookup"><span data-stu-id="d401a-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="d401a-121">打开**数据管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="d401a-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="d401a-122">单击**导入**磁贴。</span><span class="sxs-lookup"><span data-stu-id="d401a-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="d401a-123">为导入项目输入一个名称，如**导入物料 D0001 的历史需求**。</span><span class="sxs-lookup"><span data-stu-id="d401a-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="d401a-124">在**源数据格式**字段中，选择您导入的文件的文件格式。</span><span class="sxs-lookup"><span data-stu-id="d401a-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="d401a-125">若要导入此示例的 HistoricalDemandData 文件，选择 **CSV**。</span><span class="sxs-lookup"><span data-stu-id="d401a-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="d401a-126">在**实体名称**字段，选择**历史外部需求**。</span><span class="sxs-lookup"><span data-stu-id="d401a-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="d401a-127">将文件保存到您的计算机，然后上载。</span><span class="sxs-lookup"><span data-stu-id="d401a-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="d401a-128">单击**导入**。</span><span class="sxs-lookup"><span data-stu-id="d401a-128">Click **Import**.</span></span>
9. <span data-ttu-id="d401a-129">**执行汇总**页自动打开。</span><span class="sxs-lookup"><span data-stu-id="d401a-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="d401a-130">验证页面上导入的数据。</span><span class="sxs-lookup"><span data-stu-id="d401a-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="d401a-131">在您导入历史需求数据后，可以生成需求预测。</span><span class="sxs-lookup"><span data-stu-id="d401a-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d401a-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="d401a-132">Additional resources</span></span>

[<span data-ttu-id="d401a-133">生成统计基准预测</span><span class="sxs-lookup"><span data-stu-id="d401a-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
