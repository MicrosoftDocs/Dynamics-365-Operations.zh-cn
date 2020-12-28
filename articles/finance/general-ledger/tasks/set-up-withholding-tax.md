---
title: 设置预缴税金
description: 本主题说明如何设置预缴税金。
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfa1b9e43a5745eb5b5c442998597319f196f23f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440663"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="f2c0e-103">设置预缴税金</span><span class="sxs-lookup"><span data-stu-id="f2c0e-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2c0e-104">本主题说明如何设置预缴税金。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="f2c0e-105">*预缴税金* 是针对供应商的一种不创建增值税交易记录的税金。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="f2c0e-106">对供应商付款计算的预缴税金是一种负债。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="f2c0e-107">因此，在过帐预缴税金时，只有资产负债表科目或负债科目是有效科目。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="f2c0e-108">此任务指南演示如何设置预缴税金。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="f2c0e-109">转到 **导航窗格 > 模块 > 纳税 > 间接税 > 预缴税金 > 预缴税金代码**。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="f2c0e-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-110">Select **New**.</span></span>
3. <span data-ttu-id="f2c0e-111">在 **预缴税金代码** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="f2c0e-112">在 **预缴税金名称** 字段中，输入预缴税金代码的名称。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="f2c0e-113">在 **主科目** 字段中，选择将预缴应交税金过帐的主科目。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="f2c0e-114">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-114">Select **Save**.</span></span>
7. <span data-ttu-id="f2c0e-115">选择 **数值**，然后在列表中标记所需记录。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="f2c0e-116">在 **数值** 字段中，输入用于计算预缴税金的百分比。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="f2c0e-117">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-117">Select **Save**.</span></span>
10. <span data-ttu-id="f2c0e-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-118">Close the page.</span></span>
11. <span data-ttu-id="f2c0e-119">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-119">Select **Save**.</span></span>
12. <span data-ttu-id="f2c0e-120">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-120">Close the page.</span></span>
13. <span data-ttu-id="f2c0e-121">转到 **导航窗格 > 模块 > 纳税 > 间接税 > 预缴税金 > 预缴税金组**。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="f2c0e-122">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-122">Select **New**.</span></span>
15. <span data-ttu-id="f2c0e-123">在 **预缴税金组** 字段中，输入预缴税金组的标识。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="f2c0e-124">在 **描述** 字段中，输入预缴税金组的名称。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="f2c0e-125">在 **预缴税金代码** 字段中，选择预缴税金代码。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="f2c0e-126">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-126">Select **Save**.</span></span>
19. <span data-ttu-id="f2c0e-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f2c0e-127">Close the page.</span></span>

