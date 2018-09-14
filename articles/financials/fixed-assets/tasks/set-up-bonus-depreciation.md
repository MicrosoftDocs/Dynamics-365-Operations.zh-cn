--- 
title: "设置额外折旧"
description: "此过程显示如何创建特殊折旧补偿并将其与固定资产帐簿关联。"
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6bbd6b78d05fcc9d95f6e6409db2619a210ad760
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-bonus-depreciation"></a><span data-ttu-id="07b68-103">设置额外折旧</span><span class="sxs-lookup"><span data-stu-id="07b68-103">Set up bonus depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07b68-104">此过程显示如何创建特殊折旧补偿并将其与固定资产帐簿关联。</span><span class="sxs-lookup"><span data-stu-id="07b68-104">This procedure shows how to create a special depreciation allowance and associate it with a fixed asset book.</span></span> <span data-ttu-id="07b68-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="07b68-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-special-depreciation-allowance"></a><span data-ttu-id="07b68-106">创建特殊折旧补偿</span><span class="sxs-lookup"><span data-stu-id="07b68-106">Create a special depreciation allowance</span></span>
1. <span data-ttu-id="07b68-107">转到“固定资产”>“设置”>“特殊折旧补偿”。</span><span class="sxs-lookup"><span data-stu-id="07b68-107">Go to Fixed assets > Setup > Special depreciation allowance.</span></span>
2. <span data-ttu-id="07b68-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="07b68-108">Click New.</span></span>
3. <span data-ttu-id="07b68-109">在“特殊折旧补偿”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07b68-109">In the Special depreciation allowance field, type a value.</span></span>
4. <span data-ttu-id="07b68-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="07b68-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="07b68-111">在“百分比”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="07b68-111">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="07b68-112">如果尚未指示百分比，则设置金额。</span><span class="sxs-lookup"><span data-stu-id="07b68-112">If a percentage was not indicated, set an amount.</span></span>  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a><span data-ttu-id="07b68-113">将特殊折旧补偿与固定资产组帐簿关联</span><span class="sxs-lookup"><span data-stu-id="07b68-113">Associate a special depreciation allowance with a fixed asset group book</span></span>
1. <span data-ttu-id="07b68-114">转到“固定资产”>“设置”>“固定资产组”。</span><span class="sxs-lookup"><span data-stu-id="07b68-114">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="07b68-115">在列表中，选择与特殊折旧补偿关联的固定资产组。</span><span class="sxs-lookup"><span data-stu-id="07b68-115">In the list, select the fixed asset group associated with the special depreciation allowance.</span></span>
3. <span data-ttu-id="07b68-116">单击“帐簿”。</span><span class="sxs-lookup"><span data-stu-id="07b68-116">Click Books.</span></span>
4. <span data-ttu-id="07b68-117">在列表中，选择与特殊折旧补偿关联的帐簿。</span><span class="sxs-lookup"><span data-stu-id="07b68-117">In the list, select the book that is associated with the special depreciation allowance.</span></span>
5. <span data-ttu-id="07b68-118">单击特殊折旧补偿。</span><span class="sxs-lookup"><span data-stu-id="07b68-118">Click Special depreciation allowance.</span></span>
6. <span data-ttu-id="07b68-119">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="07b68-119">Click New.</span></span>
7. <span data-ttu-id="07b68-120">在“特殊折旧补偿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="07b68-120">In the Special depreciation allowance field, enter or select a value.</span></span>
    * <span data-ttu-id="07b68-121">百分比或金额默认值来自特殊折旧补偿设置。</span><span class="sxs-lookup"><span data-stu-id="07b68-121">The default for Percentage or Amount comes from the special depreciation allowance setup.</span></span>  
8. <span data-ttu-id="07b68-122">在“优先”字段，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="07b68-122">In the Priority field, enter a number.</span></span>


