--- 
title: "定义离散制造资源组"
description: "一个资源组通常对应于工作单元里的某个物理组织的一组操作资源，由生产车间的黄线定义。"
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 50733e34bbf14ae2cade6822105da4d8c2120d7d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="cfaba-103">定义离散制造资源组</span><span class="sxs-lookup"><span data-stu-id="cfaba-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cfaba-104">一个资源组通常对应于工作单元里的某个物理组织的一组操作资源，由生产车间的黄线定义。</span><span class="sxs-lookup"><span data-stu-id="cfaba-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="cfaba-105">此程序说明如何在离散化生产中定义一个资源组。</span><span class="sxs-lookup"><span data-stu-id="cfaba-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="cfaba-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="cfaba-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="cfaba-107">转到“资源组”。</span><span class="sxs-lookup"><span data-stu-id="cfaba-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="cfaba-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cfaba-108">Click New.</span></span>
3. <span data-ttu-id="cfaba-109">在“资源组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cfaba-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="cfaba-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cfaba-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cfaba-111">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cfaba-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="cfaba-112">在“生产单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cfaba-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="cfaba-113">定义默认操作参数</span><span class="sxs-lookup"><span data-stu-id="cfaba-113">Define default operational parameters</span></span>
1. <span data-ttu-id="cfaba-114">展开“操作”部分。</span><span class="sxs-lookup"><span data-stu-id="cfaba-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="cfaba-115">在“废料百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="cfaba-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="cfaba-116">在“创建类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cfaba-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="cfaba-117">在“运行时间类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cfaba-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="cfaba-118">在“操作安排百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="cfaba-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="cfaba-119">定义操作时间</span><span class="sxs-lookup"><span data-stu-id="cfaba-119">Define operating hours</span></span>
1. <span data-ttu-id="cfaba-120">展开“日历”部分。</span><span class="sxs-lookup"><span data-stu-id="cfaba-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="cfaba-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="cfaba-121">Click Add.</span></span>
3. <span data-ttu-id="cfaba-122">在“日历”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cfaba-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="cfaba-123">添加操作资源</span><span class="sxs-lookup"><span data-stu-id="cfaba-123">Add operations resources</span></span>
1. <span data-ttu-id="cfaba-124">展开“资源”部分。</span><span class="sxs-lookup"><span data-stu-id="cfaba-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="cfaba-125">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="cfaba-125">Click Add.</span></span>
3. <span data-ttu-id="cfaba-126">在“资源”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cfaba-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="cfaba-127">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="cfaba-127">Click Add.</span></span>
5. <span data-ttu-id="cfaba-128">在“资源”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cfaba-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="cfaba-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cfaba-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cfaba-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cfaba-130">In the list, click the link in the selected row.</span></span>


