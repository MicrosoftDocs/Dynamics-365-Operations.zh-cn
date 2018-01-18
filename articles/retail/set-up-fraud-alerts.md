---
title: "设置欺诈预警"
description: "此主题说明在订单处理过程中，如何设置预警规则来通知客户服务代表潜在的欺诈信息。 您可以定义特别的代码用以自动或手动地暂停可疑订单。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 9e4b0cb73c56e7800bfb90c037687dd4b91887f6
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="202ae-104">设置欺诈预警</span><span class="sxs-lookup"><span data-stu-id="202ae-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="202ae-105">本主题说明如何设置条件和规则以将具有欺诈可能性的销售订单置于暂停状态以进一步审核。</span><span class="sxs-lookup"><span data-stu-id="202ae-105">This topic explains how to set up criteria and rules to place potentially fraudulent sales orders on hold for further review.</span></span> <span data-ttu-id="202ae-106">欺诈审核功能用于确定销售订单中信息的有效性。</span><span class="sxs-lookup"><span data-stu-id="202ae-106">Fraud review functionality is used to determine the validity of information in a sales order.</span></span> <span data-ttu-id="202ae-107">如果根据组织的欺诈条件和规则，销售订单中的信息似乎可疑，则可以暂停订单以由管理员执行进一步审核。</span><span class="sxs-lookup"><span data-stu-id="202ae-107">If the information in the sales order appears to be questionable based on an organization’s fraud criteria and rules, the order may be put on hold for further review by an administrator.</span></span>

> [!NOTE]
> <span data-ttu-id="202ae-108">此功能只能用于零售呼叫中心渠道销售订单的处理。</span><span class="sxs-lookup"><span data-stu-id="202ae-108">This feature can only be used with Retail Call Center channel sales order processing.</span></span> 

<span data-ttu-id="202ae-109">在定义呼叫中心渠道时，必须将**启用订单完成**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="202ae-109">When the Call Center channel is defined, **Enable Order Completion** must be set to **Yes**.</span></span> <span data-ttu-id="202ae-110">当启用订单完成后，用户可以查看订单概括，并单击**提交**完成订单。</span><span class="sxs-lookup"><span data-stu-id="202ae-110">When order completion is enabled, users can view the order recap and click **Submit** to finalize the order.</span></span> <span data-ttu-id="202ae-111">用户还会获得手动暂停进行欺诈审核的销售订单的选项。</span><span class="sxs-lookup"><span data-stu-id="202ae-111">Users will also be provided options to manually place the sales order on fraud review hold.</span></span> <span data-ttu-id="202ae-112">由呼叫中心用户键入的销售订单在提交过程中通过欺诈检查规则进行处理。</span><span class="sxs-lookup"><span data-stu-id="202ae-112">Sales orders keyed in by a Call Center user are processed through fraud check rules and criteria during the submit process.</span></span>

<span data-ttu-id="202ae-113">有两类欺诈条件供系统用来参考以检查订单是否应该暂停并进行欺诈审核：</span><span class="sxs-lookup"><span data-stu-id="202ae-113">There are two types of fraud criteria that the system will reference to check if the order should be held for fraud review:</span></span>

-   <span data-ttu-id="202ae-114">**静态规则**使用特定值，如列入了黑名单的电话号码，或标记为被认为是过去的欺诈交易使用的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="202ae-114">**Static rules** use a specific value, such as a phone number that has been blacklisted or an email address that has been flagged as being known as used for past fraudulent transactions.</span></span> <span data-ttu-id="202ae-115">在**静态欺诈数据**页上，欺诈信息可以手动添加或通过数据导入添加，并且会为欺诈信息附上分数。</span><span class="sxs-lookup"><span data-stu-id="202ae-115">On the **Static Fraud Data** page, fraud information can be added manually or through data import, with scores attached to the fraudulent information.</span></span> <span data-ttu-id="202ae-116">如果欺诈检查打开，输入的每个销售订单都将与静态数据进行比较。</span><span class="sxs-lookup"><span data-stu-id="202ae-116">If fraud checking is turned on, every sales order entered will be compared to the static data.</span></span> <span data-ttu-id="202ae-117">如果在客户的账单地址或交货地址中找到数据，或者在销售行中的交货地址中找到，所有唯一匹配的分数将汇总。</span><span class="sxs-lookup"><span data-stu-id="202ae-117">If the data is found in either the customer’s billing or delivery address, or if the data is found in the delivery address on the sales line, the scores of all unique matches will be summed.</span></span>  
-   <span data-ttu-id="202ae-118">**动态规则**由为这些变量定义的变量和条件构成。</span><span class="sxs-lookup"><span data-stu-id="202ae-118">**Dynamic rules** are composed from variables and conditions defined for those variables.</span></span> <span data-ttu-id="202ae-119">使用动态规则，可以检查静态规则中未定义的其他条件。</span><span class="sxs-lookup"><span data-stu-id="202ae-119">With dynamic rules, other criteria not defined in the static rules can be checked.</span></span> <span data-ttu-id="202ae-120">可以使用更多复杂的“AND/OR”语句来考虑多个条件以确定是否存在与规则条件和提交的销售订单的正匹配。</span><span class="sxs-lookup"><span data-stu-id="202ae-120">More complex “AND/OR” statements can be used to consider multiple conditions to determine if there is a positive match against the rule criteria and the sales order being submitted.</span></span> <span data-ttu-id="202ae-121">例如，如果用户希望将与特定客户组值关联以及订购了特定产品的客户的所有订单均暂停以接受欺诈审核，那么验证客户和验证产品的条件将在**规则**页中使用“AND”条件定义。</span><span class="sxs-lookup"><span data-stu-id="202ae-121">For example, if a user wants to hold for fraud review all orders for customers that are tied to a specific customer group value and that ordered a specific product, the conditions to validate customer and validate products would be defined on the **Rules** page with an “AND” condition.</span></span> <span data-ttu-id="202ae-122">只有当两个条件均为 true，且分配给规则的分数值让订单的总欺诈得分超过最低欺诈分数（在呼叫中心参数中定义）时，订单才会进入欺诈保留状态。</span><span class="sxs-lookup"><span data-stu-id="202ae-122">The order would fall into fraud hold only if both conditions were true and if the score value assigned to the rule put the order’s total fraud score over the minimum fraud score as defined in Call Center parameters.</span></span>

<span data-ttu-id="202ae-123">呼叫中心用户还可以手动将订单放入欺诈保留队列。</span><span class="sxs-lookup"><span data-stu-id="202ae-123">A call center user may also manually place an order into the fraud hold queue.</span></span> <span data-ttu-id="202ae-124">如果输入订单的用户认为下订单的客户可疑并希望在处理之前由他人进一步审核订单的有效性，输入订单的用户可以在**销售订单汇总**页的**暂停**下拉菜单中选择**手动欺诈保留**选项（这将在调用**完成**订单功能后出现）。</span><span class="sxs-lookup"><span data-stu-id="202ae-124">If the user entering the order believes the customer placing the order may be suspicious and wants someone else to further review the validity of the order before it is processed, the user entering the order can choose the **Manual Fraud Hold** option from the **Holds** dropdown menu on the **Sales Order Summary** page (this appears after the **Complete** order function is called).</span></span> <span data-ttu-id="202ae-125">用户将被提示输入注释以进一步解释为何感觉该订单可能是欺诈订单，以便审核人有更多背景信息。</span><span class="sxs-lookup"><span data-stu-id="202ae-125">The user will be prompted to enter a note to further explain why they feel the order may be fraudulent so that the reviewer has more context.</span></span>

<span data-ttu-id="202ae-126">通过手动欺诈保留或系统计算欺诈分数保留的所有订单都将出现在**订单保留**页，在此页面中可以审核订单，然后采取取消或下达处理。</span><span class="sxs-lookup"><span data-stu-id="202ae-126">All orders held through manual fraud hold or by systematic calculation of fraud scores will appear on the **Order Holds** page, where the order can be reviewed and then either canceled or released to processing.</span></span>

> [!NOTE]
> <span data-ttu-id="202ae-127">在提交销售订单时，使用多个规则或过于复杂的规则将导致系统性能下降。</span><span class="sxs-lookup"><span data-stu-id="202ae-127">Use of multiple rules or overly complex rules will result in poor system performance when sales orders are submitted.</span></span> <span data-ttu-id="202ae-128">欺诈预警功能尚未优化，无法处理大量的静态欺诈数据条目和活动规则。</span><span class="sxs-lookup"><span data-stu-id="202ae-128">The fraud alert feature hasn't been optimized to handle a large volume of static fraud data entries and many active rules.</span></span> <span data-ttu-id="202ae-129">请切记，在执行呼叫中心销售订单条目的提交功能期间将对每个规则进行评估。</span><span class="sxs-lookup"><span data-stu-id="202ae-129">It’s important to remember that every rule is evaluated during the submit function of call center sales order entry.</span></span> <span data-ttu-id="202ae-130">这些规则将针对销售订单头和所有订单行进行评估。</span><span class="sxs-lookup"><span data-stu-id="202ae-130">The rules are evaluated against the sales order header and all order lines.</span></span> <span data-ttu-id="202ae-131">规则越多，规则语句越复杂，处理所需的时间就越长。</span><span class="sxs-lookup"><span data-stu-id="202ae-131">The more rules there are and the more complex the rule statements are, the longer it will take to process.</span></span> <span data-ttu-id="202ae-132">如果您的订单上有大量行项和大量的活动规则及静态数据条目，审核和验证所有数据并计算欺诈分数的这一系统过程可能会严重影响性能。</span><span class="sxs-lookup"><span data-stu-id="202ae-132">If you have a large number of line items on your order, and a large number of active rules and static data entries, this systematic process of reviewing and validating all of the data and calculating a fraud score can have a severe performance impact.</span></span>  <span data-ttu-id="202ae-133">在将对规则或静态欺诈条件的任何更改应用到生产环境之前，使用此功能的组织应始终测试并确认订单提交处理时间是否可接受。</span><span class="sxs-lookup"><span data-stu-id="202ae-133">Organizations using this feature should always test and confirm that the order submission processing time is acceptable before applying any changes to rules or static fraud criteria into the production environment.</span></span>

