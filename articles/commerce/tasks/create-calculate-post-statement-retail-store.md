---
title: 创建、计算和过帐零售商店的对帐单
description: 本主题介绍如何手动创建、计算和过帐某一商店的报表。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ef31bc02fe1761a587ff6bcbecf4a0f34daea9b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964862"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="08063-103">创建、计算和过帐零售商店的对帐单</span><span class="sxs-lookup"><span data-stu-id="08063-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08063-104">本主题介绍如何手动创建、计算和过帐某一商店的报表。</span><span class="sxs-lookup"><span data-stu-id="08063-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="08063-105">还可以配置相同任务的批处理作业。</span><span class="sxs-lookup"><span data-stu-id="08063-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="08063-106">配置和运行批处理作业的步骤可以在其他主题中找到。</span><span class="sxs-lookup"><span data-stu-id="08063-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="08063-107">要完成此过程，您必须在 POS 中有已完成的交易，让后将其拉到 Dynamics 365 Commerce 中。</span><span class="sxs-lookup"><span data-stu-id="08063-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="08063-108">此记录使用 USRT 演示数据公司。</span><span class="sxs-lookup"><span data-stu-id="08063-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="08063-109">从主页选择 **商店财务**。</span><span class="sxs-lookup"><span data-stu-id="08063-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="08063-110">选择 **新建报表**。</span><span class="sxs-lookup"><span data-stu-id="08063-110">Select **New statement**.</span></span>
3. <span data-ttu-id="08063-111">在 **商店编号** 字段中，从下拉列表中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="08063-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="08063-112">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="08063-112">Select **OK**.</span></span>
5. <span data-ttu-id="08063-113">**设置** 组中的设置可以控制报表包括哪些交易记录，以及这些交易记录如何分组到报表行。</span><span class="sxs-lookup"><span data-stu-id="08063-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="08063-114">您可以打开 **设置** 组并更改这些设置，也可以使用默认设置。</span><span class="sxs-lookup"><span data-stu-id="08063-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="08063-115">**报表方法** 字段定义了报表行如何分组。</span><span class="sxs-lookup"><span data-stu-id="08063-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="08063-116">如果您仅想要针对某个职员或收银机计算报表，请在 **职员/收银机** 字段中选择特定的职员或收银机。</span><span class="sxs-lookup"><span data-stu-id="08063-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="08063-117">在 **结算方法** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="08063-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="08063-118">从操作窗格选择 **计算报表**。</span><span class="sxs-lookup"><span data-stu-id="08063-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="08063-119">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="08063-119">Select **Yes**.</span></span>
    - <span data-ttu-id="08063-120">计算完报表之后，应出现使用所用的每种付款方式和报表方法的总金额创建的行。</span><span class="sxs-lookup"><span data-stu-id="08063-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="08063-121">如果需要输入或更新金额，在每一行输入已盘点金额。</span><span class="sxs-lookup"><span data-stu-id="08063-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="08063-122">使用 POS 中完成的清偿申报金额填充已盘点字段。</span><span class="sxs-lookup"><span data-stu-id="08063-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="08063-123">从操作窗格选择 **过帐报表**。</span><span class="sxs-lookup"><span data-stu-id="08063-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="08063-124">选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="08063-124">Select **Close**.</span></span>
11. <span data-ttu-id="08063-125">关闭该窗格。</span><span class="sxs-lookup"><span data-stu-id="08063-125">Close the pane.</span></span>
12. <span data-ttu-id="08063-126">在主页选择 **商店财务**。</span><span class="sxs-lookup"><span data-stu-id="08063-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="08063-127">选择 **已过帐的报表** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="08063-127">Select the **Posted statements** tab.</span></span>

