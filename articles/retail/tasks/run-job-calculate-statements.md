--- 
title: "配置和运行计算报表作业"
description: "此程序会逐步演示如何配置和运行重复批处理作业，以创建和计算选定商店或商店组的报表。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: f41f19ef5610de3b9b9f0ad30e7f0546173f8fbc
ms.contentlocale: zh-cn
ms.lasthandoff: 01/19/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="8abd0-103">配置和运行计算报表作业</span><span class="sxs-lookup"><span data-stu-id="8abd0-103">Configure and run a job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8abd0-104">此程序会逐步演示如何配置和运行重复批处理作业，以创建和计算选定商店或商店组的报表。</span><span class="sxs-lookup"><span data-stu-id="8abd0-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="8abd0-105">此程序使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="8abd0-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8abd0-106">转至“所有工作区”>“零售商店财务”。</span><span class="sxs-lookup"><span data-stu-id="8abd0-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="8abd0-107">单击“计算报表”。</span><span class="sxs-lookup"><span data-stu-id="8abd0-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="8abd0-108">如果您想要为一组商店创建批处理作业，选择一个特定商店或一个节点。</span><span class="sxs-lookup"><span data-stu-id="8abd0-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="8abd0-109">单击箭头以添加您的选择。</span><span class="sxs-lookup"><span data-stu-id="8abd0-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="8abd0-110">单击“后台运行”选项卡。</span><span class="sxs-lookup"><span data-stu-id="8abd0-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="8abd0-111">在“批处理”之下，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="8abd0-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="8abd0-112">单击“再循环”。</span><span class="sxs-lookup"><span data-stu-id="8abd0-112">Click Recurrence.</span></span>
6. <span data-ttu-id="8abd0-113">在“开始日期”字段中，输入一个日期。</span><span class="sxs-lookup"><span data-stu-id="8abd0-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="8abd0-114">在“开始时间”字段中，输入时间。</span><span class="sxs-lookup"><span data-stu-id="8abd0-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="8abd0-115">选择“无结束日期”选项。</span><span class="sxs-lookup"><span data-stu-id="8abd0-115">Select the No end date option.</span></span>
9. <span data-ttu-id="8abd0-116">在“PatternUnit”字段中，输入“天数”。</span><span class="sxs-lookup"><span data-stu-id="8abd0-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="8abd0-117">在“每”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="8abd0-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="8abd0-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8abd0-118">Click OK.</span></span>
12. <span data-ttu-id="8abd0-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="8abd0-119">Click OK.</span></span>


