---
title: "定义支出策略"
description: "您可以通过在 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中输入和提交费用报表和出差申请来定义工作人员必须遵守的支出策略。"
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 940d6f8c3d878c2c12806ad04a092856df2acb33
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="expense-policies"></a><span data-ttu-id="3eb32-103">支出策略</span><span class="sxs-lookup"><span data-stu-id="3eb32-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3eb32-104">您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的政策。</span><span class="sxs-lookup"><span data-stu-id="3eb32-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="3eb32-105">实施支出策略可以帮助您更有效地管理支出。</span><span class="sxs-lookup"><span data-stu-id="3eb32-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="3eb32-106">例如，您可为纽约城设置一个酒店费用政策，规定每晚酒店费用不能超过 250 美元。</span><span class="sxs-lookup"><span data-stu-id="3eb32-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="3eb32-107">如果某工作人员提交的费用报表或出差申请中的房费超过这一金额，则系统将通知该工作人员，指出超出了政策的费用金额。</span><span class="sxs-lookup"><span data-stu-id="3eb32-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="3eb32-108">在您定义该政策时，可以配置工作人员将收到的消息。</span><span class="sxs-lookup"><span data-stu-id="3eb32-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="3eb32-109">您可以定义策略的三种类型：</span><span class="sxs-lookup"><span data-stu-id="3eb32-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="3eb32-110">警告 – 允许工作人员提交费用报表或出差申请，但将为所有审核人和最新报表</span><span class="sxs-lookup"><span data-stu-id="3eb32-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="3eb32-111">标记该费用。</span><span class="sxs-lookup"><span data-stu-id="3eb32-111">for later reporting.</span></span> 
 - <span data-ttu-id="3eb32-112">错误 – 在提交支出报表或出差申请前，要求工作人员修改该费用以符合该政策。</span><span class="sxs-lookup"><span data-stu-id="3eb32-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="3eb32-113">调整 – 要求工作人员或一个经理在提交支出报表或出差申请前输入超出政策金额的调整。</span><span class="sxs-lookup"><span data-stu-id="3eb32-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="3eb32-114">您还可以为支出政策具有效力的设置日期范围。</span><span class="sxs-lookup"><span data-stu-id="3eb32-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="3eb32-115">例如，在节假日旅行旺季，丹麦和纽约城之间航线的飞机票的价格可能很昂贵。</span><span class="sxs-lookup"><span data-stu-id="3eb32-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="3eb32-116">您可以定义一个飞行支出规则，将飞往纽约城的成本限制在最高 DKK 5000，并且可以指定此规则在 3 月 15 日和 9 月 15 日之间具有效力。</span><span class="sxs-lookup"><span data-stu-id="3eb32-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

