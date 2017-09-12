--- 
title: "创建带范围的利息代码"
description: "可以设置利息代码，根据值范围以计算不同的利息金额。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 05ca41dd5d660e9f0ef72ee5bd49d800645081a5
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="b467a-103">创建带范围的利息代码</span><span class="sxs-lookup"><span data-stu-id="b467a-103">Create an interest code with a range</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b467a-104">可以设置利息代码，根据值范围以计算不同的利息金额。</span><span class="sxs-lookup"><span data-stu-id="b467a-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="b467a-105">该过程将向您显示如何添加利息代码和范围。</span><span class="sxs-lookup"><span data-stu-id="b467a-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="b467a-106">转到“信贷和收款”>“利息”>“设置利息代码”。</span><span class="sxs-lookup"><span data-stu-id="b467a-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="b467a-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b467a-107">Click New.</span></span>
3. <span data-ttu-id="b467a-108">在“利息代码”字段，输入利息代码名称。</span><span class="sxs-lookup"><span data-stu-id="b467a-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="b467a-109">在“描述”字段，输入利息代码的描述。</span><span class="sxs-lookup"><span data-stu-id="b467a-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="b467a-110">选择“月份”。</span><span class="sxs-lookup"><span data-stu-id="b467a-110">Select Month.</span></span>
6. <span data-ttu-id="b467a-111">展开“收益”部分。</span><span class="sxs-lookup"><span data-stu-id="b467a-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="b467a-112">展开“原币收益”部分。</span><span class="sxs-lookup"><span data-stu-id="b467a-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="b467a-113">在“分类帐过帐帐户”字段中，指定所需值。</span><span class="sxs-lookup"><span data-stu-id="b467a-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="b467a-114">在“范围利息”字段，选择“月份”。</span><span class="sxs-lookup"><span data-stu-id="b467a-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="b467a-115">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="b467a-115">Click Add.</span></span>
11. <span data-ttu-id="b467a-116">在“描述”字段中，输入货币和范围的描述。</span><span class="sxs-lookup"><span data-stu-id="b467a-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="b467a-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="b467a-117">Click Save.</span></span>
13. <span data-ttu-id="b467a-118">单击“范围”。</span><span class="sxs-lookup"><span data-stu-id="b467a-118">Click Ranges.</span></span>
14. <span data-ttu-id="b467a-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b467a-119">Click New.</span></span>
15. <span data-ttu-id="b467a-120">在“开始值”中输入 0，然后输入将用于计算利息的月利息百分比。</span><span class="sxs-lookup"><span data-stu-id="b467a-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="b467a-121">示例：开始值为 1.5。</span><span class="sxs-lookup"><span data-stu-id="b467a-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="b467a-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b467a-122">Click New.</span></span>
17. <span data-ttu-id="b467a-123">输入“下一开始值”为 4，是您将计算新的利息金额的第一个月。</span><span class="sxs-lookup"><span data-stu-id="b467a-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="b467a-124">输入将用于计算月份 4 后的月利息百分比。</span><span class="sxs-lookup"><span data-stu-id="b467a-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="b467a-125">在本示例中，为 2.0。</span><span class="sxs-lookup"><span data-stu-id="b467a-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="b467a-126">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="b467a-126">Click New.</span></span>
20. <span data-ttu-id="b467a-127">输入“下一开始值”为 7，是计算新的利息金额的下一个月。</span><span class="sxs-lookup"><span data-stu-id="b467a-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="b467a-128">输入将用于计算月份 7 后的月利息百分比。</span><span class="sxs-lookup"><span data-stu-id="b467a-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="b467a-129">在本示例中，为 2.5。</span><span class="sxs-lookup"><span data-stu-id="b467a-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="b467a-130">单击“关闭”以完成设置。</span><span class="sxs-lookup"><span data-stu-id="b467a-130">Click Close to complete the setup.</span></span>


