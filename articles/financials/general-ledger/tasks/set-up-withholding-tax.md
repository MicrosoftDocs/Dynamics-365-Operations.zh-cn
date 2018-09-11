--- 
title: "设置预缴税金"
description: "预缴税金是针对供应商的一种不创建增值税交易记录的税金。"
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: a2867bcbef7aa9e41b35603276742be448317221
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="79258-103">设置预缴税金</span><span class="sxs-lookup"><span data-stu-id="79258-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79258-104">预缴税金是针对供应商的一种不创建增值税交易记录的税金。</span><span class="sxs-lookup"><span data-stu-id="79258-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="79258-105">对供应商付款计算的预缴税金是一种负债。</span><span class="sxs-lookup"><span data-stu-id="79258-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="79258-106">因此，在过帐预缴税金时，只有资产负债表科目或负债科目是有效科目。</span><span class="sxs-lookup"><span data-stu-id="79258-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="79258-107">此任务指南演示如何设置预缴税金。</span><span class="sxs-lookup"><span data-stu-id="79258-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="79258-108">转到“纳税”>“间接税”>“预缴税金”>“预缴税金代码”。</span><span class="sxs-lookup"><span data-stu-id="79258-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="79258-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="79258-109">Click New.</span></span>
3. <span data-ttu-id="79258-110">在“预缴税金代码”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="79258-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="79258-111">在“预缴税金名称”字段中，输入预缴税金代码的名称。</span><span class="sxs-lookup"><span data-stu-id="79258-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="79258-112">在“主科目”字段中，选择将预缴应交税金过帐的主科目。</span><span class="sxs-lookup"><span data-stu-id="79258-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="79258-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="79258-113">Click Save.</span></span>
7. <span data-ttu-id="79258-114">单击“数值”。</span><span class="sxs-lookup"><span data-stu-id="79258-114">Click Values.</span></span>
8. <span data-ttu-id="79258-115">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="79258-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="79258-116">在“数值”字段中，输入用于计算预缴税金的百分比。</span><span class="sxs-lookup"><span data-stu-id="79258-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="79258-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="79258-117">Click Save.</span></span>
11. <span data-ttu-id="79258-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="79258-118">Close the page.</span></span>
12. <span data-ttu-id="79258-119">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="79258-119">Click Save.</span></span>
13. <span data-ttu-id="79258-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="79258-120">Close the page.</span></span>
14. <span data-ttu-id="79258-121">转到“纳税”>“间接税”>“预缴税金”>“预缴税金组”。</span><span class="sxs-lookup"><span data-stu-id="79258-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="79258-122">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="79258-122">Click New.</span></span>
16. <span data-ttu-id="79258-123">在“预缴税金组”字段中，输入预缴税金组的标识。</span><span class="sxs-lookup"><span data-stu-id="79258-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="79258-124">在“描述”字段中，输入预缴税金组的名称。</span><span class="sxs-lookup"><span data-stu-id="79258-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="79258-125">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="79258-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="79258-126">在“预缴税金代码”字段中，选择预缴税金代码。</span><span class="sxs-lookup"><span data-stu-id="79258-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="79258-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="79258-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="79258-128">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="79258-128">Click Save.</span></span>


