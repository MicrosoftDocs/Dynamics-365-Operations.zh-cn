---
title: 为日记帐启用延迟税金计算
description: 此主题介绍如何启用延迟税金计算功能以在有大量日记帐行时帮助提高税金计算的性能。
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d842b60b3cca8c29b281ab4a6a1b6c3b0bad3684
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236714"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="690bd-103">为日记帐启用延迟税金计算</span><span class="sxs-lookup"><span data-stu-id="690bd-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="690bd-104">本主题说明如何延迟日记帐的销售税计算。</span><span class="sxs-lookup"><span data-stu-id="690bd-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="690bd-105">当日记帐行很多时，此功能有助于提高税金计算的性能。</span><span class="sxs-lookup"><span data-stu-id="690bd-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="690bd-106">默认情况下，每当更新与税相关的字段时，都会计算日记帐行上的销售税金额。</span><span class="sxs-lookup"><span data-stu-id="690bd-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="690bd-107">这些字段包括销售税组和物料销售税组的字段。</span><span class="sxs-lookup"><span data-stu-id="690bd-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="690bd-108">日记帐行的任何更新都会导致重新计算所有日记帐行的税额。</span><span class="sxs-lookup"><span data-stu-id="690bd-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="690bd-109">尽管此行为可以帮助用户实时查看税额，但是如果日记帐行的数量很大，也可能影响性能。</span><span class="sxs-lookup"><span data-stu-id="690bd-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="690bd-110">延迟税金计算功能使您可以延迟日记帐的税金计算，从而帮助解决性能问题。</span><span class="sxs-lookup"><span data-stu-id="690bd-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="690bd-111">开启此功能时，则仅当用户选择 **销售税** 或过帐日记帐时，才会计算税额。</span><span class="sxs-lookup"><span data-stu-id="690bd-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="690bd-112">您可以在三个级别上延迟销售税的计算：</span><span class="sxs-lookup"><span data-stu-id="690bd-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="690bd-113">法人</span><span class="sxs-lookup"><span data-stu-id="690bd-113">Legal entity</span></span>
- <span data-ttu-id="690bd-114">日记帐名称</span><span class="sxs-lookup"><span data-stu-id="690bd-114">Journal name</span></span>
- <span data-ttu-id="690bd-115">日记帐标题</span><span class="sxs-lookup"><span data-stu-id="690bd-115">Journal header</span></span>

<span data-ttu-id="690bd-116">系统优先考虑日记帐标头的设置。</span><span class="sxs-lookup"><span data-stu-id="690bd-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="690bd-117">默认情况下，此设置来自日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="690bd-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="690bd-118">默认情况下，创建日记帐名称时，日记帐名称的设置从 **总帐参数** 页面上的设置获取。</span><span class="sxs-lookup"><span data-stu-id="690bd-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="690bd-119">以下各节说明如何为法人、日记帐名称和日记帐标头打开延迟税金计算。</span><span class="sxs-lookup"><span data-stu-id="690bd-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="690bd-120">在法人级别启用延迟税金计算</span><span class="sxs-lookup"><span data-stu-id="690bd-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="690bd-121">转到 **总帐 \> 分类帐设置 \> 总帐参数**。</span><span class="sxs-lookup"><span data-stu-id="690bd-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="690bd-122">在 **销售税** 选项卡，在 **常规** 快速选项卡，将 **延迟税金计算** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="690bd-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![总帐参数图像](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="690bd-124">在日记帐名称级别启用延迟税金计算</span><span class="sxs-lookup"><span data-stu-id="690bd-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="690bd-125">转到 **总帐 \> 日记帐设置 \> 日记帐名称**。</span><span class="sxs-lookup"><span data-stu-id="690bd-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="690bd-126">在 **常规** 快速选项卡上，在 **销售税** 部分，将 **延迟税金计算** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="690bd-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![日记帐名称图像](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="690bd-128">在日记帐标头级别启用延迟税金计算</span><span class="sxs-lookup"><span data-stu-id="690bd-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="690bd-129">转到 **总帐 \> 日记帐条目 \> 普通日记帐**。</span><span class="sxs-lookup"><span data-stu-id="690bd-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="690bd-130">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="690bd-130">Select **New**.</span></span>
3. <span data-ttu-id="690bd-131">选择一个日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="690bd-131">Select a journal name.</span></span>
4. <span data-ttu-id="690bd-132">在 **设置** 选项卡上，将 **延迟税金计算** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="690bd-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![普通日记帐页面图像](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]