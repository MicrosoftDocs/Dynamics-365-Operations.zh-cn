---
title: 设置条码
description: 本文介绍如何在 Dynamics 365 Commerce 中使用条码。
author: jblucher
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1c395caedfce7efa0a087ff6944052958c72327e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804177"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="56725-103">设置条码</span><span class="sxs-lookup"><span data-stu-id="56725-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="56725-104">本文介绍如何在 Dynamics 365 Commerce 中使用条码。</span><span class="sxs-lookup"><span data-stu-id="56725-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="56725-105">您可以使用条码采购和销售产品、跟踪产品变型和设置客户和员工。</span><span class="sxs-lookup"><span data-stu-id="56725-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="56725-106">您还可以使用条码发货和批准优惠券、礼品卡和贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="56725-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="56725-107">您可以设置产品，以便具有标准条码或自定义公司内部条码。</span><span class="sxs-lookup"><span data-stu-id="56725-107">You can set up products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="56725-108">产品可以有多个条码。</span><span class="sxs-lookup"><span data-stu-id="56725-108">Products can have more than one bar code.</span></span> <span data-ttu-id="56725-109">例如，如果来自不同的制造商，则产品可能具有多个条码，或者，如果基于大小、样式或颜色的变量它具有款式。</span><span class="sxs-lookup"><span data-stu-id="56725-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="56725-110">条码可以包含产品的重量或价格。</span><span class="sxs-lookup"><span data-stu-id="56725-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="56725-111">条码掩码是用于创建条码的模板。</span><span class="sxs-lookup"><span data-stu-id="56725-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="56725-112">如果您为每个变型组合分配唯一条码，您可以在收银机上扫描条码，让程序确定出售的是哪种产品款式。</span><span class="sxs-lookup"><span data-stu-id="56725-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="56725-113">可以按款式收集和查看有关销售的统计。</span><span class="sxs-lookup"><span data-stu-id="56725-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="56725-114">可以为每个大小、颜色和样式组都分配一个可在条码中标识该组的唯一编号。</span><span class="sxs-lookup"><span data-stu-id="56725-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="56725-115">Commerce 使用条码掩码来自动为每种款式组合生成条码。</span><span class="sxs-lookup"><span data-stu-id="56725-115">Commerce uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="56725-116">如果存在多种大小、颜色和样式的情况下功能很有用，因为不断添加款式代码将显著增加组合的数量。</span><span class="sxs-lookup"><span data-stu-id="56725-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="56725-117">如果不使用此功能，必须手动将条码分配给表示产品变型的每个组合。</span><span class="sxs-lookup"><span data-stu-id="56725-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="56725-118">可以通过手动方式或自动方式来创建条码。</span><span class="sxs-lookup"><span data-stu-id="56725-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="56725-119">若要创建条码，请按照其列出的顺序完成以下任务。</span><span class="sxs-lookup"><span data-stu-id="56725-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="56725-120">[设置条码掩码字符](set-up-bar-code-masks.md)。</span><span class="sxs-lookup"><span data-stu-id="56725-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="56725-121">[设置条码掩码](set-up-bar-code-masks.md)。</span><span class="sxs-lookup"><span data-stu-id="56725-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="56725-122">配置条码设置。</span><span class="sxs-lookup"><span data-stu-id="56725-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="56725-123">[为产品创建条码](../supply-chain/pim/tasks/create-bar-code-product.md)。</span><span class="sxs-lookup"><span data-stu-id="56725-123">[Create bar codes for products](../supply-chain/pim/tasks/create-bar-code-product.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56725-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="56725-124">Additional resources</span></span>

[<span data-ttu-id="56725-125">设置条码掩码</span><span class="sxs-lookup"><span data-stu-id="56725-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]