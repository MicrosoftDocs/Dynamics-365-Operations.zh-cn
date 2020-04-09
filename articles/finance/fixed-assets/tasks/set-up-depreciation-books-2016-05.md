---
title: 设置折旧账簿
description: 此过程将逐步完成创建新折旧账簿并将其与固定资产组关联的流程。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03f915fa91e0eeff2f26ab9a60bbd5118317e853
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154590"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="0ae9d-103">设置折旧账簿</span><span class="sxs-lookup"><span data-stu-id="0ae9d-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ae9d-104">此过程将逐步完成创建新折旧账簿并将其与固定资产组关联的流程。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="0ae9d-105">创建折旧帐簿</span><span class="sxs-lookup"><span data-stu-id="0ae9d-105">Create a depreciation book</span></span>
1. <span data-ttu-id="0ae9d-106">转到“固定资产”>“设置”>“折旧帐簿”。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="0ae9d-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-107">Click New.</span></span>
3. <span data-ttu-id="0ae9d-108">在“折旧帐簿”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="0ae9d-109">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0ae9d-110">选中或取消选中“计算折旧”复选框。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="0ae9d-111">在“折旧模板”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0ae9d-112">在列表中，查找并选择所需折旧模板。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="0ae9d-113">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0ae9d-114">在“备选折旧模板”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="0ae9d-115">在列表中，选择所需折旧模板。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="0ae9d-116">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0ae9d-117">异常折旧模板用于异常情况下资产的额外折旧。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="0ae9d-118">例如，您可以使用此来记录自然灾害导致的折旧。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="0ae9d-119">选中或取消选中“使用基本调整创建折旧调整”复选框。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="0ae9d-120">在“日历”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="0ae9d-121">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="0ae9d-122">将折旧帐簿与固定资产组关联</span><span class="sxs-lookup"><span data-stu-id="0ae9d-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="0ae9d-123">单击“固定资产组”。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="0ae9d-124">在“固定资产组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0ae9d-125">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0ae9d-126">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0ae9d-127">在“折旧惯例”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="0ae9d-128">在“使用年限”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="0ae9d-129">请注意，“折旧期间”字段值将在设置使用年限后计算。</span><span class="sxs-lookup"><span data-stu-id="0ae9d-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

