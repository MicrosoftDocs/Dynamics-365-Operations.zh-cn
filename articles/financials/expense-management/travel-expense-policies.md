---
title: 定义支出策略
description: 您可以在 Microsoft Dynamics 365 for Finance and Operations 中定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的支出政策。
author: ryansandness
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26336710b277ce9594c8546f2214e152a3460204
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840881"
---
# <a name="expense-policies"></a><span data-ttu-id="e595e-103">支出策略</span><span class="sxs-lookup"><span data-stu-id="e595e-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e595e-104">您可以定义您的工作人员在输入和提交支出报表和出差申请时必须遵守的政策。</span><span class="sxs-lookup"><span data-stu-id="e595e-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="e595e-105">实施支出策略可以帮助您更有效地管理支出。</span><span class="sxs-lookup"><span data-stu-id="e595e-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="e595e-106">例如，您可为纽约城设置一个酒店费用政策，规定每晚酒店费用不能超过 250 美元。</span><span class="sxs-lookup"><span data-stu-id="e595e-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="e595e-107">如果员工提交的支出报表或出差申请中的房费超过了此金额，系统将通知</span><span class="sxs-lookup"><span data-stu-id="e595e-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="e595e-108">该员工，指出超出了针对支出的政策金额。</span><span class="sxs-lookup"><span data-stu-id="e595e-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="e595e-109">在您定义该政策时，可以配置员工</span><span class="sxs-lookup"><span data-stu-id="e595e-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="e595e-110">将收到的消息。</span><span class="sxs-lookup"><span data-stu-id="e595e-110">define the policy.</span></span>      
        
<span data-ttu-id="e595e-111">您可以定义策略的三种类型：</span><span class="sxs-lookup"><span data-stu-id="e595e-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="e595e-112">警告 – 允许工作人员提交费用报表或出差申请，但将为所有审核人和最新报表</span><span class="sxs-lookup"><span data-stu-id="e595e-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="e595e-113">标记该费用。</span><span class="sxs-lookup"><span data-stu-id="e595e-113">for later reporting.</span></span>        

- <span data-ttu-id="e595e-114">错误 – 在提交支出报表或出差申请前，要求工作人员修改该费用以符合该政策。</span><span class="sxs-lookup"><span data-stu-id="e595e-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="e595e-115">调整 – 要求工作人员或一个经理在提交支出报表或出差申请前输入超出政策金额的调整。</span><span class="sxs-lookup"><span data-stu-id="e595e-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="e595e-116">政策提示</span><span class="sxs-lookup"><span data-stu-id="e595e-116">Policy tips</span></span>
<span data-ttu-id="e595e-117">下面是一些在为费用管理新建政策时可以帮助您的建议。</span><span class="sxs-lookup"><span data-stu-id="e595e-117">Here are a few suggestions that can assist you whe creating new policies for expense management.</span></span> 
* <span data-ttu-id="e595e-118">政策有生效日期，如果创建政策时不为其设置费用产生后的日期，政策不会生效。</span><span class="sxs-lookup"><span data-stu-id="e595e-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="e595e-119">例如，如果今天创建新政策以实施最大餐费 50 美元，则不会针对此政策检查截止昨天的任何现有费用。</span><span class="sxs-lookup"><span data-stu-id="e595e-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="e595e-120">为可明细化的费用类别创建政策时，请考虑为费用行类型添加条件。</span><span class="sxs-lookup"><span data-stu-id="e595e-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="e595e-121">某些政策（如索取收据）可能对明细化行无意义，只应该应用于标题行或非明细化行。</span><span class="sxs-lookup"><span data-stu-id="e595e-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="e595e-122">何时评估政策</span><span class="sxs-lookup"><span data-stu-id="e595e-122">When to evaluate policies</span></span>

<span data-ttu-id="e595e-123">费用管理参数中有一个选项，用于在保存行时或在提交费用报表时评估费用管理政策。</span><span class="sxs-lookup"><span data-stu-id="e595e-123">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="e595e-124">如果选择在保存行时评估，这将确保用户可以查看需要执行哪些操作才能一次性完成所有费用报表。</span><span class="sxs-lookup"><span data-stu-id="e595e-124">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="e595e-125">否则，如果要在结束时向工作流提交期间进行验证，可以推迟政策评估并节约时间。</span><span class="sxs-lookup"><span data-stu-id="e595e-125">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
