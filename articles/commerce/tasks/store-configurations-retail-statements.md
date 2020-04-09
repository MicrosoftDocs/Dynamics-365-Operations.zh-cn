---
title: 零售报表的商店配置
description: 此程序会逐步演示商店的配置（这会影响到如何创建和过帐商业报表）。
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57081b9e737373641cd9d884919d03dcf62a2ffe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140647"
---
# <a name="store-configurations-for-retail-statements"></a><span data-ttu-id="7a0fe-103">零售报表的商店配置</span><span class="sxs-lookup"><span data-stu-id="7a0fe-103">Store configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a0fe-104">此程序会逐步演示商店的配置（这会影响到如何创建和过帐商业报表）。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-104">This procedure walks through configurations for the store that affect how Commerce statements get created and posted.</span></span> <span data-ttu-id="7a0fe-105">商店的财务维度将在另一个程序中论述。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-105">Financial dimensions on stores are covered in another procedure.</span></span> <span data-ttu-id="7a0fe-106">此程序使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-106">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="7a0fe-107">在**导航窗格**中，转到**模块 > Retail 和 Commerce > 渠道 > 商店 > 所有商店**。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-107">In the **Navgiation pane**, go to **Modules > Retail and Commerce > Channels > Stores > All stores**.</span></span>
2. <span data-ttu-id="7a0fe-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7a0fe-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7a0fe-110">单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-110">Click **Edit**.</span></span>
5. <span data-ttu-id="7a0fe-111">**报表/结算**快速选项卡中的设置会影响到商店的报表创建、验证和过帐。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-111">The settings in the **Statement/closing** fastTab affect the statement creation, validation, and posting for the store.</span></span> <span data-ttu-id="7a0fe-112">展开**报表/结算**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-112">Expand the **Statement/closing** fastTab.</span></span>  
6. <span data-ttu-id="7a0fe-113">在**报表方法**字段中，选择您想要用于对报表行进行分组的方法。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-113">In the **Statement method** field, select the method you want to use to to group the statement lines by.</span></span>  
7. <span data-ttu-id="7a0fe-114">如果在从报表创建批处理作业创建报表时，每天仅可创建一份报表，请在**每天一个报表**中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-114">Select "Yes" in **One statement per day** if there should only be one statement created per day when creating statements from the statement creation batch job.</span></span>  
8. <span data-ttu-id="7a0fe-115">**清偿申报计算**字段定义了清偿申报是否应合计或是否应使用最后一个。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-115">The **Tender declaration calculation** field defines whether tender declarations should be added together or if the last one should be used.</span></span>  
9. <span data-ttu-id="7a0fe-116">在**舍入**字段中，选择将舍入差额过帐到其中的会计科目。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-116">In the **Rounding** field, select the ledger account to post rounding differences into.</span></span>  
10. <span data-ttu-id="7a0fe-117">在**最大舍入差额**字段中，输入允许的最大舍入差额。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-117">In the **Maximum rounding difference** field, enter the maximum rounding difference allowed.</span></span>
11. <span data-ttu-id="7a0fe-118">在**过帐**字段中，输入报表允许的最大总过帐差额。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-118">In the **Posting** field, enter the maximum total posting difference allowed for a statement.</span></span>
12. <span data-ttu-id="7a0fe-119">在**班次**字段中，输入报表班次中的最大总过帐差额。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-119">In the **Shift** field, enter the maximum total difference within a shift in a statement.</span></span>  
13. <span data-ttu-id="7a0fe-120">在**交易**字段中，输入报表行中的最大总过帐差额。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-120">In the **Transaction** field, enter the maximum total difference in a statement line.</span></span>  
14. <span data-ttu-id="7a0fe-121">在**结算方法**字段中，定义将包括在报表中的交易是已结算的班次的一部分，还是定义的日期/时间范围内的任何交易。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-121">In the **Closing method** field, define whether transactions that will be included in a statement should be part of a closed shift or if they can be any transactions within the defined date/time range.</span></span>  
15. <span data-ttu-id="7a0fe-122">在**工作日结束时**字段中，输入一个时间，如果午夜之后发生的交易应随前一天过帐。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-122">In the **End of business day** field, enter a time if transactions that happen after midnight should be posted with the previous day.</span></span>  
16. <span data-ttu-id="7a0fe-123">如果午夜之后发生的交易应过帐为前一天的一部分，请在**按工作日过帐**中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-123">Select "Yes" in **Post as business day** if transactions that happen after midnight should be posted as part of the previous day.</span></span>  
17. <span data-ttu-id="7a0fe-124">在**按报表拆分方法**中选择“是”，以为定义的每种报表方法创建报表。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-124">Select "Yes" in **Split by Statement method** to get statements created for each statement method defined.</span></span> <span data-ttu-id="7a0fe-125">如果需要为交易数量高的商店提高过帐性能，这可能很有用，因为它将创建许多可并行处理的较小的报表。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-125">This can be useful if the performance of the posting needs to be improved for stores with high transaction volumes since it will create many smaller statements that can be processed in parallel.</span></span>  
18. <span data-ttu-id="7a0fe-126">在**常规**快速选项卡的**默认客户**字段中，您可以选择客户科目，以用于未经预约而来的客户的销售。</span><span class="sxs-lookup"><span data-stu-id="7a0fe-126">In the **General** fastTab, in the **Default customer** field, you can select the customer account to use for sales to walk-in customers.</span></span>  

