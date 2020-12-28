---
title: 设置价值模型
description: 此过程显示如何创建新固定资产帐簿并将其与固定资产组关联。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a59bafe3099b50d34bdd9e125cfb7f43d219dcc6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440815"
---
# <a name="set-up-value-models"></a><span data-ttu-id="7e51e-103">设置价值模型</span><span class="sxs-lookup"><span data-stu-id="7e51e-103">Set up value models</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e51e-104">此过程显示如何创建新固定资产帐簿并将其与固定资产组关联。</span><span class="sxs-lookup"><span data-stu-id="7e51e-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="7e51e-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="7e51e-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="7e51e-106">创建帐簿</span><span class="sxs-lookup"><span data-stu-id="7e51e-106">Create a book</span></span>
1. <span data-ttu-id="7e51e-107">转到“固定资产”>“设置”>“帐簿”。</span><span class="sxs-lookup"><span data-stu-id="7e51e-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="7e51e-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7e51e-108">Click New.</span></span>
3. <span data-ttu-id="7e51e-109">在“帐簿”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7e51e-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="7e51e-110">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7e51e-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="7e51e-111">如果选择“计算折旧”，关联资产帐簿将包含于折旧方案中。</span><span class="sxs-lookup"><span data-stu-id="7e51e-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="7e51e-112">如果未选择它，资产帐簿将不自动折旧。</span><span class="sxs-lookup"><span data-stu-id="7e51e-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="7e51e-113">在“计算折旧”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="7e51e-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="7e51e-114">在“折旧模板”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7e51e-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="7e51e-115">备选折旧模板也称作折旧转换方法。</span><span class="sxs-lookup"><span data-stu-id="7e51e-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="7e51e-116">当备选模板计算等于或大于默认折旧模板的折旧金额时，折旧方案将切换到此模板。</span><span class="sxs-lookup"><span data-stu-id="7e51e-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="7e51e-117">异常折旧模板用于异常情况下资产的额外折旧。</span><span class="sxs-lookup"><span data-stu-id="7e51e-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="7e51e-118">例如，您可以使用此来记录自然灾害导致的折旧。</span><span class="sxs-lookup"><span data-stu-id="7e51e-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="7e51e-119">如果选择“使用基础调整创建折旧调整”，在资产价值更新时将自动创建折旧调整。</span><span class="sxs-lookup"><span data-stu-id="7e51e-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="7e51e-120">如果未选择它，更新资产价值将只影响后面的折旧计算。</span><span class="sxs-lookup"><span data-stu-id="7e51e-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="7e51e-121">在“使用基本调整创建折旧调整”字段中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="7e51e-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="7e51e-122">默认情况下，固定资产帐簿交易记录将过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="7e51e-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="7e51e-123">可以通过将“过帐到总帐”字段设置为“否”，为帐簿禁用过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="7e51e-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="7e51e-124">不过帐到总帐的帐簿通常用于报税用途。</span><span class="sxs-lookup"><span data-stu-id="7e51e-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="7e51e-125">这样您的灵活性更高，可以删除资产帐簿的历史交易信息，因为这些信息尚未提交给总帐。</span><span class="sxs-lookup"><span data-stu-id="7e51e-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="7e51e-126">如果帐簿过帐到总帐，则“过帐层”为“当前层”，否则为“无”。</span><span class="sxs-lookup"><span data-stu-id="7e51e-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="7e51e-127">如果您需要将此帐簿的交易过帐到不同层，则更新过帐层。</span><span class="sxs-lookup"><span data-stu-id="7e51e-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="7e51e-128">在“日历”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7e51e-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="7e51e-129">派生帐簿将把交易同时过帐到不同帐簿。</span><span class="sxs-lookup"><span data-stu-id="7e51e-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="7e51e-130">可以使用主要帐簿创建交易，并在过帐期间将一模一样的交易副本过帐到衍生帐簿。</span><span class="sxs-lookup"><span data-stu-id="7e51e-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="7e51e-131">不对衍生帐簿交易进行重新计算，所以不应将其用于折旧交易。</span><span class="sxs-lookup"><span data-stu-id="7e51e-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="7e51e-132">将帐簿与固定资产组关联</span><span class="sxs-lookup"><span data-stu-id="7e51e-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="7e51e-133">单击“固定资产组”。</span><span class="sxs-lookup"><span data-stu-id="7e51e-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="7e51e-134">在“固定资产组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="7e51e-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="7e51e-135">在“使用年限”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="7e51e-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="7e51e-136">请注意，在设置使用年限后，计算“折旧期间”。</span><span class="sxs-lookup"><span data-stu-id="7e51e-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="7e51e-137">您可以为税务目的将折扣惯例设置为必需。</span><span class="sxs-lookup"><span data-stu-id="7e51e-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  

