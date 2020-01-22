---
title: 分析报告未更新
description: 本主题说明如果客户的数据更改不出现在任何客户的工作区时该怎么做。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fc2e6259a8f9d17dc0f7652f207acfa53da76a8d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898565"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="bb032-103">分析报告未更新</span><span class="sxs-lookup"><span data-stu-id="bb032-103">Analytic reports are not updated</span></span>

<span data-ttu-id="bb032-104">**发货**</span><span class="sxs-lookup"><span data-stu-id="bb032-104">**Issue**</span></span>

<span data-ttu-id="bb032-105">客户的数据更改不出现在任何客户的工作区的**分析**选项卡。</span><span class="sxs-lookup"><span data-stu-id="bb032-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="bb032-106">**原因**</span><span class="sxs-lookup"><span data-stu-id="bb032-106">**Cause**</span></span>

<span data-ttu-id="bb032-107">默认情况下，Microsoft Power BI 报表根据部署度量批处理作业的计划每四小时刷新一次。</span><span class="sxs-lookup"><span data-stu-id="bb032-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="bb032-108">**分辨率**</span><span class="sxs-lookup"><span data-stu-id="bb032-108">**Resolution**</span></span>

<span data-ttu-id="bb032-109">此问题可能只是时间问题。</span><span class="sxs-lookup"><span data-stu-id="bb032-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="bb032-110">请执行以下步骤开始批处理作业并更新分析工作区。</span><span class="sxs-lookup"><span data-stu-id="bb032-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="bb032-111">在**系统管理 \> 链接 \> 批处理作业 \> 批处理作业**打开**批处理作业**页。</span><span class="sxs-lookup"><span data-stu-id="bb032-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="bb032-112">或者，使用“搜索”，输入**批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="bb032-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="bb032-113">在列表中查找**部署度量**作业。</span><span class="sxs-lookup"><span data-stu-id="bb032-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="bb032-114">选择该页顶部的**编辑**，将计划的开始日期/时间设置为将刷新更接近当前时间的分析的值。</span><span class="sxs-lookup"><span data-stu-id="bb032-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![批处理作业](media/batch-jobs.png)
