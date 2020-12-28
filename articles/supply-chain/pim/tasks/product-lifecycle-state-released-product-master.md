---
title: 对已发布的基础产品分配产品生命周期状态
description: 此过程显示如何将产品生命周期状态分配给已发布的基础产品及其变型。
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c644f118e0bdb46b296cec7e4a3ea89031f2d52
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422851"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="7d666-103">对已发布的基础产品分配产品生命周期状态</span><span class="sxs-lookup"><span data-stu-id="7d666-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d666-104">此过程显示如何将产品生命周期状态分配给已发布的基础产品及其变型。</span><span class="sxs-lookup"><span data-stu-id="7d666-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="7d666-105">先决条件：您需要先播放任务指南“创建新的产品生命周期状态”以确保至少创建了一个产品生命周期状态，然后才可以播放此任务指南。</span><span class="sxs-lookup"><span data-stu-id="7d666-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="7d666-106">查找已发布的基础产品</span><span class="sxs-lookup"><span data-stu-id="7d666-106">Find a released product master</span></span>
1. <span data-ttu-id="7d666-107">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="7d666-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7d666-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="7d666-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="7d666-109">基础产品包含产品子类型基础产品。</span><span class="sxs-lookup"><span data-stu-id="7d666-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="7d666-110">更新生命周期状态</span><span class="sxs-lookup"><span data-stu-id="7d666-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="7d666-111">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="7d666-111">Click Edit.</span></span>
2. <span data-ttu-id="7d666-112">在“产品生命周期状态”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d666-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="7d666-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7d666-113">Click Save.</span></span>
4. <span data-ttu-id="7d666-114">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="7d666-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="7d666-115">如果选择“是”，与已发布基础产品具有相同原始状态的所有相关的已发布产品变型也会更新到新的产品生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="7d666-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="7d666-116">如果选择“否”，所有变型都会保留其实际状态。</span><span class="sxs-lookup"><span data-stu-id="7d666-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="7d666-117">具有与已发布基础产品不同的产品生命周期状态的变型不会更新。</span><span class="sxs-lookup"><span data-stu-id="7d666-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="7d666-118">验证变型的生命周期状态</span><span class="sxs-lookup"><span data-stu-id="7d666-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="7d666-119">单击“已发布的产品变型”。</span><span class="sxs-lookup"><span data-stu-id="7d666-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="7d666-120">请注意，所有变型均已从发布的基础产品继承所选生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="7d666-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="7d666-121">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="7d666-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="7d666-122">在“产品生命周期状态”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7d666-122">In the Product lifecycle state field, enter or select a value.</span></span>

