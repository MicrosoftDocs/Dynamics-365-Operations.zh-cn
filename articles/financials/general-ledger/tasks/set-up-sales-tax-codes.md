---
title: 设置销售税代码
description: 为法人实体必须计算、征收和向销售税主管机构缴纳的所有间接税或关税创建销售税代码。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571575"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="76c94-103">设置销售税代码</span><span class="sxs-lookup"><span data-stu-id="76c94-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76c94-104">为法人实体必须计算、征收和向销售税主管机构缴纳的所有间接税或关税创建销售税代码。</span><span class="sxs-lookup"><span data-stu-id="76c94-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="76c94-105">本任务使用 USMF 公司进行演示。</span><span class="sxs-lookup"><span data-stu-id="76c94-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="76c94-106">转到报税>间接税>销售税》销售税代码。</span><span class="sxs-lookup"><span data-stu-id="76c94-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="76c94-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="76c94-107">Click New.</span></span>
3. <span data-ttu-id="76c94-108">在“销售税代码”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="76c94-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="76c94-109">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="76c94-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="76c94-110">选择某一结算期间，以指定需要在哪一期间间隔内必须向哪一销售税主管机构申报和缴纳。</span><span class="sxs-lookup"><span data-stu-id="76c94-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="76c94-111">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="76c94-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="76c94-112">选择分类帐过帐组，以指定将销售税过帐到总帐的主科目。</span><span class="sxs-lookup"><span data-stu-id="76c94-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="76c94-113">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="76c94-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="76c94-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="76c94-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="76c94-115">展开“计算”快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="76c94-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="76c94-116">“计算”快速选项卡有多个字段，可控制销售税金额计算方式。</span><span class="sxs-lookup"><span data-stu-id="76c94-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="76c94-117">在操作窗格上，单击“销售税代码”。</span><span class="sxs-lookup"><span data-stu-id="76c94-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="76c94-118">单击“数值”。</span><span class="sxs-lookup"><span data-stu-id="76c94-118">Click Values.</span></span>
13. <span data-ttu-id="76c94-119">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="76c94-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="76c94-120">输入此税费代码的值。</span><span class="sxs-lookup"><span data-stu-id="76c94-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="76c94-121">在“计算”快速选项卡上的“来源”字段中，如果选择“单位金额”，将用该数值乘以该交易记录数量得出销售税金额。</span><span class="sxs-lookup"><span data-stu-id="76c94-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="76c94-122">如果销售税代码不是基于单位税，则该值为在用于该税码的来源上，用以计算销售税金额的百分比。</span><span class="sxs-lookup"><span data-stu-id="76c94-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="76c94-123">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="76c94-123">Click Save.</span></span>
16. <span data-ttu-id="76c94-124">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="76c94-124">Close the page.</span></span>
17. <span data-ttu-id="76c94-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="76c94-125">Click Save.</span></span>

