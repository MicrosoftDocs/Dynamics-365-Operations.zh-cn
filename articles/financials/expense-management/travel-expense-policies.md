---
title: "定义支出策略"
description: "您可以通过在 Microsoft Dynamics 365 for Finance and Operations 中输入和提交费用报表和出差申请来定义工作人员必须遵守的支出策略。"
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 062d6f01bb07324ad5b8dc6b9fd7617756502c17
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="expense-policies"></a><span data-ttu-id="fe935-103">支出策略</span><span class="sxs-lookup"><span data-stu-id="fe935-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe935-104">您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的政策。</span><span class="sxs-lookup"><span data-stu-id="fe935-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="fe935-105">实施支出策略可以帮助您更有效地管理支出。</span><span class="sxs-lookup"><span data-stu-id="fe935-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="fe935-106">例如，您可为纽约城设置一个酒店费用政策，规定每晚酒店费用不能超过 250 美元。</span><span class="sxs-lookup"><span data-stu-id="fe935-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="fe935-107">如果员工提交的支出报表或出差申请中的房费超过了此金额，系统将通知</span><span class="sxs-lookup"><span data-stu-id="fe935-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="fe935-108">该员工，指出超出了针对支出的政策金额。</span><span class="sxs-lookup"><span data-stu-id="fe935-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="fe935-109">在您定义该政策时，可以配置员工</span><span class="sxs-lookup"><span data-stu-id="fe935-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="fe935-110">将收到的消息。</span><span class="sxs-lookup"><span data-stu-id="fe935-110">define the policy.</span></span>      
        
<span data-ttu-id="fe935-111">您可以定义策略的三种类型：</span><span class="sxs-lookup"><span data-stu-id="fe935-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="fe935-112">警告 – 允许工作人员提交费用报表或出差申请，但将为所有审核人和最新报表</span><span class="sxs-lookup"><span data-stu-id="fe935-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="fe935-113">标记该费用。</span><span class="sxs-lookup"><span data-stu-id="fe935-113">for later reporting.</span></span>        

- <span data-ttu-id="fe935-114">错误 – 在提交支出报表或出差申请前，要求工作人员修改该费用以符合该政策。</span><span class="sxs-lookup"><span data-stu-id="fe935-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="fe935-115">调整 – 要求工作人员或一个经理在提交支出报表或出差申请前输入超出政策金额的调整。</span><span class="sxs-lookup"><span data-stu-id="fe935-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="fe935-116">您还可以为支出政策具有效力的设置日期范围。</span><span class="sxs-lookup"><span data-stu-id="fe935-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="fe935-117">例如，在节假日旅行旺季，丹麦</span><span class="sxs-lookup"><span data-stu-id="fe935-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="fe935-118">和纽约市之间航线的飞机票的价格可能很贵。</span><span class="sxs-lookup"><span data-stu-id="fe935-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="fe935-119">您可以定义一个飞行支出规则，</span><span class="sxs-lookup"><span data-stu-id="fe935-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="fe935-120">将飞往纽约城的成本限制在最高 DKK 5000，并且可以指定此规则在 3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="fe935-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="fe935-121">和 9 月 15 日之间具有效力。</span><span class="sxs-lookup"><span data-stu-id="fe935-121">September 15.</span></span>

