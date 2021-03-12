---
title: 复制配方
description: 此过程重点是创建包括相同的成分作为现有配方的配方，不过差异很小。
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0643209f7ef5090684db693bea2483fadcf3760b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998770"
---
# <a name="copy-a-formula"></a><span data-ttu-id="51c3e-103">复制配方</span><span class="sxs-lookup"><span data-stu-id="51c3e-103">Copy a formula</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51c3e-104">此过程重点是创建包括相同的成分作为现有配方的配方，不过差异很小。</span><span class="sxs-lookup"><span data-stu-id="51c3e-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="51c3e-105">若要创建配方行，您可以使用“复制”功能复制具有大多数所需成分的现有配方。</span><span class="sxs-lookup"><span data-stu-id="51c3e-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="51c3e-106">然后可以对新版本中各行进行必要的更改。</span><span class="sxs-lookup"><span data-stu-id="51c3e-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="51c3e-107">通过使用“复制”功能，您不必创建几乎完全相同的多个配方。</span><span class="sxs-lookup"><span data-stu-id="51c3e-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="51c3e-108">使用 USP2 公司演示数据创建此任务。</span><span class="sxs-lookup"><span data-stu-id="51c3e-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="51c3e-109">创建配方</span><span class="sxs-lookup"><span data-stu-id="51c3e-109">Create a formula</span></span>
1. <span data-ttu-id="51c3e-110">转到“产品信息管理”>“物料清单和配方”>“配方”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="51c3e-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-111">Click New.</span></span>
3. <span data-ttu-id="51c3e-112">在“配方”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="51c3e-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="51c3e-113">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="51c3e-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="51c3e-114">为该配方键入有意义的名称。</span><span class="sxs-lookup"><span data-stu-id="51c3e-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="51c3e-115">在“位置”字段中，单击下拉按钮打开查询。</span><span class="sxs-lookup"><span data-stu-id="51c3e-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="51c3e-116">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="51c3e-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="51c3e-117">在“物料组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="51c3e-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="51c3e-118">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="51c3e-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="51c3e-119">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="51c3e-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="51c3e-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="51c3e-121">复制配方行</span><span class="sxs-lookup"><span data-stu-id="51c3e-121">Copy formula lines</span></span>
1. <span data-ttu-id="51c3e-122">在操作窗格上，单击“配方”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="51c3e-123">单击“复制”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-123">Click Copy.</span></span>
3. <span data-ttu-id="51c3e-124">在“物料编号”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="51c3e-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="51c3e-125">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="51c3e-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="51c3e-126">在“配方版本”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="51c3e-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="51c3e-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="51c3e-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="51c3e-128">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="51c3e-129">调整复制的配方行</span><span class="sxs-lookup"><span data-stu-id="51c3e-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="51c3e-130">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="51c3e-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="51c3e-131">单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-131">Click Delete.</span></span>
3. <span data-ttu-id="51c3e-132">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="51c3e-133">审核配方</span><span class="sxs-lookup"><span data-stu-id="51c3e-133">Approve formula</span></span>
1. <span data-ttu-id="51c3e-134">在操作窗格上，单击“配方”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="51c3e-135">单击“审核配方”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-135">Click Approve formula.</span></span>
3. <span data-ttu-id="51c3e-136">在“审核人”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="51c3e-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="51c3e-137">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="51c3e-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="51c3e-138">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-138">Click Select.</span></span>
6. <span data-ttu-id="51c3e-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="51c3e-139">Click OK.</span></span>

