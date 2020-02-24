---
title: 创建默认客户
description: 本主题描述如何创建在 Microsoft Dynamics 365 Commerce 中创建渠道时要使用的默认客户。
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
ms.openlocfilehash: 9e1087821b357c578993cdd5742399c5ec0ecc95
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001798"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="db272-103">创建默认客户</span><span class="sxs-lookup"><span data-stu-id="db272-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="db272-104">本主题描述如何创建在 Microsoft Dynamics 365 Commerce 中创建渠道时要使用的默认客户。</span><span class="sxs-lookup"><span data-stu-id="db272-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="db272-105">概览</span><span class="sxs-lookup"><span data-stu-id="db272-105">Overview</span></span>

<span data-ttu-id="db272-106">创建零售或在线渠道时，您将需要提供一个默认客户。</span><span class="sxs-lookup"><span data-stu-id="db272-106">When creating a retail or online channel, you will need to provide a default customer.</span></span> <span data-ttu-id="db272-107">在首先创建客户组和客户地址簿后，可以轻松创建默认客户。</span><span class="sxs-lookup"><span data-stu-id="db272-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="db272-108">创建客户组</span><span class="sxs-lookup"><span data-stu-id="db272-108">Create a customer group</span></span>

<span data-ttu-id="db272-109">如果尚不存在客户组，则可以创建一个。</span><span class="sxs-lookup"><span data-stu-id="db272-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="db272-110">示例可能是代表不同客户组（例如批发、零售、互联网、员工等）的组。</span><span class="sxs-lookup"><span data-stu-id="db272-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="db272-111">要创建客户组，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="db272-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="db272-112">在导航窗格中，转到**模块 \> Retail and Commerce \> 客户 \> 客户组**。</span><span class="sxs-lookup"><span data-stu-id="db272-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="db272-113">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="db272-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="db272-114">在**客户组**框中，输入客户组 ID。</span><span class="sxs-lookup"><span data-stu-id="db272-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="db272-115">在**描述**框中，输入适当的描述。</span><span class="sxs-lookup"><span data-stu-id="db272-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="db272-116">在**付款期限**框中，输入适当的值。</span><span class="sxs-lookup"><span data-stu-id="db272-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="db272-117">在**发票到期日期与付款日期之间的时间**框中，输入适当的值。</span><span class="sxs-lookup"><span data-stu-id="db272-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="db272-118">在**默认税组**框，输入税组（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="db272-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="db272-119">如果适用，请选中**价格包括销售税**复选框。</span><span class="sxs-lookup"><span data-stu-id="db272-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="db272-120">在**默认勾销原因**框，输入适当的值（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="db272-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="db272-121">下图显示了几个已配置的客户组。</span><span class="sxs-lookup"><span data-stu-id="db272-121">The following image shows several configured customer groups.</span></span>

![客户组](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="db272-123">新建客户通讯簿</span><span class="sxs-lookup"><span data-stu-id="db272-123">Create a customer address book</span></span>

<span data-ttu-id="db272-124">客户需要与通讯簿相关联。</span><span class="sxs-lookup"><span data-stu-id="db272-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="db272-125">如果尚未创建，则需要创建一个。</span><span class="sxs-lookup"><span data-stu-id="db272-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="db272-126">要创建客户通讯簿，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="db272-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="db272-127">在导航窗格中，转到**模块 \> Retail and Commerce \> 渠道设置 \> 通讯簿**。</span><span class="sxs-lookup"><span data-stu-id="db272-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="db272-128">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="db272-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="db272-129">在**名称**框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="db272-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="db272-130">在**描述**框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="db272-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="db272-131">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="db272-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="db272-132">下图显示了一个通讯簿示例。</span><span class="sxs-lookup"><span data-stu-id="db272-132">The following image shows an example address book.</span></span>

![通讯簿](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="db272-134">创建默认客户</span><span class="sxs-lookup"><span data-stu-id="db272-134">Create a default customer</span></span>

<span data-ttu-id="db272-135">要创建默认客户，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="db272-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="db272-136">在导航窗格中，转到**模块 \> Retail and Commerce \> 客户 \> 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="db272-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="db272-137">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="db272-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="db272-138">在**类型**下拉列表中，选择“人员”。</span><span class="sxs-lookup"><span data-stu-id="db272-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="db272-139">在**客户账户**下拉列表中，选择或输入帐号（例如，“100001”）。</span><span class="sxs-lookup"><span data-stu-id="db272-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="db272-140">在**名字**下拉列表中，选择或输入名称（例如，“默认”）。</span><span class="sxs-lookup"><span data-stu-id="db272-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="db272-141">在**中间名**下拉列表中，选择或输入名称（例如，“零售”）。</span><span class="sxs-lookup"><span data-stu-id="db272-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="db272-142">在**姓氏**下拉列表中，选择或输入名称（例如，“客户”）。</span><span class="sxs-lookup"><span data-stu-id="db272-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="db272-143">在**货币**下拉列表中，选择或输入货币（例如，“美元”）。</span><span class="sxs-lookup"><span data-stu-id="db272-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="db272-144">在**货币**下拉列表中，选择先前创建的客户组。</span><span class="sxs-lookup"><span data-stu-id="db272-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="db272-145">在**地址簿**下拉列表中，选择一个现有的客户通讯簿。</span><span class="sxs-lookup"><span data-stu-id="db272-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="db272-146">选择**保存**以保存并返回到新客户的客户详细信息屏幕。</span><span class="sxs-lookup"><span data-stu-id="db272-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="db272-147">不必为默认客户添加地址。</span><span class="sxs-lookup"><span data-stu-id="db272-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="db272-148">下图显示客户创建的示例。</span><span class="sxs-lookup"><span data-stu-id="db272-148">The following image shows an example of customer creation.</span></span>

![默认客户创建](media/default-customer-creation.png)

<span data-ttu-id="db272-150">下图显示了默认的客户配置。</span><span class="sxs-lookup"><span data-stu-id="db272-150">The following image shows a default customer configuration.</span></span>

![客户配置示例](media/default-customer-configuration1.png)

<span data-ttu-id="db272-152">客户详细信息屏幕上的大多数默认值都可以保留，但是应该更改两个值。</span><span class="sxs-lookup"><span data-stu-id="db272-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="db272-153">在客户详细信息屏幕上，展开**销售订单默认值**。</span><span class="sxs-lookup"><span data-stu-id="db272-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="db272-154">在**站点**下拉列表中，选择或输入一个预配置的站点。</span><span class="sxs-lookup"><span data-stu-id="db272-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="db272-155">在**仓库**下拉列表中，选择或输入一个预配置的仓库。</span><span class="sxs-lookup"><span data-stu-id="db272-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="db272-156">下图显示客户配置示例。</span><span class="sxs-lookup"><span data-stu-id="db272-156">The following image shows an example customer configuration.</span></span>

![客户配置示例](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="db272-158">其他资源</span><span class="sxs-lookup"><span data-stu-id="db272-158">Additional resources</span></span>

[<span data-ttu-id="db272-159">渠道概览</span><span class="sxs-lookup"><span data-stu-id="db272-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="db272-160">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="db272-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
