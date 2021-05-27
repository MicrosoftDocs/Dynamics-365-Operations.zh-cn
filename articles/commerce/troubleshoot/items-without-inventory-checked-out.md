---
title: 没有库存的商品可以结帐
description: 本主题提供了故障排除指南，可以在客户将缺货商品添加到购物车并继续进行结帐时提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018450"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="6107e-103">没有库存的商品可以结帐</span><span class="sxs-lookup"><span data-stu-id="6107e-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6107e-104">本主题提供了故障排除指南，可以在客户将缺货商品添加到购物车并继续进行结帐时提供帮助。</span><span class="sxs-lookup"><span data-stu-id="6107e-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="6107e-105">说明</span><span class="sxs-lookup"><span data-stu-id="6107e-105">Description</span></span>

<span data-ttu-id="6107e-106">即使商店中没有现有库存，用户也可以将商品添加到购物车中，然后进入结帐页面。</span><span class="sxs-lookup"><span data-stu-id="6107e-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="6107e-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="6107e-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="6107e-108">在 Commerce 站点构建器中启用“显示缺货错误”属性</span><span class="sxs-lookup"><span data-stu-id="6107e-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="6107e-109">要在 Commerce 站点构建器中启用 **显示缺货错误** 属性，请执行这些步骤。</span><span class="sxs-lookup"><span data-stu-id="6107e-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="6107e-110">选择您正在处理的站点。</span><span class="sxs-lookup"><span data-stu-id="6107e-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="6107e-111">在左侧导航中，选择 **页面**。</span><span class="sxs-lookup"><span data-stu-id="6107e-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="6107e-112">选择 **购物车页面** 打开它。</span><span class="sxs-lookup"><span data-stu-id="6107e-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="6107e-113">选择 **购物车 1** 插槽，选择 **编辑**，然后在属性窗格中，选择 **显示缺货错误** 复选框。</span><span class="sxs-lookup"><span data-stu-id="6107e-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="6107e-114">保存并发布页面。</span><span class="sxs-lookup"><span data-stu-id="6107e-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6107e-115">其他资源</span><span class="sxs-lookup"><span data-stu-id="6107e-115">Additional resources</span></span>

[<span data-ttu-id="6107e-116">应用库存设置</span><span class="sxs-lookup"><span data-stu-id="6107e-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="6107e-117">计算零售渠道的库存现有量</span><span class="sxs-lookup"><span data-stu-id="6107e-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="6107e-118">配置库存缓冲区和库存级别</span><span class="sxs-lookup"><span data-stu-id="6107e-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
