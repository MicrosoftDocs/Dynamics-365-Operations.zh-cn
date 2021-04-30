---
title: 财务维度集
description: 本主题介绍了财务维度集并提供一些优化其用法的提示。
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864404"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="2de55-103">财务维度集</span><span class="sxs-lookup"><span data-stu-id="2de55-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2de55-104">本主题介绍了财务维度集并提供一些优化其用法的提示。</span><span class="sxs-lookup"><span data-stu-id="2de55-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="2de55-105">维度集是财务维度的已排序列表，可用于以用户定义的方式汇总总帐数据。</span><span class="sxs-lookup"><span data-stu-id="2de55-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="2de55-106">维度集的主要用途是定义试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="2de55-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="2de55-107">唯一的标准维度集是仅包含主科目的维度集。</span><span class="sxs-lookup"><span data-stu-id="2de55-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="2de55-108">使用 **财务维度集** 页面创建和管理财务维度集。</span><span class="sxs-lookup"><span data-stu-id="2de55-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="2de55-109">维度集平衡表</span><span class="sxs-lookup"><span data-stu-id="2de55-109">Dimension set balances</span></span>

<span data-ttu-id="2de55-110">维度集可以具有基于其财务维度的平衡表。</span><span class="sxs-lookup"><span data-stu-id="2de55-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="2de55-111">平衡表存在于总帐中，并且基于维集集定义。</span><span class="sxs-lookup"><span data-stu-id="2de55-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="2de55-112">汇总总帐数据中的平衡表以帮助在检索平衡表时（例如，当生成试算平衡表时）提高性能。</span><span class="sxs-lookup"><span data-stu-id="2de55-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="2de55-113">创建余额</span><span class="sxs-lookup"><span data-stu-id="2de55-113">Create balances</span></span>

<span data-ttu-id="2de55-114">使用 **创建平衡表** 按钮初始化当前没有平衡表的维度集的平衡表。</span><span class="sxs-lookup"><span data-stu-id="2de55-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="2de55-115">我们建议您限制具有平衡表的维度集的数量，因为平衡表更新会影响所有总帐过帐活动。</span><span class="sxs-lookup"><span data-stu-id="2de55-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="2de55-116">更新余额</span><span class="sxs-lookup"><span data-stu-id="2de55-116">Update balances</span></span>

<span data-ttu-id="2de55-117">使用 **更新平衡表** 按钮将最新的总帐过帐活动包括在平衡表中。</span><span class="sxs-lookup"><span data-stu-id="2de55-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="2de55-118">平衡表更新是简单的操作。</span><span class="sxs-lookup"><span data-stu-id="2de55-118">Balance updates are light operations.</span></span> <span data-ttu-id="2de55-119">它们必须仅处理自上次更新以来发生的总帐过帐活动。</span><span class="sxs-lookup"><span data-stu-id="2de55-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="2de55-120">显示试算平衡表会强制进行更新，以确保显示的平衡表是最新的。</span><span class="sxs-lookup"><span data-stu-id="2de55-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="2de55-121">考虑使用定期批处理作业，以便快速更新最常用的维度集。</span><span class="sxs-lookup"><span data-stu-id="2de55-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="2de55-122">通过这种方式，您可以最大程度地减少试用平衡表用户必须等待的时间。</span><span class="sxs-lookup"><span data-stu-id="2de55-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="2de55-123">重建余额</span><span class="sxs-lookup"><span data-stu-id="2de55-123">Rebuild balances</span></span>

<span data-ttu-id="2de55-124">使用 **重建平衡表** 按钮从头开始重新创建平衡表。</span><span class="sxs-lookup"><span data-stu-id="2de55-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="2de55-125">通过这种方式，您可以帮助确保它们与总帐中的数据匹配。</span><span class="sxs-lookup"><span data-stu-id="2de55-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="2de55-126">重建平衡表需要大量处理，通常不需要这样做。</span><span class="sxs-lookup"><span data-stu-id="2de55-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="2de55-127">如果您有需要定期重建平衡表的场景，我们建议您与客户支持联系。</span><span class="sxs-lookup"><span data-stu-id="2de55-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="2de55-128">客户支持可以帮助您确定为什么平衡表与总帐中的数据不匹配。</span><span class="sxs-lookup"><span data-stu-id="2de55-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="2de55-129">结算余额</span><span class="sxs-lookup"><span data-stu-id="2de55-129">Clear balances</span></span>

<span data-ttu-id="2de55-130">使用 **清除平衡表** 按钮删除平衡表并停止任何进一步更新。</span><span class="sxs-lookup"><span data-stu-id="2de55-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="2de55-131">维度集将不再对总帐过帐活动产生影响。</span><span class="sxs-lookup"><span data-stu-id="2de55-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="2de55-132">有关详细信息，请参阅[财务维度](financial-dimensions.md)。</span><span class="sxs-lookup"><span data-stu-id="2de55-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
