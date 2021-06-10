---
title: 分析报告疑难解答
description: 本文说明如果客户的数据更改不出现在任何客户的工作区时该怎么做。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8dab12213e9730e72aede70c5b5d1368ef77664e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053531"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="69d8f-103">分析报告疑难解答</span><span class="sxs-lookup"><span data-stu-id="69d8f-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="69d8f-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="69d8f-104">**Issue**</span></span>

<span data-ttu-id="69d8f-105">客户的数据更改不出现在任何客户的工作区的 **分析** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="69d8f-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="69d8f-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="69d8f-106">**Cause**</span></span>

<span data-ttu-id="69d8f-107">默认情况下，Microsoft Power BI 报表根据部署度量批处理作业的计划每四小时刷新一次。</span><span class="sxs-lookup"><span data-stu-id="69d8f-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="69d8f-108">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="69d8f-108">**Resolution**</span></span>

<span data-ttu-id="69d8f-109">此问题可能只是时间问题。</span><span class="sxs-lookup"><span data-stu-id="69d8f-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="69d8f-110">请执行以下步骤开始批处理作业并更新分析工作区。</span><span class="sxs-lookup"><span data-stu-id="69d8f-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="69d8f-111">在 **系统管理 \> 链接 \> 批处理作业 \> 批处理作业** 打开 **批处理作业** 页。</span><span class="sxs-lookup"><span data-stu-id="69d8f-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="69d8f-112">或者，使用“搜索”，输入 **批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="69d8f-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="69d8f-113">在列表中查找 **部署度量** 作业。</span><span class="sxs-lookup"><span data-stu-id="69d8f-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="69d8f-114">选择该页顶部的 **编辑**，将计划的开始日期/时间设置为将刷新更接近当前时间的分析的值。</span><span class="sxs-lookup"><span data-stu-id="69d8f-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![批处理作业](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]