--- 
title: "设置折旧帐簿"
description: "此任务指南将创建新的折旧帐簿并将其与固定资产组关联。"
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d2001da7b3487a07a91abd406f74558916ac9f23
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="cf146-103">设置折旧帐簿</span><span class="sxs-lookup"><span data-stu-id="cf146-103">Set up depreciation books</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf146-104">此任务指南将创建新的折旧帐簿并将其与固定资产组关联。</span><span class="sxs-lookup"><span data-stu-id="cf146-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="cf146-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="cf146-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="cf146-106">创建折旧帐簿</span><span class="sxs-lookup"><span data-stu-id="cf146-106">Create a depreciation book</span></span>
1. <span data-ttu-id="cf146-107">转到“固定资产”>“设置”>“折旧帐簿”。</span><span class="sxs-lookup"><span data-stu-id="cf146-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="cf146-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cf146-108">Click New.</span></span>
3. <span data-ttu-id="cf146-109">在“折旧帐簿”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cf146-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="cf146-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cf146-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cf146-111">选中或取消选中“计算折旧”复选框。</span><span class="sxs-lookup"><span data-stu-id="cf146-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="cf146-112">在“折旧模板”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cf146-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cf146-113">在列表中，查找并选择所需折旧模板。</span><span class="sxs-lookup"><span data-stu-id="cf146-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="cf146-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cf146-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cf146-115">在“备选折旧模板”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cf146-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="cf146-116">在列表中，选择所需折旧模板。</span><span class="sxs-lookup"><span data-stu-id="cf146-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="cf146-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cf146-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cf146-118">异常折旧模板用于异常情况下资产的额外折旧。</span><span class="sxs-lookup"><span data-stu-id="cf146-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="cf146-119">例如，您可以使用此来记录自然灾害导致的折旧。</span><span class="sxs-lookup"><span data-stu-id="cf146-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="cf146-120">选中或取消选中“使用基本调整创建折旧调整”复选框。</span><span class="sxs-lookup"><span data-stu-id="cf146-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="cf146-121">在“日历”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cf146-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="cf146-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cf146-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="cf146-123">将折旧帐簿与固定资产组关联</span><span class="sxs-lookup"><span data-stu-id="cf146-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="cf146-124">单击“固定资产组”。</span><span class="sxs-lookup"><span data-stu-id="cf146-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="cf146-125">在“固定资产组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="cf146-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cf146-126">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cf146-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cf146-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cf146-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cf146-128">在“折旧惯例”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="cf146-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="cf146-129">在“使用年限”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="cf146-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="cf146-130">请注意，“折旧期间”字段值将在设置使用年限后计算。</span><span class="sxs-lookup"><span data-stu-id="cf146-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  


