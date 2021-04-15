---
title: 配置 B2B 电子商务站点的客户帐户付款方式
description: 本主题介绍如何为企业到企业 (B2B) 电子商务站点配置客户帐户付款方式。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799797"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a><span data-ttu-id="ec607-103">配置 B2B 电子商务站点的客户帐户付款方式</span><span class="sxs-lookup"><span data-stu-id="ec607-103">Configure the customer account payment method for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec607-104">本主题介绍如何为企业到企业 (B2B) 电子商务站点配置客户帐户付款方式。</span><span class="sxs-lookup"><span data-stu-id="ec607-104">This topic describes how to configure the customer account payment method for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="ec607-105">零售商可以接受各种类型的付款来交换其在电子商务渠道中销售的产品和服务。</span><span class="sxs-lookup"><span data-stu-id="ec607-105">Retailers can accept various types of payment in exchange for the products and services that they sell in an e-commerce channel.</span></span> <span data-ttu-id="ec607-106">设置系统时，必须在 Microsoft Dynamics 365 Commerce 中配置零售商接受的每种付款类型。</span><span class="sxs-lookup"><span data-stu-id="ec607-106">Each payment type that a retailer accepts must be configured in Microsoft Dynamics 365 Commerce when the system is set up.</span></span> <span data-ttu-id="ec607-107">B2B 电子商务站点必须支持客户帐户（或“分期付款”）付款方式。</span><span class="sxs-lookup"><span data-stu-id="ec607-107">The customer account (or "on account") payment method must be supported on B2B e-commerce sites.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="ec607-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="ec607-108">Prerequisites</span></span>

1. <span data-ttu-id="ec607-109">在 Commerce headquarters 中添加客户帐户付款方式。</span><span class="sxs-lookup"><span data-stu-id="ec607-109">Add the customer account payment method in Commerce headquarters.</span></span>
2. <span data-ttu-id="ec607-110">将客户帐户付款方式与电子商务渠道关联。</span><span class="sxs-lookup"><span data-stu-id="ec607-110">Associate the customer account payment method with the e-commerce channel.</span></span>
3. <span data-ttu-id="ec607-111">确保在 Commerce headquarters 中，在 **Retail 和 Commerce \> 客户 \> 所有客户 \> 付款默认值** 中为客户启用了 **允许分期付款**。</span><span class="sxs-lookup"><span data-stu-id="ec607-111">Make sure that **Allow on account** is enabled for the customer at **Retail and Commerce \> Customers \> All customers \> Payment defaults** in Commerce headquarters.</span></span> <span data-ttu-id="ec607-112">同时确保在 Commerce headquarters 中，在 **Retail 和 Commerce \> 客户 \> 所有客户 \> 信用和收款** 中为客户正确设置了 **信用额度** 参数。</span><span class="sxs-lookup"><span data-stu-id="ec607-112">Also make sure that **Credit limit** parameters are set appropriately for the customer at **Retail and Commerce \> Customers \> All customers \> Credit and Collections** in Commerce headquarters.</span></span> 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a><span data-ttu-id="ec607-113">在 Commerce 站点构建器中启用客户帐户付款方式</span><span class="sxs-lookup"><span data-stu-id="ec607-113">Enable the customer account payment method in Commerce site builder</span></span> 

<span data-ttu-id="ec607-114">要在 Commerce 站点构建器中启用客户帐户付款方式，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ec607-114">To enable the customer account payment method in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ec607-115">转到 **站点设置 \> 扩展**。</span><span class="sxs-lookup"><span data-stu-id="ec607-115">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="ec607-116">将 **启用客户帐户付款** 属性设置为 **为 B2B 客户启用**。</span><span class="sxs-lookup"><span data-stu-id="ec607-116">Set the **Enable customer account payments** property to **Enabled for B2B customers**.</span></span> 
1. <span data-ttu-id="ec607-117">选择 **保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="ec607-117">Select **Save and Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="ec607-118">新站点设置仅在更新 app.settings.json 文件后才会生效。</span><span class="sxs-lookup"><span data-stu-id="ec607-118">The new site settings take effect only after the app.settings.json file is updated.</span></span> <span data-ttu-id="ec607-119">有关详细信息，请参阅 [SDK 和模块库更新](../e-commerce-extensibility/sdk-updates.md)。</span><span class="sxs-lookup"><span data-stu-id="ec607-119">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md).</span></span>

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a><span data-ttu-id="ec607-120">在 B2B 电子商务站点的结帐页上启用客户帐户付款方式</span><span class="sxs-lookup"><span data-stu-id="ec607-120">Enable the customer account payment method on the checkout page for the B2B e-commerce site</span></span>

<span data-ttu-id="ec607-121">要在 B2B 电子商务站点的结帐页上启用客户帐户付款方式，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ec607-121">To enable the customer account payment method on the checkout page for the B2B e-commerce site, follow these steps.</span></span>

1. <span data-ttu-id="ec607-122">在 Commerce 站点构建器中，找到并编辑包含 B2B 电子商务站点的结帐模块的结帐页面或片段。</span><span class="sxs-lookup"><span data-stu-id="ec607-122">In Commerce site builder, find and edit the checkout page or fragment that contains the checkout module for the B2B e-commerce site.</span></span>
1. <span data-ttu-id="ec607-123">在 **结帐部分容器** 插槽中，选择 **添加模块**，然后添加 **客户帐户付款** 模块。</span><span class="sxs-lookup"><span data-stu-id="ec607-123">In the **Checkout section container** slot, select **Add Module**, and then add a **Customer account payment** module.</span></span>
1. <span data-ttu-id="ec607-124">选择省略号 (**...**)，然后根据需要选择 **上移** 或 **下移**，来放置 **客户帐户付款** 模块。</span><span class="sxs-lookup"><span data-stu-id="ec607-124">Position the **Customer account payment** module by selecting the ellipsis (**...**), and then selecting **Move Up** or **Move Down** as required.</span></span>
1. <span data-ttu-id="ec607-125">选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="ec607-125">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a><span data-ttu-id="ec607-126">确认已启用并发布客户帐户付款方式</span><span class="sxs-lookup"><span data-stu-id="ec607-126">Confirm that the customer account payment method has been enabled and published</span></span>

<span data-ttu-id="ec607-127">要确认已启用客户帐户付款方式，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ec607-127">To confirm that the customer account payment method has been enabled, follow these steps.</span></span>

1. <span data-ttu-id="ec607-128">登录电子商务站点。</span><span class="sxs-lookup"><span data-stu-id="ec607-128">Sign in to the e-commerce site.</span></span>
1. <span data-ttu-id="ec607-129">向购物车添加产品。</span><span class="sxs-lookup"><span data-stu-id="ec607-129">Add a product to the cart.</span></span>
1. <span data-ttu-id="ec607-130">转到结帐页。</span><span class="sxs-lookup"><span data-stu-id="ec607-130">Go to the checkout page.</span></span> <span data-ttu-id="ec607-131">您应该会看到新的 **客户帐户** 付款方式。</span><span class="sxs-lookup"><span data-stu-id="ec607-131">You should see the new **Customer Account** payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec607-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="ec607-132">Additional resources</span></span>

[<span data-ttu-id="ec607-133">建立 B2B 电子商务站点</span><span class="sxs-lookup"><span data-stu-id="ec607-133">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="ec607-134">为 B2B 组织创建组织建模层次结构</span><span class="sxs-lookup"><span data-stu-id="ec607-134">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="ec607-135">在 B2B 电子商务站点上管理业务合作伙伴用户</span><span class="sxs-lookup"><span data-stu-id="ec607-135">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="ec607-136">设置 B2B 电子商务站点的产品数量限制</span><span class="sxs-lookup"><span data-stu-id="ec607-136">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

[<span data-ttu-id="ec607-137">SDK 和模块库更新</span><span class="sxs-lookup"><span data-stu-id="ec607-137">SDK and Module library updates</span></span>](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]