---
title: 将渠道添加到组织层次结构
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中将渠道添加到组织层次结构。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 297bd34f9bde23d5cc7de266b8e8f49b1a752662
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993680"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="1370f-103">将渠道添加到组织层次结构</span><span class="sxs-lookup"><span data-stu-id="1370f-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1370f-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中将渠道添加到组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="1370f-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1370f-105">概览</span><span class="sxs-lookup"><span data-stu-id="1370f-105">Overview</span></span>

<span data-ttu-id="1370f-106">渠道需要与一个或多个组织层次结构相关联。</span><span class="sxs-lookup"><span data-stu-id="1370f-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="1370f-107">在创建渠道之前，您需要确认已设置组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="1370f-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="1370f-108">参阅[组织层次结构](channels-org-hierarchies.md)，以了解有关如何创建组织层次结构的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="1370f-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="1370f-109">选择层次结构</span><span class="sxs-lookup"><span data-stu-id="1370f-109">Select a hierarchy</span></span>

<span data-ttu-id="1370f-110">若要选择层次结构，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1370f-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="1370f-111">在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 组织层次结构**。</span><span class="sxs-lookup"><span data-stu-id="1370f-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="1370f-112">从列表中，选择要将渠道添加到的组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="1370f-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="1370f-113">在操作窗格上，选择 **查看** 以查看层次结构详细信息。</span><span class="sxs-lookup"><span data-stu-id="1370f-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="1370f-114">下图显示了所选层次结构的组织层次结构详细信息。</span><span class="sxs-lookup"><span data-stu-id="1370f-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![所选层次结构的组织层次结构详细信息](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="1370f-116">将渠道添加到层次结构节点</span><span class="sxs-lookup"><span data-stu-id="1370f-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="1370f-117">若要将渠道添加到层次结构节点，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1370f-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="1370f-118">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="1370f-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="1370f-119">选择要将渠道添加到的层次结构节点，然后从 **插入** 下拉列表中选择 **零售渠道**。</span><span class="sxs-lookup"><span data-stu-id="1370f-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="1370f-120">选择要添加的渠道，然后选择 **确定** 按钮。</span><span class="sxs-lookup"><span data-stu-id="1370f-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="1370f-121">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1370f-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="1370f-122">在操作窗格上，选择 **发布** 并提供一个过去的 **生效日期** 以立即执行此操作。</span><span class="sxs-lookup"><span data-stu-id="1370f-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="1370f-123">下图显示了如何选择要添加到层次结构节点的渠道。</span><span class="sxs-lookup"><span data-stu-id="1370f-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![选择要添加到层次结构节点的渠道](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="1370f-125">下图显示了添加了各种渠道的层次结构。</span><span class="sxs-lookup"><span data-stu-id="1370f-125">The following image shows a hierarchy with various channels added.</span></span>

![添加了各种渠道的层次结构](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="1370f-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="1370f-127">Additional resources</span></span>

[<span data-ttu-id="1370f-128">渠道概览</span><span class="sxs-lookup"><span data-stu-id="1370f-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="1370f-129">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="1370f-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="1370f-130">组织和组织层次结构概览</span><span class="sxs-lookup"><span data-stu-id="1370f-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1370f-131">规划组织层次结构</span><span class="sxs-lookup"><span data-stu-id="1370f-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1370f-132">组织层次结构</span><span class="sxs-lookup"><span data-stu-id="1370f-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="1370f-133">设置零售渠道</span><span class="sxs-lookup"><span data-stu-id="1370f-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="1370f-134">设置在线渠道</span><span class="sxs-lookup"><span data-stu-id="1370f-134">Set up an online channel</span></span>](channel-setup-online.md)
