---
title: 购买和出售休假
description: 在 Dynamics 365 Human Resources 中，您可以根据公司设置的购买和出售休假策略提交购买和出售休假请求。
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d32abacc1539cb930ad6f1ebcfe6fa9af4befcf
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271470"
---
# <a name="buy-and-sell-leave"></a><span data-ttu-id="8cd86-103">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="8cd86-103">Buy and sell leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8cd86-104">在 Dynamics 365 Human Resources 中，您可以根据公司设置的购买和出售休假策略提交购买和出售休假请求。</span><span class="sxs-lookup"><span data-stu-id="8cd86-104">In Dynamics 365 Human Resources, you can submit requests to buy and sell leave based on the buy and sell leave policies set up by your company.</span></span>  

## <a name="request-to-buy-leave"></a><span data-ttu-id="8cd86-105">购买休假的请求</span><span class="sxs-lookup"><span data-stu-id="8cd86-105">Request to buy leave</span></span>

1. <span data-ttu-id="8cd86-106">在 **员工自助服务** 工作区中，在 **休息时间余额** 磁贴中选择 **购买休假请求**。</span><span class="sxs-lookup"><span data-stu-id="8cd86-106">In the **Employee self service** workspace, select **Buy leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="8cd86-107">添加一个 **休假类型**，然后输入您想要购买的休假金额的 **金额**。</span><span class="sxs-lookup"><span data-stu-id="8cd86-107">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to buy.</span></span> 

3. <span data-ttu-id="8cd86-108">准备好提交请求时选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="8cd86-108">Select **Submit** when you're ready to submit your request.</span></span> 

<span data-ttu-id="8cd86-109">您的余额将自动更新，或者在更新之前经过审批流程。</span><span class="sxs-lookup"><span data-stu-id="8cd86-109">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="8cd86-110">这取决于如何配置购买策略。</span><span class="sxs-lookup"><span data-stu-id="8cd86-110">This depends on how the buy policy has been configured.</span></span>

## <a name="request-to-sell-leave"></a><span data-ttu-id="8cd86-111">出售休假请求</span><span class="sxs-lookup"><span data-stu-id="8cd86-111">Request to sell leave</span></span>

1. <span data-ttu-id="8cd86-112">在 **员工自助服务** 工作区中，在 **休息时间余额** 磁贴中选择 **出售休假请求**。</span><span class="sxs-lookup"><span data-stu-id="8cd86-112">In the **Employee self service** workspace, select **Sell leave request** in the **Time Off Balances** tile.</span></span> 

2. <span data-ttu-id="8cd86-113">添加一个 **休假类型**，然后输入您想要出售的休假金额的 **金额**。</span><span class="sxs-lookup"><span data-stu-id="8cd86-113">Add a **Leave type** and enter an **Amount** for the amount of leave you'd like to sell.</span></span> 

3. <span data-ttu-id="8cd86-114">准备好提交请求时选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="8cd86-114">Select **Submit** when you're ready to submit your request.</span></span>

<span data-ttu-id="8cd86-115">您的余额将自动更新，或者在更新之前经过审批流程。</span><span class="sxs-lookup"><span data-stu-id="8cd86-115">Your balances will either automatically update or go through an approval process before updating.</span></span> <span data-ttu-id="8cd86-116">这取决于如何配置购买策略。</span><span class="sxs-lookup"><span data-stu-id="8cd86-116">This depends on how the buy policy has been configured.</span></span>


## <a name="troubleshooting"></a><span data-ttu-id="8cd86-117">疑难解答</span><span class="sxs-lookup"><span data-stu-id="8cd86-117">Troubleshooting</span></span> 

<span data-ttu-id="8cd86-118">如果购买或出售休假请求工作流失败，具有 **EssLeaveBuySellRequestApprover** 特权的用户可以查看所有休假购买和出售请求的消息日志。</span><span class="sxs-lookup"><span data-stu-id="8cd86-118">If a buy or sell leave request workflow fails, users with the **EssLeaveBuySellRequestApprover** privilege can review the message log for all leave buy and sell requests.</span></span> <span data-ttu-id="8cd86-119">为此，请转到 **休假和缺勤 > 链接 > 购买和出售休假请求 > 消息日志**（在左上角）。</span><span class="sxs-lookup"><span data-stu-id="8cd86-119">To do this, go to **Leave and absence > Link > Buy and sell leave requests > Message log** (on the upper left).</span></span> <span data-ttu-id="8cd86-120">**消息日志** 向用户显示交易的处理方式和关联的工作流历史记录。</span><span class="sxs-lookup"><span data-stu-id="8cd86-120">The **Message log** shows users how the transactions were processed and the associated workflow history.</span></span>


## <a name="see-also"></a><span data-ttu-id="8cd86-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="8cd86-121">See also</span></span>

[<span data-ttu-id="8cd86-122">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="8cd86-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="8cd86-123">管理购买和出售休假策略</span><span class="sxs-lookup"><span data-stu-id="8cd86-123">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
