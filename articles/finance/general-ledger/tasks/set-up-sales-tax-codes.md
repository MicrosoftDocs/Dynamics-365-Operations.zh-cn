---
title: 设置销售税代码
description: 本主题说明如何在 Dynamics 365 Finance 中设置销售税代码。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26dc61e340afcf1ce99d37c43d5942dc8792b765
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144735"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="98629-103">设置销售税代码</span><span class="sxs-lookup"><span data-stu-id="98629-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98629-104">本主题说明如何设置销售税代码。</span><span class="sxs-lookup"><span data-stu-id="98629-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="98629-105">为法人实体必须计算、征收和向销售税主管机构缴纳的所有间接税或关税创建销售税代码。</span><span class="sxs-lookup"><span data-stu-id="98629-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="98629-106">此任务使用 USMF 公司演示。</span><span class="sxs-lookup"><span data-stu-id="98629-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="98629-107">转到**导航窗格 > 纳税 > 间接税 > 销售税 > 销售税代码**。</span><span class="sxs-lookup"><span data-stu-id="98629-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="98629-108">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="98629-108">Select **New**.</span></span>
3. <span data-ttu-id="98629-109">在**销售税代码**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="98629-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="98629-110">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="98629-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="98629-111">通过打开下拉列表选择某一**结算期间**，以指定需要在哪一期间间隔内必须向哪一销售税主管机构申报和缴纳。</span><span class="sxs-lookup"><span data-stu-id="98629-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="98629-112">选择**分类帐过帐组**，以指定将销售税过帐到总帐的主科目。</span><span class="sxs-lookup"><span data-stu-id="98629-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="98629-113">展开**计算**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="98629-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="98629-114">其中包含多个字段，可控制销售税金额计算方式。</span><span class="sxs-lookup"><span data-stu-id="98629-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="98629-115">根据需要填写这些字段。</span><span class="sxs-lookup"><span data-stu-id="98629-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="98629-116">在界面顶部的**操作窗格**上，选择**销售税代码**。</span><span class="sxs-lookup"><span data-stu-id="98629-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="98629-117">选择**值**。</span><span class="sxs-lookup"><span data-stu-id="98629-117">Select **Values**.</span></span>
10. <span data-ttu-id="98629-118">在**值**列中输入此税代码的值。</span><span class="sxs-lookup"><span data-stu-id="98629-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="98629-119">在**计算**快速选项卡上的“来源”字段中，如果选择“单位金额”，将用该数值乘以该交易记录数量得出销售税金额。</span><span class="sxs-lookup"><span data-stu-id="98629-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="98629-120">如果销售税代码不是基于单位税，则该值为在用于该税码的来源上，用以计算销售税金额的百分比。</span><span class="sxs-lookup"><span data-stu-id="98629-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="98629-121">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="98629-121">Select **Save**.</span></span>
12. <span data-ttu-id="98629-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="98629-122">Close the page.</span></span>
13. <span data-ttu-id="98629-123">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="98629-123">Select **Save**.</span></span>

