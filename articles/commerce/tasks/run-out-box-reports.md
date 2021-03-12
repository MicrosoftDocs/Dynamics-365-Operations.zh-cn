---
title: 生成和运行现成报表
description: 可使用此任务指南运行不同工作区中总部的现成报表和“商业”中的“查询和销售“报表。
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e11bca1e6850f401f52c2ccbea1089a4e71591c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003695"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="f3001-103">生成和运行现成报表</span><span class="sxs-lookup"><span data-stu-id="f3001-103">Generate and run out of box reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3001-104">可使用此任务指南运行不同工作区中总部的现成报表和“商业”中的“查询和销售“报表。</span><span class="sxs-lookup"><span data-stu-id="f3001-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="f3001-105">创建此记录时使用的演示数据公司为 USRT。</span><span class="sxs-lookup"><span data-stu-id="f3001-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="f3001-106">此录制专门面向系统管理员角色。</span><span class="sxs-lookup"><span data-stu-id="f3001-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="f3001-107">启动工作区中的报表</span><span class="sxs-lookup"><span data-stu-id="f3001-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="f3001-108">转至“Retail 和 Commerce”>“产品和类别”>“类别和产品管理”。</span><span class="sxs-lookup"><span data-stu-id="f3001-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="f3001-109">单击此箭头可展开或折叠“报表”部分。</span><span class="sxs-lookup"><span data-stu-id="f3001-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="f3001-110">单击“排名靠前的产品报表”。</span><span class="sxs-lookup"><span data-stu-id="f3001-110">Click Top products report.</span></span>
4. <span data-ttu-id="f3001-111">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="f3001-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="f3001-112">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="f3001-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="f3001-113">在“渠道”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f3001-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f3001-114">在树结构中，请选择“Contoso Retail\Contoso Retail USA\中心\休斯顿”。</span><span class="sxs-lookup"><span data-stu-id="f3001-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="f3001-115">这会显示“商业报告”目的的默认组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="f3001-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="f3001-116">转至“组织管理”>“组织”>“组织层次结构目的”，选择“商业报告”，然后在“已分配层次结构”下，选中“默认”列已选中的层次结构名称。</span><span class="sxs-lookup"><span data-stu-id="f3001-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="f3001-117">作为演示数据的一部分（用于此任务录制），您会注意到，“商店(按地区)”是报告目的的默认组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="f3001-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="f3001-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f3001-118">Click OK.</span></span>
9. <span data-ttu-id="f3001-119">在“视图”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f3001-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="f3001-120">在“依据”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f3001-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="f3001-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f3001-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="f3001-122">从查询和销售报表中启动报表</span><span class="sxs-lookup"><span data-stu-id="f3001-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="f3001-123">转至“Retail 和 Commerce”>“查询和报表”>“销售报表”>“类别销售报表”。</span><span class="sxs-lookup"><span data-stu-id="f3001-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="f3001-124">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="f3001-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="f3001-125">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="f3001-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="f3001-126">在“渠道”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="f3001-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f3001-127">在树结构中，请选择“Contoso Retail\Contoso Retail USA\西部\西雅图”。</span><span class="sxs-lookup"><span data-stu-id="f3001-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="f3001-128">这会显示“商业报告”目的的默认组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="f3001-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="f3001-129">转至“组织管理”>“组织”>“组织层次结构目的”，选择“商业报告”，然后在“已分配层次结构”下，选中“默认”列已选中的层次结构名称。</span><span class="sxs-lookup"><span data-stu-id="f3001-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="f3001-130">作为演示数据的一部分（用于此任务录制），您会注意到，“商店(按地区)”是报告目的的默认组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="f3001-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="f3001-131">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f3001-131">Click OK.</span></span>
7. <span data-ttu-id="f3001-132">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f3001-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="f3001-133">导出 HQ 报表</span><span class="sxs-lookup"><span data-stu-id="f3001-133">Export an HQ reports</span></span>
1. <span data-ttu-id="f3001-134">转至“Retail 和 Commerce”>“查询和报表”>“销售报表”>“组织销售报表”。</span><span class="sxs-lookup"><span data-stu-id="f3001-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="f3001-135">在“开始日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="f3001-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="f3001-136">在“结束日期”字段中输入日期。</span><span class="sxs-lookup"><span data-stu-id="f3001-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="f3001-137">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f3001-137">Click OK.</span></span>
5. <span data-ttu-id="f3001-138">单击“导出”。</span><span class="sxs-lookup"><span data-stu-id="f3001-138">Click Export.</span></span>
6. <span data-ttu-id="f3001-139">单击 PDF。</span><span class="sxs-lookup"><span data-stu-id="f3001-139">Click PDF.</span></span>

