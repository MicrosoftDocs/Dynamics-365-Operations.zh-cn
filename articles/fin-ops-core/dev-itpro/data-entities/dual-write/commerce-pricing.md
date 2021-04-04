---
title: 对 Dynamics 365 Sales 使用 Dynamics 365 Commerce 定价引擎
description: 本主题介绍如何在 Dynamics 365 Sales 中使用 Microsoft Dynamics 365 Commerce 定价引擎创建销售报价单。
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: cd784bb37eddfc74699d1070eab453a3b527201a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560265"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="e191a-103">对 Dynamics 365 Sales 使用 Dynamics 365 Commerce 定价引擎</span><span class="sxs-lookup"><span data-stu-id="e191a-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e191a-104">本主题介绍如何在 Dynamics 365 Sales 中使用 Microsoft Dynamics 365 Commerce 定价引擎创建销售报价单。</span><span class="sxs-lookup"><span data-stu-id="e191a-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="e191a-105">Dynamics 365 Commerce 定价引擎支持大多数企业对消费者 (B2C) 定价方案，如商店级定价、基于隶属关系和基于会员制的定价、组合折扣、数量折扣和阈值折扣。</span><span class="sxs-lookup"><span data-stu-id="e191a-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="e191a-106">定价引擎使用复杂的规则来确定给定报价单或订单的最佳价格。</span><span class="sxs-lookup"><span data-stu-id="e191a-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="e191a-107">使用[双写入](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview)时，您可以根据需要选择三个选项。</span><span class="sxs-lookup"><span data-stu-id="e191a-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="e191a-108">您可以使用 Dynamics 365 Sales 中价格列表中的静态定价、Dynamics 365 Supply Chain Management 中的定价引擎或 Dynamics 365 Commerce 中的定价引擎。</span><span class="sxs-lookup"><span data-stu-id="e191a-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="e191a-109">在这些选项中，Commerce 定价引擎最适合 B2C 方案。</span><span class="sxs-lookup"><span data-stu-id="e191a-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="e191a-110">在 Sales 中使用 Commerce 定价引擎</span><span class="sxs-lookup"><span data-stu-id="e191a-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="e191a-111">现在，Commerce 定价引擎只能用于在 Sales 中创建报价单。</span><span class="sxs-lookup"><span data-stu-id="e191a-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="e191a-112">销售订单尚不能与 Commerce 定价引擎集成。</span><span class="sxs-lookup"><span data-stu-id="e191a-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="e191a-113">当用户在 Sales 中启动报价单时，双写入框架会将报价单详细信息复制到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="e191a-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="e191a-114">将把对在 Sales 中现有报价单行或任何新添加的报价单行的任何更改都复制到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="e191a-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="e191a-115">当用户要使用 Commerce 定价引擎对报价单定价时，可以选择 **报价单** 根据 Commerce 定价引擎更新报价单的价格。</span><span class="sxs-lookup"><span data-stu-id="e191a-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="e191a-116">然后同时在 Sales 和 Commerce 中自动更新价格。</span><span class="sxs-lookup"><span data-stu-id="e191a-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e191a-117">先决条件</span><span class="sxs-lookup"><span data-stu-id="e191a-117">Prerequisites</span></span>

- <span data-ttu-id="e191a-118">必须先执行[双写入中的目标客户到现金](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)中的步骤，才能使用 Sales 中的 Commerce 定价引擎。</span><span class="sxs-lookup"><span data-stu-id="e191a-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="e191a-119">您必须按照以下步骤关闭手动输入的贸易协议评估：</span><span class="sxs-lookup"><span data-stu-id="e191a-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="e191a-120">在 Commerce 环境中，转至 **应收帐款 \> 设置 \> 应收帐款参数**。</span><span class="sxs-lookup"><span data-stu-id="e191a-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="e191a-121">在 **价格** 选项卡上的 **贸易协议评估** 快速选项卡上，清除 **手动输入** 复选框。</span><span class="sxs-lookup"><span data-stu-id="e191a-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e191a-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="e191a-122">Additional resources</span></span>

[<span data-ttu-id="e191a-123">双写入中的目标客户到现金</span><span class="sxs-lookup"><span data-stu-id="e191a-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]