---
title: 配置信用卡处理
description: 此程序会逐步演示如何查看付款提供商列表，以及如何配置应收账款的付款帐户。
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d75ff895c252bfd4f70f8bcc4c4adece585d9a22
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548477"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="6629b-103">配置信用卡处理</span><span class="sxs-lookup"><span data-stu-id="6629b-103">Configure credit card processing</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6629b-104">此程序会逐步演示如何查看付款提供商列表，以及如何配置应收账款的付款帐户。</span><span class="sxs-lookup"><span data-stu-id="6629b-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="6629b-105">此程序使用 USRT 演示数据公司，且旨在面向管理员和 IT 专业人员。</span><span class="sxs-lookup"><span data-stu-id="6629b-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="6629b-106">查看付款提供商列表</span><span class="sxs-lookup"><span data-stu-id="6629b-106">View a list of payment providers</span></span>
1. <span data-ttu-id="6629b-107">转至“应付账款”>“付款设置”>“付款服务”。</span><span class="sxs-lookup"><span data-stu-id="6629b-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="6629b-108">单击“查看可用提供商”。</span><span class="sxs-lookup"><span data-stu-id="6629b-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="6629b-109">配置付款帐户</span><span class="sxs-lookup"><span data-stu-id="6629b-109">Configure payment account</span></span>
1. <span data-ttu-id="6629b-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6629b-110">Click New.</span></span>
2. <span data-ttu-id="6629b-111">在“付款服务”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="6629b-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="6629b-112">在“付款连接器”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="6629b-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="6629b-113">切换“付款服务帐户”部分的扩展项。</span><span class="sxs-lookup"><span data-stu-id="6629b-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="6629b-114">在“环境”字段中，键入“PROD”。</span><span class="sxs-lookup"><span data-stu-id="6629b-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="6629b-115">单击“信用卡类型”。</span><span class="sxs-lookup"><span data-stu-id="6629b-115">Click Credit card types.</span></span>
7. <span data-ttu-id="6629b-116">在“付款日记帐”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6629b-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6629b-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6629b-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6629b-118">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="6629b-118">Click Add.</span></span>
10. <span data-ttu-id="6629b-119">在“货币”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6629b-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="6629b-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6629b-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="6629b-121">在“付款日记帐”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6629b-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="6629b-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6629b-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6629b-123">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="6629b-123">Click Add.</span></span>
15. <span data-ttu-id="6629b-124">在“货币”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6629b-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="6629b-125">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="6629b-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6629b-126">您可以根据自己需要的卡类型数量重复执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="6629b-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="6629b-127">在“付款日记帐”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="6629b-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="6629b-128">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="6629b-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="6629b-129">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="6629b-129">Click Add.</span></span>
20. <span data-ttu-id="6629b-130">在“货币”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6629b-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="6629b-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6629b-131">Click Save.</span></span>
22. <span data-ttu-id="6629b-132">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6629b-132">Close the page.</span></span>
23. <span data-ttu-id="6629b-133">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="6629b-133">Click Validate.</span></span>
24. <span data-ttu-id="6629b-134">单击“新信用卡的默认处理程序”复选框。</span><span class="sxs-lookup"><span data-stu-id="6629b-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="6629b-135">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6629b-135">Click Save.</span></span>

