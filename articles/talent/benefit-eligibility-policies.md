---
title: "福利资格策略"
description: "本文提供有关福利资格策略的信息，可帮助您定义哪些人有资格享受特定福利。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d0f599964833162dd4bf4b490019cbed692428eb
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="e97f1-103">福利资格策略</span><span class="sxs-lookup"><span data-stu-id="e97f1-103">Benefit eligibility policies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e97f1-104">本主题提供有关福利资格策略的信息，可帮助您定义哪些人有资格享受特定福利。</span><span class="sxs-lookup"><span data-stu-id="e97f1-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="e97f1-105">在您创建福利时，您决定哪些福利可用于哪些员工。</span><span class="sxs-lookup"><span data-stu-id="e97f1-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="e97f1-106">下表显示您可以使其用于特定员工的福利示例。</span><span class="sxs-lookup"><span data-stu-id="e97f1-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="e97f1-107">福利</span><span class="sxs-lookup"><span data-stu-id="e97f1-107">Benefit</span></span>          | <span data-ttu-id="e97f1-108">福利可用于谁</span><span class="sxs-lookup"><span data-stu-id="e97f1-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="e97f1-109">健康保险</span><span class="sxs-lookup"><span data-stu-id="e97f1-109">Health insurance</span></span> | <span data-ttu-id="e97f1-110">所有员工</span><span class="sxs-lookup"><span data-stu-id="e97f1-110">All employees</span></span>                   |
| <span data-ttu-id="e97f1-111">移动电话</span><span class="sxs-lookup"><span data-stu-id="e97f1-111">Mobile phone</span></span>     | <span data-ttu-id="e97f1-112">销售员工、主管人员</span><span class="sxs-lookup"><span data-stu-id="e97f1-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="e97f1-113">停车证</span><span class="sxs-lookup"><span data-stu-id="e97f1-113">Parking passes</span></span>   | <span data-ttu-id="e97f1-114">主管人员</span><span class="sxs-lookup"><span data-stu-id="e97f1-114">Executives</span></span>                      |

<span data-ttu-id="e97f1-115">以下组件用于创建资格策略：</span><span class="sxs-lookup"><span data-stu-id="e97f1-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="e97f1-116">政策规则类型</span><span class="sxs-lookup"><span data-stu-id="e97f1-116">Policy rule types</span></span>
-   <span data-ttu-id="e97f1-117">福利资格策略</span><span class="sxs-lookup"><span data-stu-id="e97f1-117">Benefit eligibility policies</span></span>

<span data-ttu-id="e97f1-118">策略规则类型定义开发具体政策规则时所使用的查询参数。</span><span class="sxs-lookup"><span data-stu-id="e97f1-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="e97f1-119">在您创建政策规则类型后，您可以创建福利资格策略。</span><span class="sxs-lookup"><span data-stu-id="e97f1-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="e97f1-120">策略可以创建适用于一个或多个法人的规则集合。</span><span class="sxs-lookup"><span data-stu-id="e97f1-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="e97f1-121">在每个策略中，您可以查看您之前创建的任何福利资格策略规则类型。</span><span class="sxs-lookup"><span data-stu-id="e97f1-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="e97f1-122">您定义策略中的规则范围。</span><span class="sxs-lookup"><span data-stu-id="e97f1-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="e97f1-123">例如，如果，您创建一个名为**主管人员**的福利资格政策规则类型，您可以指定在该策略中有哪些规则。</span><span class="sxs-lookup"><span data-stu-id="e97f1-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="e97f1-124">在此示例中，规则可能规定包含字词“主管人员”的任何职务都应包括该规则内。</span><span class="sxs-lookup"><span data-stu-id="e97f1-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="e97f1-125">在您定义规则的参数或在策略包括的规则后，可以将一个特定规则分配到福利。</span><span class="sxs-lookup"><span data-stu-id="e97f1-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="e97f1-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="e97f1-126">See also</span></span>
--------

[<span data-ttu-id="e97f1-127">定义和管理福利计划</span><span class="sxs-lookup"><span data-stu-id="e97f1-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)



