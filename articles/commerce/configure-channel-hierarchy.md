---
title: 配置渠道以使用渠道导航层次结构
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置渠道以使用渠道导航层次结构。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 94d38c5c3a091263b310f346f839e1a67d6c0609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796116"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="b9586-103">配置渠道以使用渠道导航层次结构</span><span class="sxs-lookup"><span data-stu-id="b9586-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b9586-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置渠道以使用渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="b9586-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b9586-105">概览</span><span class="sxs-lookup"><span data-stu-id="b9586-105">Overview</span></span>

<span data-ttu-id="b9586-106">渠道导航层次结构按类别组织产品，以便可以在电子商务站点或销售点 (POS) 上浏览产品。</span><span class="sxs-lookup"><span data-stu-id="b9586-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="b9586-107">对于渠道导航层次结构，必须配置零售和在线渠道。</span><span class="sxs-lookup"><span data-stu-id="b9586-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="b9586-108">配置渠道</span><span class="sxs-lookup"><span data-stu-id="b9586-108">Configure the channel</span></span>

<span data-ttu-id="b9586-109">要配置渠道以使用渠道导航层次结构，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b9586-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b9586-110">在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 渠道类别和产品属性**。</span><span class="sxs-lookup"><span data-stu-id="b9586-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="b9586-111">选择要配置的渠道。</span><span class="sxs-lookup"><span data-stu-id="b9586-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="b9586-112">在操作窗格上，选择 **设置属性元数据**。</span><span class="sxs-lookup"><span data-stu-id="b9586-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="b9586-113">在 **类别层次结构** 下拉列表中，选择合适的渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="b9586-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="b9586-114">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b9586-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="b9586-115">在 **属性组** 下面，添加将成为所有节点的全局属性的所有属性组。</span><span class="sxs-lookup"><span data-stu-id="b9586-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="b9586-116">下图显示了如何配置渠道以使用渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="b9586-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![渠道配置示例](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="b9586-118">设置属性元数据</span><span class="sxs-lookup"><span data-stu-id="b9586-118">Set attribute metadata</span></span>

<span data-ttu-id="b9586-119">设置属性元数据将允许在每个节点上配置属性。</span><span class="sxs-lookup"><span data-stu-id="b9586-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="b9586-120">要设置属性元数据，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b9586-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="b9586-121">在操作窗格上，选择 **设置属性元数据**。</span><span class="sxs-lookup"><span data-stu-id="b9586-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="b9586-122">对于每个节点，请选择 **渠道产品属性**。</span><span class="sxs-lookup"><span data-stu-id="b9586-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="b9586-123">将 **在渠道上显示属性** 设置为 **是**，将 **可细化** 设置为 **是**，以在该渠道上启用优化器。</span><span class="sxs-lookup"><span data-stu-id="b9586-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="b9586-124">根据需要配置每个节点后，在 **操作窗格** 上，选择 **保存** 按钮进行保存。</span><span class="sxs-lookup"><span data-stu-id="b9586-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="b9586-125">选择右上角中的 **X** 以将此屏幕退回到 **渠道类别和产品属性** 页。</span><span class="sxs-lookup"><span data-stu-id="b9586-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="b9586-126">下图显示了在渠道类别节点上配置的一组渠道产品属性的示例。</span><span class="sxs-lookup"><span data-stu-id="b9586-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![渠道类别节点上的渠道属性](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="b9586-128">发布渠道</span><span class="sxs-lookup"><span data-stu-id="b9586-128">Publish changes</span></span>

<span data-ttu-id="b9586-129">若要让更改生效，则需要发布这些更改。</span><span class="sxs-lookup"><span data-stu-id="b9586-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="b9586-130">若要发布更改，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b9586-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="b9586-131">在操作窗格上，选择 **发布渠道更新**。</span><span class="sxs-lookup"><span data-stu-id="b9586-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="b9586-132">在 **发布渠道更新** 窗格中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9586-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="b9586-133">下图显示了如何发布渠道更新。</span><span class="sxs-lookup"><span data-stu-id="b9586-133">The following image shows how to publish channel updates.</span></span>

![发布渠道更新](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="b9586-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="b9586-135">Additional resources</span></span>

[<span data-ttu-id="b9586-136">创建渠道导航层次结构</span><span class="sxs-lookup"><span data-stu-id="b9586-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]