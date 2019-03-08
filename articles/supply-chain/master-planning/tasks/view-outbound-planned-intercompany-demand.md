---
title: 查看传出计划内部公司需求
description: 此过程显示如何查看内部公司供应商将满足的所有计划订单。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e0e3a4613e5598e725c475c7dff7662bf4169a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "333706"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="eab9d-103">查看传出计划内部公司需求</span><span class="sxs-lookup"><span data-stu-id="eab9d-103">View outbound planned intercompany demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eab9d-104">此过程显示如何查看内部公司供应商将满足的所有计划订单。</span><span class="sxs-lookup"><span data-stu-id="eab9d-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="eab9d-105">用于创建此过程的演示数据公司是 DEMF。</span><span class="sxs-lookup"><span data-stu-id="eab9d-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="eab9d-106">单击“主计划”。</span><span class="sxs-lookup"><span data-stu-id="eab9d-106">Click Master planning.</span></span>
2. <span data-ttu-id="eab9d-107">在“计划”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="eab9d-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="eab9d-108">在“计划”字段中，选择计划 10。</span><span class="sxs-lookup"><span data-stu-id="eab9d-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="eab9d-109">单击“运行”。</span><span class="sxs-lookup"><span data-stu-id="eab9d-109">Click Run.</span></span>
4. <span data-ttu-id="eab9d-110">在“线程数”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="eab9d-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="eab9d-111">这表示要用于主计划的并行线程数。</span><span class="sxs-lookup"><span data-stu-id="eab9d-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="eab9d-112">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="eab9d-112">Click OK.</span></span>
    * <span data-ttu-id="eab9d-113">这可能需要花费一段时间。</span><span class="sxs-lookup"><span data-stu-id="eab9d-113">This may take a while.</span></span>  
6. <span data-ttu-id="eab9d-114">单击“计划内部公司需求”。</span><span class="sxs-lookup"><span data-stu-id="eab9d-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="eab9d-115">单击“传出计划内部公司需求”。</span><span class="sxs-lookup"><span data-stu-id="eab9d-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="eab9d-116">此页提供内部供应商提供商满足的所有计划需求的概览。</span><span class="sxs-lookup"><span data-stu-id="eab9d-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="eab9d-117">展开"上游需求详细信息"部分。</span><span class="sxs-lookup"><span data-stu-id="eab9d-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="eab9d-118">在此部分中，可以看到有关如何满足需求的详细信息。</span><span class="sxs-lookup"><span data-stu-id="eab9d-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="eab9d-119">可能需要先等待供应公司中运行主计划，才能在此处看到更多信息。</span><span class="sxs-lookup"><span data-stu-id="eab9d-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

