--- 
title: "创建、计算和过帐零售商店的报表"
description: "此程序会逐步演示如何手动创建、计算和过帐某一商店的报表。"
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42ab631e29a7fae1140acd41ad80c13e55ca1404
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="01f86-103">创建、计算和过帐零售商店的报表</span><span class="sxs-lookup"><span data-stu-id="01f86-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="01f86-104">此程序会逐步演示如何手动创建、计算和过帐某一商店的报表。</span><span class="sxs-lookup"><span data-stu-id="01f86-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="01f86-105">还可以配置相同任务的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="01f86-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="01f86-106">配置和运行批处理作业的步骤可以在其他主题中找到。</span><span class="sxs-lookup"><span data-stu-id="01f86-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="01f86-107">要完成此程序，您必须在 POS 中有已完成的交易，让后将其拉到 Dynamics AX 中。</span><span class="sxs-lookup"><span data-stu-id="01f86-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="01f86-108">此记录使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="01f86-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="01f86-109">此过程可能涉及 Microsoft Dynamics AX。</span><span class="sxs-lookup"><span data-stu-id="01f86-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="01f86-110">请注意，Dynamics AX 现在称为 Microsoft Dynamics 365 for Operations。</span><span class="sxs-lookup"><span data-stu-id="01f86-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="01f86-111">转至“所有工作区”></span><span class="sxs-lookup"><span data-stu-id="01f86-111">Go to All workspaces > ..</span></span> <span data-ttu-id="01f86-112">>“零售商店财务”。</span><span class="sxs-lookup"><span data-stu-id="01f86-112">> Retail store financials.</span></span>
2. <span data-ttu-id="01f86-113">单击“新建报表”。</span><span class="sxs-lookup"><span data-stu-id="01f86-113">Click New statement.</span></span>
3. <span data-ttu-id="01f86-114">在“商店编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="01f86-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="01f86-115">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="01f86-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="01f86-116">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="01f86-116">Click OK.</span></span>
    * <span data-ttu-id="01f86-117">“设置组”中的设置可以控制报表包括哪些交易记录，以及这些交易记录如何分组到报表行。</span><span class="sxs-lookup"><span data-stu-id="01f86-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="01f86-118">您可以打开“设置组”并更改这些设置，也可以使用默认设置。</span><span class="sxs-lookup"><span data-stu-id="01f86-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="01f86-119">“报表方法”字段定义了报表行如何分组。</span><span class="sxs-lookup"><span data-stu-id="01f86-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="01f86-120">如果您仅想要针对某个职员或收银机计算报表，请选择特定的职员或收银机。</span><span class="sxs-lookup"><span data-stu-id="01f86-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="01f86-121">在“结算方法”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="01f86-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="01f86-122">单击“计算报表”。</span><span class="sxs-lookup"><span data-stu-id="01f86-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="01f86-123">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="01f86-123">Click Yes.</span></span>
    * <span data-ttu-id="01f86-124">计算完报表之后，应出现使用所用的每种付款方式和报表方法的总金额创建的行。</span><span class="sxs-lookup"><span data-stu-id="01f86-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="01f86-125">如果需要输入或更新金额，在每一行输入已盘点金额。</span><span class="sxs-lookup"><span data-stu-id="01f86-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="01f86-126">使用 POS 中完成的清偿申报金额填充已盘点字段。</span><span class="sxs-lookup"><span data-stu-id="01f86-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="01f86-127">单击“将报表过帐”。</span><span class="sxs-lookup"><span data-stu-id="01f86-127">Click Post statement.</span></span>
10. <span data-ttu-id="01f86-128">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="01f86-128">Click Close.</span></span>
11. <span data-ttu-id="01f86-129">转至“零售和商业”>“渠道”>“零售商店财务”。</span><span class="sxs-lookup"><span data-stu-id="01f86-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="01f86-130">单击“已过帐的报表”选项卡。</span><span class="sxs-lookup"><span data-stu-id="01f86-130">Click the Posted statements tab.</span></span>

