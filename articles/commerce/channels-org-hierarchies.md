---
title: 设置组织层次结构
description: 此主题描述如何在 Microsoft Dynamics 365 Commerce 中设置组织层次结构。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 29d4b686cbb66715196fca06e4642fbb8a337ace
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113843"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="76be0-103">设置组织层次结构</span><span class="sxs-lookup"><span data-stu-id="76be0-103">Set up organization hierarchies</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="76be0-104">此主题描述如何在 Microsoft Dynamics 365 Commerce 中设置组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="76be0-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="76be0-105">概览</span><span class="sxs-lookup"><span data-stu-id="76be0-105">Overview</span></span>

<span data-ttu-id="76be0-106">在创建渠道之前，您需要确保已设置组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="76be0-106">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="76be0-107">可以使用组织层次结构从自各种视角查看和申报业务。</span><span class="sxs-lookup"><span data-stu-id="76be0-107">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="76be0-108">例如，您可以针对纳税、法律或法定申报设置一种层次结构。</span><span class="sxs-lookup"><span data-stu-id="76be0-108">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="76be0-109">然后，您可以设置另一层次结构，以报告不是法律要求但用于内部报表的财务信息。</span><span class="sxs-lookup"><span data-stu-id="76be0-109">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="76be0-110">在创建某一组织层次结构之前，必须先创建组织。</span><span class="sxs-lookup"><span data-stu-id="76be0-110">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="76be0-111">有关详细信息，请参阅[创建法人](channels-legal-entities.md)或[创建运营单位](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="76be0-111">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="76be0-112">有关详细信息，请参见以下主题。</span><span class="sxs-lookup"><span data-stu-id="76be0-112">For more information, see the following topics.</span></span>
- [<span data-ttu-id="76be0-113">组织和组织层次结构概览</span><span class="sxs-lookup"><span data-stu-id="76be0-113">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="76be0-114">规划组织层次结构</span><span class="sxs-lookup"><span data-stu-id="76be0-114">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="76be0-115">创建组织层次结构</span><span class="sxs-lookup"><span data-stu-id="76be0-115">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="76be0-116">创建组织层次结构</span><span class="sxs-lookup"><span data-stu-id="76be0-116">Create an organizational hierarchy</span></span>

<span data-ttu-id="76be0-117">若要创建组织层次结构，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="76be0-117">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="76be0-118">在导航窗格中，转到**模块 \> Retail and Commerce \> 渠道设置 \> 组织层次结构**。</span><span class="sxs-lookup"><span data-stu-id="76be0-118">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="76be0-119">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="76be0-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="76be0-120">在**名称**字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="76be0-120">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="76be0-121">在**用途**部分中，选择**分配用途**。</span><span class="sxs-lookup"><span data-stu-id="76be0-121">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="76be0-122">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="76be0-122">In the list, find and select the desired record.</span></span> <span data-ttu-id="76be0-123">选择分配给组织层次结构的用途。</span><span class="sxs-lookup"><span data-stu-id="76be0-123">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="76be0-124">在**已分配层次结构**部分中，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="76be0-124">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="76be0-125">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="76be0-125">In the list, mark the selected row.</span></span> <span data-ttu-id="76be0-126">查找您刚才创建的层次结构。</span><span class="sxs-lookup"><span data-stu-id="76be0-126">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="76be0-127">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="76be0-127">Select **OK**.</span></span>

<span data-ttu-id="76be0-128">下图显示了为商店的虚拟“Adventure Works”组创建的组织层次结构示例。</span><span class="sxs-lookup"><span data-stu-id="76be0-128">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![组织层次结构示例](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="76be0-130">将组织添加到层次结构</span><span class="sxs-lookup"><span data-stu-id="76be0-130">Add organizations to a hierarchy</span></span>

<span data-ttu-id="76be0-131">若将组织添加到层次结构，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="76be0-131">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="76be0-132">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="76be0-132">In the list, find and select the desired record.</span></span> <span data-ttu-id="76be0-133">选择层次结构。</span><span class="sxs-lookup"><span data-stu-id="76be0-133">Select your hierarchy.</span></span>
1. <span data-ttu-id="76be0-134">在操作窗格上，选择**查看**。</span><span class="sxs-lookup"><span data-stu-id="76be0-134">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="76be0-135">根据需要添加组织。</span><span class="sxs-lookup"><span data-stu-id="76be0-135">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="76be0-136">要添加组织，请选择**编辑**，然后选择**插入**。</span><span class="sxs-lookup"><span data-stu-id="76be0-136">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="76be0-137">在进行更改后，您可以保存草稿和发布更改。</span><span class="sxs-lookup"><span data-stu-id="76be0-137">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="76be0-138">下图显示了在层次结构根位置添加的法人，并为“购物中心”、“出口”、“在线”和“呼叫中心”渠道添加了四个成本中心。</span><span class="sxs-lookup"><span data-stu-id="76be0-138">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="76be0-139">然后可以将各种零售、呼叫中心和在线渠道添加到每个成本中心。</span><span class="sxs-lookup"><span data-stu-id="76be0-139">Various retail, call center and online channels can then be added to each.</span></span>

![层次结构设计器示例](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="76be0-141">其他资源</span><span class="sxs-lookup"><span data-stu-id="76be0-141">Additional resources</span></span>

[<span data-ttu-id="76be0-142">组织和组织层次结构概览</span><span class="sxs-lookup"><span data-stu-id="76be0-142">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="76be0-143">规划组织层次结构</span><span class="sxs-lookup"><span data-stu-id="76be0-143">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="76be0-144">创建法人</span><span class="sxs-lookup"><span data-stu-id="76be0-144">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="76be0-145">创建运营单位</span><span class="sxs-lookup"><span data-stu-id="76be0-145">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="76be0-146">渠道概览</span><span class="sxs-lookup"><span data-stu-id="76be0-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="76be0-147">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="76be0-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)
