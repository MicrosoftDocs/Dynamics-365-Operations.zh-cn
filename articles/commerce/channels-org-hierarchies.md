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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 490d466c10cfe0640f8fbcf8fe2298536e499d9b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477988"
---
# <a name="set-up-organization-hierarchies"></a><span data-ttu-id="004f1-103">设置组织层次结构</span><span class="sxs-lookup"><span data-stu-id="004f1-103">Set up organization hierarchies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="004f1-104">此主题描述如何在 Microsoft Dynamics 365 Commerce 中设置组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="004f1-104">This topic describes how to set up organization hierarchies in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="004f1-105">在创建渠道之前，您需要确保已设置组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="004f1-105">Before creating channels, you'll want to ensure you have set up your organization hierarchies.</span></span>

<span data-ttu-id="004f1-106">可以使用组织层次结构从自各种视角查看和申报业务。</span><span class="sxs-lookup"><span data-stu-id="004f1-106">You can use organization hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="004f1-107">例如，您可以针对纳税、法律或法定申报设置一种层次结构。</span><span class="sxs-lookup"><span data-stu-id="004f1-107">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="004f1-108">然后，您可以设置另一层次结构，以报告不是法律要求但用于内部报表的财务信息。</span><span class="sxs-lookup"><span data-stu-id="004f1-108">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span>

<span data-ttu-id="004f1-109">在创建某一组织层次结构之前，必须先创建组织。</span><span class="sxs-lookup"><span data-stu-id="004f1-109">Before you create an organization hierarchy, you must create organizations.</span></span> <span data-ttu-id="004f1-110">有关详细信息，请参阅[创建法人](channels-legal-entities.md)或[创建运营单位](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="004f1-110">For more information, see [Create legal entities](channels-legal-entities.md) or [Create operating units](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).</span></span>


<span data-ttu-id="004f1-111">有关详细信息，请参见以下主题。</span><span class="sxs-lookup"><span data-stu-id="004f1-111">For more information, see the following topics.</span></span>
- [<span data-ttu-id="004f1-112">组织和组织层次结构概览</span><span class="sxs-lookup"><span data-stu-id="004f1-112">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="004f1-113">规划组织层次结构</span><span class="sxs-lookup"><span data-stu-id="004f1-113">Plan your organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="004f1-114">创建组织层次结构</span><span class="sxs-lookup"><span data-stu-id="004f1-114">Create an organization hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a><span data-ttu-id="004f1-115">创建组织层次结构</span><span class="sxs-lookup"><span data-stu-id="004f1-115">Create an organizational hierarchy</span></span>

<span data-ttu-id="004f1-116">若要创建组织层次结构，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="004f1-116">To create an organizational hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="004f1-117">在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 组织层次结构**。</span><span class="sxs-lookup"><span data-stu-id="004f1-117">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="004f1-118">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="004f1-118">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="004f1-119">在 **名称** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="004f1-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="004f1-120">在 **用途** 部分中，选择 **分配用途**。</span><span class="sxs-lookup"><span data-stu-id="004f1-120">In the **Purpose** section, select **Assign purpose**.</span></span>
1. <span data-ttu-id="004f1-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="004f1-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="004f1-122">选择分配给组织层次结构的用途。</span><span class="sxs-lookup"><span data-stu-id="004f1-122">Select a purpose to assign to your organization hierarchy.</span></span>
1. <span data-ttu-id="004f1-123">在 **已分配层次结构** 部分中，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="004f1-123">In the **Assigned hierarchies** section, select **Add**.</span></span>
1. <span data-ttu-id="004f1-124">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="004f1-124">In the list, mark the selected row.</span></span> <span data-ttu-id="004f1-125">查找您刚才创建的层次结构。</span><span class="sxs-lookup"><span data-stu-id="004f1-125">Find the hierarchy you just created.</span></span>
1. <span data-ttu-id="004f1-126">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="004f1-126">Select **OK**.</span></span>

<span data-ttu-id="004f1-127">下图显示了为商店的虚拟“Adventure Works”组创建的组织层次结构示例。</span><span class="sxs-lookup"><span data-stu-id="004f1-127">The following image shows an example organizational hierarchy created for a fictitious "Adventure Works" set of stores.</span></span>

![组织层次结构示例](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a><span data-ttu-id="004f1-129">将组织添加到层次结构</span><span class="sxs-lookup"><span data-stu-id="004f1-129">Add organizations to a hierarchy</span></span>

<span data-ttu-id="004f1-130">若将组织添加到层次结构，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="004f1-130">To add organizations to a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="004f1-131">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="004f1-131">In the list, find and select the desired record.</span></span> <span data-ttu-id="004f1-132">选择层次结构。</span><span class="sxs-lookup"><span data-stu-id="004f1-132">Select your hierarchy.</span></span>
1. <span data-ttu-id="004f1-133">在操作窗格上，选择 **查看**。</span><span class="sxs-lookup"><span data-stu-id="004f1-133">On the action pane, select **View**.</span></span>
1. <span data-ttu-id="004f1-134">根据需要添加组织。</span><span class="sxs-lookup"><span data-stu-id="004f1-134">Add organizations, as necessary.</span></span>
1. <span data-ttu-id="004f1-135">要添加组织，请选择 **编辑**，然后选择 **插入**。</span><span class="sxs-lookup"><span data-stu-id="004f1-135">To add an organization, select **Edit** and then select **Insert**.</span></span> <span data-ttu-id="004f1-136">在进行更改后，您可以保存草稿和发布更改。</span><span class="sxs-lookup"><span data-stu-id="004f1-136">When you are done making changes you can save a draft and publish the changes.</span></span>

<span data-ttu-id="004f1-137">下图显示了在层次结构根位置添加的法人，并为“购物中心”、“出口”、“在线”和“呼叫中心”渠道添加了四个成本中心。</span><span class="sxs-lookup"><span data-stu-id="004f1-137">The following image shows a legal entity added at the hierarchy root with four cost centers added for "Mall", "Outlet", "Online" and "Call Center" channels.</span></span> <span data-ttu-id="004f1-138">然后可以将各种零售、呼叫中心和在线渠道添加到每个成本中心。</span><span class="sxs-lookup"><span data-stu-id="004f1-138">Various retail, call center and online channels can then be added to each.</span></span>

![层次结构设计器示例](media/hierarchy-designer.png)

## <a name="additional-resources"></a><span data-ttu-id="004f1-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="004f1-140">Additional resources</span></span>

[<span data-ttu-id="004f1-141">组织和组织层次结构概览</span><span class="sxs-lookup"><span data-stu-id="004f1-141">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="004f1-142">规划组织层次结构</span><span class="sxs-lookup"><span data-stu-id="004f1-142">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="004f1-143">创建法人</span><span class="sxs-lookup"><span data-stu-id="004f1-143">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="004f1-144">创建运营单位</span><span class="sxs-lookup"><span data-stu-id="004f1-144">Create operating units</span></span>](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="004f1-145">渠道概览</span><span class="sxs-lookup"><span data-stu-id="004f1-145">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="004f1-146">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="004f1-146">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
