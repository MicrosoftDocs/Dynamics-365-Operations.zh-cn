---
title: 设置折旧帐簿（2016 年 5 月）
description: 此任务指南将创建新的折旧帐簿并将其与固定资产组关联。
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
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839849"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="7b1da-103">设置折旧帐簿（2016 年 5 月）</span><span class="sxs-lookup"><span data-stu-id="7b1da-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b1da-104">此任务指南将创建新的折旧帐簿并将其与固定资产组关联。</span><span class="sxs-lookup"><span data-stu-id="7b1da-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="7b1da-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="7b1da-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="7b1da-106">创建折旧帐簿</span><span class="sxs-lookup"><span data-stu-id="7b1da-106">Create a depreciation book</span></span>
1. <span data-ttu-id="7b1da-107">转到“固定资产”>“设置”>“折旧帐簿”。</span><span class="sxs-lookup"><span data-stu-id="7b1da-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="7b1da-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7b1da-108">Click New.</span></span>
3. <span data-ttu-id="7b1da-109">在“折旧帐簿”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7b1da-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="7b1da-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7b1da-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7b1da-111">选中或取消选中“计算折旧”复选框。</span><span class="sxs-lookup"><span data-stu-id="7b1da-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="7b1da-112">在“折旧模板”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="7b1da-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7b1da-113">在列表中，查找并选择所需折旧模板。</span><span class="sxs-lookup"><span data-stu-id="7b1da-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="7b1da-114">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7b1da-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7b1da-115">在“备选折旧模板”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="7b1da-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="7b1da-116">在列表中，选择所需折旧模板。</span><span class="sxs-lookup"><span data-stu-id="7b1da-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="7b1da-117">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7b1da-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7b1da-118">异常折旧模板用于异常情况下资产的额外折旧。</span><span class="sxs-lookup"><span data-stu-id="7b1da-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="7b1da-119">例如，您可以使用此来记录自然灾害导致的折旧。</span><span class="sxs-lookup"><span data-stu-id="7b1da-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="7b1da-120">选中或取消选中“使用基本调整创建折旧调整”复选框。</span><span class="sxs-lookup"><span data-stu-id="7b1da-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="7b1da-121">在“日历”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="7b1da-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="7b1da-122">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7b1da-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="7b1da-123">将折旧帐簿与固定资产组关联</span><span class="sxs-lookup"><span data-stu-id="7b1da-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="7b1da-124">单击“固定资产组”。</span><span class="sxs-lookup"><span data-stu-id="7b1da-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="7b1da-125">在“固定资产组”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="7b1da-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7b1da-126">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="7b1da-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7b1da-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7b1da-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7b1da-128">在“折旧惯例”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="7b1da-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="7b1da-129">在“使用年限”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7b1da-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="7b1da-130">请注意，“折旧期间”字段值将在设置使用年限后计算。</span><span class="sxs-lookup"><span data-stu-id="7b1da-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

