---
title: "用于防止为零售产品打折的选项"
description: "零售商可能出于多种原因不希望 POS 中某些产品在促销或销售期间不打折。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: eaee79e2a20ab443cf3779e8499bf29d63ad3dfc
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2018

---

# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="17e6d-103">用于防止为零售产品打折的选项</span><span class="sxs-lookup"><span data-stu-id="17e6d-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17e6d-104">零售商可能出于多种原因不希望 POS 中某些产品在促销或销售期间不打折。</span><span class="sxs-lookup"><span data-stu-id="17e6d-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="17e6d-105">可通过以下选项（位于所发布产品的**零售**选项卡上）将产品配置为阻止全部折扣或手动折扣。</span><span class="sxs-lookup"><span data-stu-id="17e6d-105">The following options, which can be found on the **Retail** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="17e6d-106">也可以从零售类别层次结构的类别级别指定这些设置。</span><span class="sxs-lookup"><span data-stu-id="17e6d-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

<span data-ttu-id="17e6d-107">**阻止所有折扣**：选择此选项将阻止为此产品应用所有类型的折扣。</span><span class="sxs-lookup"><span data-stu-id="17e6d-107">**Prevent all discounts**: Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="17e6d-108">包括促销，如组合购买和阈值折扣，以及 POS 用户执行销售期间应用的手动行和交易记录折扣。</span><span class="sxs-lookup"><span data-stu-id="17e6d-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>

<span data-ttu-id="17e6d-109">**阻止手动折扣**：选择此选项将仅阻止 POS 用户执行销售期间应用的手动行和交易记录折扣。</span><span class="sxs-lookup"><span data-stu-id="17e6d-109">**Prevent manual discounts**: Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="17e6d-110">选择了此选项的产品仍然有资格享受促销，如组合购买和数量以及阈值折扣。</span><span class="sxs-lookup"><span data-stu-id="17e6d-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

<span data-ttu-id="17e6d-111">**注意**：这些设置不限制价格覆盖操作，因为此操作设置基础价格，不被视为折扣。</span><span class="sxs-lookup"><span data-stu-id="17e6d-111">**Note**: These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>  

<span data-ttu-id="17e6d-112">[![“阻止折扣”字段](./media/prevent discounts.png)](./media/prevent discounts.png)</span><span class="sxs-lookup"><span data-stu-id="17e6d-112">[![prevent discounts field](./media/prevent discounts.png)](./media/prevent discounts.png)</span></span>

