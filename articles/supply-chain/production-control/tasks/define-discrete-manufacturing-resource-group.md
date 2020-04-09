---
title: 定义离散制造资源组
description: 一个资源组通常对应于工作单元里的某个物理组织的一组操作资源，由生产车间的黄线定义。
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01b797aa97e73cbe112c37a1efcd1e759730bc24
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149105"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="135be-103">定义离散制造资源组</span><span class="sxs-lookup"><span data-stu-id="135be-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="135be-104">一个资源组通常对应于工作单元里的某个物理组织的一组操作资源，由生产车间的黄线定义。</span><span class="sxs-lookup"><span data-stu-id="135be-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="135be-105">此程序说明如何在离散化生产中定义一个资源组。</span><span class="sxs-lookup"><span data-stu-id="135be-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="135be-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="135be-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="135be-107">转到“资源组”。</span><span class="sxs-lookup"><span data-stu-id="135be-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="135be-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="135be-108">Click New.</span></span>
3. <span data-ttu-id="135be-109">在“资源组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="135be-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="135be-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="135be-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="135be-111">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="135be-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="135be-112">在“生产单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="135be-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="135be-113">定义默认操作参数</span><span class="sxs-lookup"><span data-stu-id="135be-113">Define default operational parameters</span></span>
1. <span data-ttu-id="135be-114">展开“操作”部分。</span><span class="sxs-lookup"><span data-stu-id="135be-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="135be-115">在“废料百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="135be-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="135be-116">在“创建类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="135be-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="135be-117">在“运行时间类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="135be-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="135be-118">在“操作安排百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="135be-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="135be-119">定义操作时间</span><span class="sxs-lookup"><span data-stu-id="135be-119">Define operating hours</span></span>
1. <span data-ttu-id="135be-120">展开“日历”部分。</span><span class="sxs-lookup"><span data-stu-id="135be-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="135be-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="135be-121">Click Add.</span></span>
3. <span data-ttu-id="135be-122">在“日历”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="135be-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="135be-123">添加操作资源</span><span class="sxs-lookup"><span data-stu-id="135be-123">Add operations resources</span></span>
1. <span data-ttu-id="135be-124">展开“资源”部分。</span><span class="sxs-lookup"><span data-stu-id="135be-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="135be-125">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="135be-125">Click Add.</span></span>
3. <span data-ttu-id="135be-126">在“资源”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="135be-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="135be-127">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="135be-127">Click Add.</span></span>
5. <span data-ttu-id="135be-128">在“资源”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="135be-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="135be-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="135be-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="135be-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="135be-130">In the list, click the link in the selected row.</span></span>

