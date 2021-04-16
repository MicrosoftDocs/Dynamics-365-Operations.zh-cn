---
title: 财务报表设计器中的报表定义
description: 本文提供了有关报表定义的信息。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52322453328814b06bacefb4829bb10bf9953186
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755436"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="87488-103">财务报表设计器中的报表定义</span><span class="sxs-lookup"><span data-stu-id="87488-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87488-104">本文提供了有关报表定义的信息。</span><span class="sxs-lookup"><span data-stu-id="87488-104">This article provides information about report definitions.</span></span> <span data-ttu-id="87488-105">报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。</span><span class="sxs-lookup"><span data-stu-id="87488-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="87488-106">报表定义还提供自定义报表的选项和设置。</span><span class="sxs-lookup"><span data-stu-id="87488-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="87488-107">报表定义是使用行定义、列定义和可选报告结构树定义创建报表的报表组件（或构建基块）。</span><span class="sxs-lookup"><span data-stu-id="87488-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="87488-108">报表定义还提供了可用于自定义报表的选项和设置。</span><span class="sxs-lookup"><span data-stu-id="87488-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="87488-109">在定义行定义和列定义之后，必须在报表定义中合并这些定义。</span><span class="sxs-lookup"><span data-stu-id="87488-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="87488-110">此时，您还将定义定义的其他方面，如详细程度和报表日期。</span><span class="sxs-lookup"><span data-stu-id="87488-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="87488-111">然后您可保存和生成报表。</span><span class="sxs-lookup"><span data-stu-id="87488-111">You can then save and generate a report.</span></span> <span data-ttu-id="87488-112">财务报告提供下列详细级别：</span><span class="sxs-lookup"><span data-stu-id="87488-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="87488-113">财务</span><span class="sxs-lookup"><span data-stu-id="87488-113">Financial</span></span>
- <span data-ttu-id="87488-114">财务和科目</span><span class="sxs-lookup"><span data-stu-id="87488-114">Financial and Account</span></span>
- <span data-ttu-id="87488-115">财务、科目和交易记录</span><span class="sxs-lookup"><span data-stu-id="87488-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="87488-116">但是，根据数据在 Microsoft Dynamics ERP 系统中的存储方式，可能无法在报表中使用交易记录明细。</span><span class="sxs-lookup"><span data-stu-id="87488-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="87488-117">创建报表定义</span><span class="sxs-lookup"><span data-stu-id="87488-117">Create a report definition</span></span>
1. <span data-ttu-id="87488-118">在报表设计器的 **文件** 菜单上，单击 **新建**，然后选择 **报表定义**。</span><span class="sxs-lookup"><span data-stu-id="87488-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="87488-119">在 **报表**、**输出和分配**、**页眉和页脚** 以及 **设置** 选项卡上指定相应信息。</span><span class="sxs-lookup"><span data-stu-id="87488-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="87488-120">报表定义的内容</span><span class="sxs-lookup"><span data-stu-id="87488-120">Contents of a report definition</span></span>
<span data-ttu-id="87488-121">下表说明了报表定义中的各个选项卡以及如何使用这些信息。</span><span class="sxs-lookup"><span data-stu-id="87488-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="87488-122">选项卡</span><span class="sxs-lookup"><span data-stu-id="87488-122">Tab</span></span></th>
<th><span data-ttu-id="87488-123">说明</span><span class="sxs-lookup"><span data-stu-id="87488-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="87488-124">报表</span><span class="sxs-lookup"><span data-stu-id="87488-124">Report</span></span></td>
<td><span data-ttu-id="87488-125">创建报表、配置报表或修改现有报表。</span><span class="sxs-lookup"><span data-stu-id="87488-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87488-126">输出和分发</span><span class="sxs-lookup"><span data-stu-id="87488-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="87488-127">更改报表的输出类型和目标。</span><span class="sxs-lookup"><span data-stu-id="87488-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87488-128">页眉和页脚</span><span class="sxs-lookup"><span data-stu-id="87488-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="87488-129">定义报表的页眉和页脚并设置其格式。</span><span class="sxs-lookup"><span data-stu-id="87488-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="87488-130">例如，您可向页眉或页脚添加文本或图像。</span><span class="sxs-lookup"><span data-stu-id="87488-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="87488-131">对于图像，财务报告支持 .bmp、.jpg 和 .png 文件。</span><span class="sxs-lookup"><span data-stu-id="87488-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="87488-132">您还可添加自动图文集代码以插入其他信息（如公司名称、报表名称或页码）。</span><span class="sxs-lookup"><span data-stu-id="87488-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="87488-133">设置</span><span class="sxs-lookup"><span data-stu-id="87488-133">Settings</span></span></td>
<td><span data-ttu-id="87488-134">指定报表定义设置，例如以下设置：</span><span class="sxs-lookup"><span data-stu-id="87488-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="87488-135">金额格式和化整金额</span><span class="sxs-lookup"><span data-stu-id="87488-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="87488-136">设置明细报表的格式</span><span class="sxs-lookup"><span data-stu-id="87488-136">Format detail reports</span></span></li>
<li><span data-ttu-id="87488-137">设置报告树的格式</span><span class="sxs-lookup"><span data-stu-id="87488-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="87488-138">生成异常报表</span><span class="sxs-lookup"><span data-stu-id="87488-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="87488-139">指定币种转换</span><span class="sxs-lookup"><span data-stu-id="87488-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="87488-140">小计和筛选会计科目明细</span><span class="sxs-lookup"><span data-stu-id="87488-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="87488-141">其他资源</span><span class="sxs-lookup"><span data-stu-id="87488-141">Additional resources</span></span>

[<span data-ttu-id="87488-142">财务申报</span><span class="sxs-lookup"><span data-stu-id="87488-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]