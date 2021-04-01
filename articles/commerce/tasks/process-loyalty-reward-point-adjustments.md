---
title: 处理会员奖励分调整
description: 该过程说明了如何查看积分卡信息，以及如何调整奖励积分点数。
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailLoyaltyCards, RetailLoyaltyCardRewardPointTrans, RetailLoyaltyCardRewardPointAdjustment, RetailAffiliationLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fca59651065d20e79a47b49a4eb3b4def7cac674
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232802"
---
# <a name="process-loyalty-reward-point-adjustments"></a><span data-ttu-id="71fe0-103">处理会员奖励分调整</span><span class="sxs-lookup"><span data-stu-id="71fe0-103">Process loyalty reward point adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71fe0-104">该过程说明了如何查看积分卡信息，以及如何调整奖励积分点数。</span><span class="sxs-lookup"><span data-stu-id="71fe0-104">This procedure demonstrates how to look up loyalty card information and adjust loyalty reward points.</span></span> <span data-ttu-id="71fe0-105">创建此任务的演示数据公司是 USRT。</span><span class="sxs-lookup"><span data-stu-id="71fe0-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="71fe0-106">此任务是为“商业业务经理”角色或“客服服务经理”角色而设计的。</span><span class="sxs-lookup"><span data-stu-id="71fe0-106">This task is intended for the Commerce operations manager role or a Customer service manager role.</span></span>

1. <span data-ttu-id="71fe0-107">转到“积分卡”。</span><span class="sxs-lookup"><span data-stu-id="71fe0-107">Go to Loyalty cards.</span></span>
2. <span data-ttu-id="71fe0-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="71fe0-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="71fe0-109">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="71fe0-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="71fe0-110">单击“积分卡交易”。</span><span class="sxs-lookup"><span data-stu-id="71fe0-110">Click Card transactions.</span></span>
    * <span data-ttu-id="71fe0-111">在此页可以查看所选积分卡的所有相关积分交易记录。</span><span class="sxs-lookup"><span data-stu-id="71fe0-111">On this page you can view all loyalty transactions for the selected loyalty card.</span></span>  
5. <span data-ttu-id="71fe0-112">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="71fe0-112">Close the page.</span></span>
6. <span data-ttu-id="71fe0-113">单击“积分卡调整”。</span><span class="sxs-lookup"><span data-stu-id="71fe0-113">Click Card adjustments.</span></span>
7. <span data-ttu-id="71fe0-114">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="71fe0-114">Click New.</span></span>
8. <span data-ttu-id="71fe0-115">在“奖励点数”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="71fe0-115">In the Reward point field, enter or select a value.</span></span>
9. <span data-ttu-id="71fe0-116">在“金额或数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="71fe0-116">In the Amount or quantity field, enter a number.</span></span>
    * <span data-ttu-id="71fe0-117">通过使用正负数，您可以添加或删除该积分卡的点数。</span><span class="sxs-lookup"><span data-stu-id="71fe0-117">You can add or remove points from the loyalty card by using positive or negative amounts.</span></span>  
10. <span data-ttu-id="71fe0-118">在“积分项目”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="71fe0-118">In the Loyalty program field, enter or select a value.</span></span>
11. <span data-ttu-id="71fe0-119">在“注释”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="71fe0-119">In the Comment field, type a value.</span></span>
12. <span data-ttu-id="71fe0-120">单击“过帐调整”。</span><span class="sxs-lookup"><span data-stu-id="71fe0-120">Click Post adjustment.</span></span>
13. <span data-ttu-id="71fe0-121">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="71fe0-121">Click Yes.</span></span>
14. <span data-ttu-id="71fe0-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="71fe0-122">Close the page.</span></span>
    * <span data-ttu-id="71fe0-123">通常此时您可以刷新该页以在“奖励积分总额”选项卡中查看奖励积分调整的结果。但是，如果您正在作为任务指南运行它，则不要刷新，否则，该任务指南将会停止。</span><span class="sxs-lookup"><span data-stu-id="71fe0-123">Normally at this point you'd refresh the page to see the result of the reward points adjustment in the Reward point summary tab. But if you are running this as a task guide, don't refresh now because if you do, the task guide will stop.</span></span>  
15. <span data-ttu-id="71fe0-124">单击“积分卡交易”。</span><span class="sxs-lookup"><span data-stu-id="71fe0-124">Click Card transactions.</span></span>
16. <span data-ttu-id="71fe0-125">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="71fe0-125">Close the page.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]