---
title: "费用报表上的分配"
description: "在支出报表输入费用时，您可以在您的组织中配送多个项目、法人或帐户。"
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8c3eccb686f5577cd55d7ed31e6f1adf3456096a
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="2b4f1-103">费用报表上的分配</span><span class="sxs-lookup"><span data-stu-id="2b4f1-103">Distributions on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b4f1-104">在费用报表输入费用时，您可以在您的组织中配送多个项目、财务维度或帐户。</span><span class="sxs-lookup"><span data-stu-id="2b4f1-104">When you enter expenses on an expense report, you can distribute the expense across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="2b4f1-105">例如，南希，销售代表从法兰克福出差到哥本哈根。</span><span class="sxs-lookup"><span data-stu-id="2b4f1-105">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="2b4f1-106">在法兰克福，她具有两个组织讨论上述每个组织的单独的项目。</span><span class="sxs-lookup"><span data-stu-id="2b4f1-106">In Frankfurt, she met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="2b4f1-107">南希与组织 A 在项目 A 上所用的七个工作日和在组织 B 项目 B 上所用的三个工作日。</span><span class="sxs-lookup"><span data-stu-id="2b4f1-107">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="2b4f1-108">由于南希在法兰克福时从事在两个不同的项目，当她输入支出报表时，她根据需要为每个项目分配相应的费用。</span><span class="sxs-lookup"><span data-stu-id="2b4f1-108">Because Nancy worked on two separate projects when she was in Frankfurt, when she enters her expense report, she distributes her expenses as appropriate for each project.</span></span> <span data-ttu-id="2b4f1-109">下表显示南希如何分配自己的费用。</span><span class="sxs-lookup"><span data-stu-id="2b4f1-109">The following table shows how Nancy distributed her expenses.</span></span>


| <span data-ttu-id="2b4f1-110"><strong>支出类型</strong></span><span class="sxs-lookup"><span data-stu-id="2b4f1-110"><strong>Expense type</strong></span></span> | <span data-ttu-id="2b4f1-111"><strong>支出总金额</strong></span><span class="sxs-lookup"><span data-stu-id="2b4f1-111"><strong>Total expense amount</strong></span></span> | <span data-ttu-id="2b4f1-112"><strong>金额已分配到项目 A。</strong></span><span class="sxs-lookup"><span data-stu-id="2b4f1-112"><strong>Amount distributed to project A</strong></span></span> | <span data-ttu-id="2b4f1-113"><strong>金额已分配到项目 B。</strong></span><span class="sxs-lookup"><span data-stu-id="2b4f1-113"><strong>Amount distributed to project B</strong></span></span> |
|-------------------------------|---------------------------------------|--------------------------------------------------|--------------------------------------------------|
|          <span data-ttu-id="2b4f1-114">火车票价</span><span class="sxs-lookup"><span data-stu-id="2b4f1-114">Train fare</span></span>           |                <span data-ttu-id="2b4f1-115">DKK 578</span><span class="sxs-lookup"><span data-stu-id="2b4f1-115">DKK 578</span></span>                |                     <span data-ttu-id="2b4f1-116">DKK 405</span><span class="sxs-lookup"><span data-stu-id="2b4f1-116">DKK 405</span></span>                      |                     <span data-ttu-id="2b4f1-117">DKK 173</span><span class="sxs-lookup"><span data-stu-id="2b4f1-117">DKK 173</span></span>                      |
|             <span data-ttu-id="2b4f1-118">酒店</span><span class="sxs-lookup"><span data-stu-id="2b4f1-118">Hotel</span></span>             |                <span data-ttu-id="2b4f1-119">725 欧元</span><span class="sxs-lookup"><span data-stu-id="2b4f1-119">EUR 725</span></span>                |                     <span data-ttu-id="2b4f1-120">557 欧元</span><span class="sxs-lookup"><span data-stu-id="2b4f1-120">EUR 557</span></span>                      |                     <span data-ttu-id="2b4f1-121">168 欧元</span><span class="sxs-lookup"><span data-stu-id="2b4f1-121">EUR 168</span></span>                      |
|             <span data-ttu-id="2b4f1-122">餐费</span><span class="sxs-lookup"><span data-stu-id="2b4f1-122">Meals</span></span>             |                <span data-ttu-id="2b4f1-123">346 欧元</span><span class="sxs-lookup"><span data-stu-id="2b4f1-123">EUR 346</span></span>                |                     <span data-ttu-id="2b4f1-124">284 欧元</span><span class="sxs-lookup"><span data-stu-id="2b4f1-124">EUR 284</span></span>                      |                      <span data-ttu-id="2b4f1-125">62 欧元</span><span class="sxs-lookup"><span data-stu-id="2b4f1-125">EUR 62</span></span>                      |


