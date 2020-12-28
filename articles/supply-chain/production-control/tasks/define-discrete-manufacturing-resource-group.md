---
title: 定义离散制造资源组
description: 一个资源组通常对应于工作单元里的某个物理组织的一组操作资源，由生产车间的黄线定义。
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eaccb566c04d6d4b91ea8cb046931e750a4c6eed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422702"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="ebf95-103">定义离散制造资源组</span><span class="sxs-lookup"><span data-stu-id="ebf95-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ebf95-104">一个资源组通常对应于工作单元里的某个物理组织的一组操作资源，由生产车间的黄线定义。</span><span class="sxs-lookup"><span data-stu-id="ebf95-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="ebf95-105">此程序说明如何在离散化生产中定义一个资源组。</span><span class="sxs-lookup"><span data-stu-id="ebf95-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="ebf95-106">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="ebf95-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="ebf95-107">转到“资源组”。</span><span class="sxs-lookup"><span data-stu-id="ebf95-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="ebf95-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ebf95-108">Click New.</span></span>
3. <span data-ttu-id="ebf95-109">在“资源组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf95-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="ebf95-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf95-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ebf95-111">在“站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf95-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="ebf95-112">在“生产单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf95-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="ebf95-113">定义默认操作参数</span><span class="sxs-lookup"><span data-stu-id="ebf95-113">Define default operational parameters</span></span>
1. <span data-ttu-id="ebf95-114">展开“操作”部分。</span><span class="sxs-lookup"><span data-stu-id="ebf95-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="ebf95-115">在“废料百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ebf95-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="ebf95-116">在“创建类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf95-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="ebf95-117">在“运行时间类别”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf95-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="ebf95-118">在“操作安排百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="ebf95-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="ebf95-119">定义操作时间</span><span class="sxs-lookup"><span data-stu-id="ebf95-119">Define operating hours</span></span>
1. <span data-ttu-id="ebf95-120">展开“日历”部分。</span><span class="sxs-lookup"><span data-stu-id="ebf95-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="ebf95-121">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ebf95-121">Click Add.</span></span>
3. <span data-ttu-id="ebf95-122">在“日历”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf95-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="ebf95-123">添加操作资源</span><span class="sxs-lookup"><span data-stu-id="ebf95-123">Add operations resources</span></span>
1. <span data-ttu-id="ebf95-124">展开“资源”部分。</span><span class="sxs-lookup"><span data-stu-id="ebf95-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="ebf95-125">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ebf95-125">Click Add.</span></span>
3. <span data-ttu-id="ebf95-126">在“资源”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf95-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="ebf95-127">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="ebf95-127">Click Add.</span></span>
5. <span data-ttu-id="ebf95-128">在“资源”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ebf95-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="ebf95-129">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ebf95-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ebf95-130">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ebf95-130">In the list, click the link in the selected row.</span></span>

