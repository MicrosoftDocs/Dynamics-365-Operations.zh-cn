---
title: 在线订单的税金计算错误
description: 本主题提供了故障排除指南，当在线订单上的税金计算错误或未正确设置销售行上的税组时，此指南可以提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7f71add679e1d24f80db8ce3990058b591128ec1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801403"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="b3f50-103">在线订单的税金计算错误</span><span class="sxs-lookup"><span data-stu-id="b3f50-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3f50-104">本主题提供了故障排除指南，当在线订单上的税金计算错误或未正确设置销售行上的税组时，此指南可以提供帮助。</span><span class="sxs-lookup"><span data-stu-id="b3f50-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="b3f50-105">说明</span><span class="sxs-lookup"><span data-stu-id="b3f50-105">Description</span></span>

<span data-ttu-id="b3f50-106">下达电子商务订单时，税额计算错误，或未正确设置销售行上的税组。</span><span class="sxs-lookup"><span data-stu-id="b3f50-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="b3f50-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="b3f50-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="b3f50-108">在 Commerce Headquarters 中配置零售商店的销售税</span><span class="sxs-lookup"><span data-stu-id="b3f50-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="b3f50-109">要在 Commerce Headquarters 中配置零售商店的销售税，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b3f50-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b3f50-110">转至 **Retail 和 Commerce \> 渠道 \> 所有商店**。</span><span class="sxs-lookup"><span data-stu-id="b3f50-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="b3f50-111">选择要为其配置销售税的商店。</span><span class="sxs-lookup"><span data-stu-id="b3f50-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="b3f50-112">在 **常规** 快速选项卡上，在 **销售税** 部分，配置商店的销售税信息。</span><span class="sxs-lookup"><span data-stu-id="b3f50-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="b3f50-113">对于从商店取货，税组来自选择要取货的商店。</span><span class="sxs-lookup"><span data-stu-id="b3f50-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="b3f50-114">有关详细信息，请参阅[设置商店的其他税金选项](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores)。</span><span class="sxs-lookup"><span data-stu-id="b3f50-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="b3f50-115">在 Commerce Headquarters 中配置客户地址的相应销售税</span><span class="sxs-lookup"><span data-stu-id="b3f50-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="b3f50-116">要在 Commerce Headquarters 中配置客户地址的相应销售税，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b3f50-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b3f50-117">转到 **应付帐款 \> 客户 \> 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="b3f50-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="b3f50-118">选择要为其配置销售税的客户。</span><span class="sxs-lookup"><span data-stu-id="b3f50-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="b3f50-119">在 **地址** 快速选项卡上，选择要为其配置销售税的地址，再选择 **更多选项**，然后选择 **高级**。</span><span class="sxs-lookup"><span data-stu-id="b3f50-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="b3f50-120">在 **常规** 快速选项卡上，选择 **税组**。</span><span class="sxs-lookup"><span data-stu-id="b3f50-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="b3f50-121">在 **销售税** 字段中，输入合适的值。</span><span class="sxs-lookup"><span data-stu-id="b3f50-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="b3f50-122">对于涉及客户地址上的销售税的装运，该行的收货地址确定该行的税组。</span><span class="sxs-lookup"><span data-stu-id="b3f50-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="b3f50-123">如果客户要送货到具有已配置税组的现有地址，则将使用现有税组。</span><span class="sxs-lookup"><span data-stu-id="b3f50-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="b3f50-124">默认情况下，地址在创建时没有税组。</span><span class="sxs-lookup"><span data-stu-id="b3f50-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="b3f50-125">在 Commerce Headquarters 中配置一般销售税组</span><span class="sxs-lookup"><span data-stu-id="b3f50-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="b3f50-126">要在 Commerce Headquarters 中配置一般销售税组，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b3f50-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b3f50-127">转到 **税 \> 间接税 \> 销售税 \> 销售税组**。</span><span class="sxs-lookup"><span data-stu-id="b3f50-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="b3f50-128">在左侧导航栏中，选择要配置的税组。</span><span class="sxs-lookup"><span data-stu-id="b3f50-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="b3f50-129">在 **基于零售目的地的税** 快速选项卡上，为销售税组配置税。</span><span class="sxs-lookup"><span data-stu-id="b3f50-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="b3f50-130">对于涉及客户地址上的销售税的装运，该行的交货地址以及为税组配置的基于目的地的税将确定税组。</span><span class="sxs-lookup"><span data-stu-id="b3f50-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="b3f50-131">有关详细信息，请参阅[设置基于目的地的在线商店税金](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)。</span><span class="sxs-lookup"><span data-stu-id="b3f50-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3f50-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="b3f50-132">Additional resources</span></span>

[<span data-ttu-id="b3f50-133">配置在线订单的销售税</span><span class="sxs-lookup"><span data-stu-id="b3f50-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
