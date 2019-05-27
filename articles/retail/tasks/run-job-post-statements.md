---
title: 配置和运行作业以过帐报表
description: 此程序会逐步演示如何配置和运行某一重复批处理作业，以过帐选定商店或商店组的报表。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550108"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="d6c41-103">配置和运行作业以过帐报表</span><span class="sxs-lookup"><span data-stu-id="d6c41-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d6c41-104">此程序会逐步演示如何配置和运行某一重复批处理作业，以过帐选定商店或商店组的报表。</span><span class="sxs-lookup"><span data-stu-id="d6c41-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="d6c41-105">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="d6c41-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d6c41-106">转至“所有工作区”></span><span class="sxs-lookup"><span data-stu-id="d6c41-106">Go to All workspaces > ..</span></span> <span data-ttu-id="d6c41-107">>“零售商店财务”。</span><span class="sxs-lookup"><span data-stu-id="d6c41-107">> Retail store financials.</span></span>
2. <span data-ttu-id="d6c41-108">单击“对报表过帐”。</span><span class="sxs-lookup"><span data-stu-id="d6c41-108">Click Post statements.</span></span>
    * <span data-ttu-id="d6c41-109">选择一个组织层次结构，然后在组织节点树结构中，选择一个商店或节点。</span><span class="sxs-lookup"><span data-stu-id="d6c41-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="d6c41-110">如果您想要为一组商店创建批处理作业，选择一个节点。</span><span class="sxs-lookup"><span data-stu-id="d6c41-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="d6c41-111">单击箭头以添加您的选择。</span><span class="sxs-lookup"><span data-stu-id="d6c41-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="d6c41-112">单击“后台运行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="d6c41-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="d6c41-113">选中或取消选中“批处理”复选框。</span><span class="sxs-lookup"><span data-stu-id="d6c41-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="d6c41-114">单击“再循环”。</span><span class="sxs-lookup"><span data-stu-id="d6c41-114">Click Recurrence.</span></span>
6. <span data-ttu-id="d6c41-115">在“开始日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="d6c41-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="d6c41-116">在“开始时间”字段中，输入时间。</span><span class="sxs-lookup"><span data-stu-id="d6c41-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="d6c41-117">选择您是否想要在特定运行数量或特定日期之后结束重复，或从不结束重复。</span><span class="sxs-lookup"><span data-stu-id="d6c41-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="d6c41-118">然后选择不同选项，以定义您希望作业的运行频率是什么。</span><span class="sxs-lookup"><span data-stu-id="d6c41-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="d6c41-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d6c41-119">Click OK.</span></span>
9. <span data-ttu-id="d6c41-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d6c41-120">Click OK.</span></span>

