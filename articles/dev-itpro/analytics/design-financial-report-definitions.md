---
title: "财务报表设计器中的报表定义"
description: "本文提供了有关报表定义的信息。 报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。 报表定义还提供自定义报表的选项和设置。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: e16471e6570989b678b1856a8199796084c38bc7
ms.contentlocale: zh-cn
ms.lasthandoff: 01/19/2018

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="00528-105">财务报表设计器中的报表定义</span><span class="sxs-lookup"><span data-stu-id="00528-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="00528-106">本文提供了有关报表定义的信息。</span><span class="sxs-lookup"><span data-stu-id="00528-106">This article provides information about report definitions.</span></span> <span data-ttu-id="00528-107">报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。</span><span class="sxs-lookup"><span data-stu-id="00528-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="00528-108">报表定义还提供自定义报表的选项和设置。</span><span class="sxs-lookup"><span data-stu-id="00528-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="00528-109">报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。</span><span class="sxs-lookup"><span data-stu-id="00528-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="00528-110">报表定义还提供了可用于自定义报表的选项和设置。</span><span class="sxs-lookup"><span data-stu-id="00528-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="00528-111">在定义行定义和列定义之后，必须在报表定义中合并这些定义。</span><span class="sxs-lookup"><span data-stu-id="00528-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="00528-112">此时，您还将定义定义的其他方面，如详细程度和报表日期。</span><span class="sxs-lookup"><span data-stu-id="00528-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="00528-113">然后您可保存和生成报表。</span><span class="sxs-lookup"><span data-stu-id="00528-113">You can then save and generate a report.</span></span> <span data-ttu-id="00528-114">财务报告提供下列详细级别：</span><span class="sxs-lookup"><span data-stu-id="00528-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="00528-115">财务</span><span class="sxs-lookup"><span data-stu-id="00528-115">Financial</span></span>
-   <span data-ttu-id="00528-116">财务和科目</span><span class="sxs-lookup"><span data-stu-id="00528-116">Financial and Account</span></span>
-   <span data-ttu-id="00528-117">财务、科目和交易记录</span><span class="sxs-lookup"><span data-stu-id="00528-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="00528-118">但是，根据数据在 Microsoft Dynamics ERP 系统中的存储方式，可能无法在报表中使用交易记录明细。</span><span class="sxs-lookup"><span data-stu-id="00528-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="00528-119">创建报表定义</span><span class="sxs-lookup"><span data-stu-id="00528-119">Create a report definition</span></span>
1.  <span data-ttu-id="00528-120">在报表设计器的**“文件”**菜单上，单击**“新建”**，然后选择**“报表定义”**。</span><span class="sxs-lookup"><span data-stu-id="00528-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="00528-121">在**“报表”**、**“输出和分配”**、**“页眉和页脚”**以及**“设置”**选项卡上指定相应信息。</span><span class="sxs-lookup"><span data-stu-id="00528-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="00528-122">报表定义的内容</span><span class="sxs-lookup"><span data-stu-id="00528-122">Contents of a report definition</span></span>
<span data-ttu-id="00528-123">下表说明了报表定义中的各个选项卡以及如何使用这些信息。</span><span class="sxs-lookup"><span data-stu-id="00528-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00528-124">选项卡</span><span class="sxs-lookup"><span data-stu-id="00528-124">Tab</span></span></th>
<th><span data-ttu-id="00528-125">说明</span><span class="sxs-lookup"><span data-stu-id="00528-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00528-126">报表</span><span class="sxs-lookup"><span data-stu-id="00528-126">Report</span></span></td>
<td><span data-ttu-id="00528-127">创建报表、配置报表或修改现有报表。</span><span class="sxs-lookup"><span data-stu-id="00528-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00528-128">输出和分发</span><span class="sxs-lookup"><span data-stu-id="00528-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="00528-129">更改报表的输出类型和目标。</span><span class="sxs-lookup"><span data-stu-id="00528-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00528-130">页眉和页脚</span><span class="sxs-lookup"><span data-stu-id="00528-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="00528-131">定义报表的页眉和页脚并设置其格式。</span><span class="sxs-lookup"><span data-stu-id="00528-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="00528-132">例如，您可向页眉或页脚添加文本或图像。</span><span class="sxs-lookup"><span data-stu-id="00528-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="00528-133">对于图像，财务报告支持 .bmp、.jpg 和 .png 文件。</span><span class="sxs-lookup"><span data-stu-id="00528-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="00528-134">您还可添加自动图文集代码以插入其他信息（如公司名称、报表名称或页码）。</span><span class="sxs-lookup"><span data-stu-id="00528-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00528-135">设置</span><span class="sxs-lookup"><span data-stu-id="00528-135">Settings</span></span></td>
<td><span data-ttu-id="00528-136">指定报表定义设置，例如以下设置：</span><span class="sxs-lookup"><span data-stu-id="00528-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="00528-137">金额格式和舍入金额</span><span class="sxs-lookup"><span data-stu-id="00528-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="00528-138">设置明细报表的格式</span><span class="sxs-lookup"><span data-stu-id="00528-138">Format detail reports</span></span></li>
<li><span data-ttu-id="00528-139">设置报告树的格式</span><span class="sxs-lookup"><span data-stu-id="00528-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="00528-140">生成异常报表</span><span class="sxs-lookup"><span data-stu-id="00528-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="00528-141">指定货币转换</span><span class="sxs-lookup"><span data-stu-id="00528-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="00528-142">对科目详细信息进行小计和筛选</span><span class="sxs-lookup"><span data-stu-id="00528-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="00528-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="00528-143">See also</span></span>
--------

[<span data-ttu-id="00528-144">财务申报</span><span class="sxs-lookup"><span data-stu-id="00528-144">Financial reporting</span></span>](financial-reporting-intro.md)




