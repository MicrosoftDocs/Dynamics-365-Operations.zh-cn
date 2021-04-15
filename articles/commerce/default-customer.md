---
title: 创建默认客户
description: 本主题描述如何创建在 Microsoft Dynamics 365 Commerce 中创建渠道时要使用的默认客户。
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
ms.openlocfilehash: ecdf4e5618d3397527bf83977857fbe3f8dbb265
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799171"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="6b046-103">创建默认客户</span><span class="sxs-lookup"><span data-stu-id="6b046-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b046-104">本主题描述如何创建在 Microsoft Dynamics 365 Commerce 中创建渠道时要使用的默认客户。</span><span class="sxs-lookup"><span data-stu-id="6b046-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6b046-105">创建渠道时，您将需要提供一个默认客户。</span><span class="sxs-lookup"><span data-stu-id="6b046-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="6b046-106">在首先创建客户组和客户地址簿后，可以轻松创建默认客户。</span><span class="sxs-lookup"><span data-stu-id="6b046-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="6b046-107">创建客户组</span><span class="sxs-lookup"><span data-stu-id="6b046-107">Create a customer group</span></span>

<span data-ttu-id="6b046-108">如果尚不存在客户组，则可以创建一个。</span><span class="sxs-lookup"><span data-stu-id="6b046-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="6b046-109">示例可能是代表不同客户组（例如批发、零售、互联网、员工等）的组。</span><span class="sxs-lookup"><span data-stu-id="6b046-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="6b046-110">要创建客户组，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6b046-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="6b046-111">在导航窗格中，转到 **模块 \> Retail and Commerce \> 客户 \> 客户组**。</span><span class="sxs-lookup"><span data-stu-id="6b046-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="6b046-112">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6b046-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6b046-113">在 **客户组** 框中，输入客户组 ID。</span><span class="sxs-lookup"><span data-stu-id="6b046-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="6b046-114">在 **描述** 框中，输入适当的描述。</span><span class="sxs-lookup"><span data-stu-id="6b046-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="6b046-115">在 **付款期限** 框中，输入适当的值。</span><span class="sxs-lookup"><span data-stu-id="6b046-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="6b046-116">在 **发票到期日期与付款日期之间的时间** 框中，输入适当的值。</span><span class="sxs-lookup"><span data-stu-id="6b046-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="6b046-117">在 **默认税组** 框，输入税组（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="6b046-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="6b046-118">如果适用，请选中 **价格包括销售税** 复选框。</span><span class="sxs-lookup"><span data-stu-id="6b046-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="6b046-119">在 **默认勾销原因** 框，输入适当的值（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="6b046-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="6b046-120">下图显示了几个已配置的客户组。</span><span class="sxs-lookup"><span data-stu-id="6b046-120">The following image shows several configured customer groups.</span></span>

![客户组](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="6b046-122">新建客户通讯簿</span><span class="sxs-lookup"><span data-stu-id="6b046-122">Create a customer address book</span></span>

<span data-ttu-id="6b046-123">客户需要与通讯簿相关联。</span><span class="sxs-lookup"><span data-stu-id="6b046-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="6b046-124">如果尚未创建，则需要创建一个。</span><span class="sxs-lookup"><span data-stu-id="6b046-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="6b046-125">要创建客户通讯簿，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6b046-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="6b046-126">在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 通讯簿**。</span><span class="sxs-lookup"><span data-stu-id="6b046-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="6b046-127">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="6b046-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6b046-128">在 **名称** 框中，输入名称。</span><span class="sxs-lookup"><span data-stu-id="6b046-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="6b046-129">在 **描述** 框中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="6b046-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="6b046-130">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6b046-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6b046-131">下图显示了一个通讯簿示例。</span><span class="sxs-lookup"><span data-stu-id="6b046-131">The following image shows an example address book.</span></span>

![通讯簿](media/address-book.png)

## <a name="create-a-default-customer&quot;></a><span data-ttu-id=&quot;6b046-133&quot;>创建默认客户</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b046-133&quot;>Create a default customer</span></span>

<span data-ttu-id=&quot;6b046-134&quot;>要创建默认客户，请执行以下步骤。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b046-134&quot;>To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id=&quot;6b046-135&quot;>在导航窗格中，转到 **模块 \> Retail and Commerce \> 客户 \> 所有客户**。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b046-135&quot;>In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id=&quot;6b046-136&quot;>在操作窗格上，选择 **新建**。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b046-136&quot;>On the action pane, select **New**.</span></span>
1. <span data-ttu-id=&quot;6b046-137&quot;>在 **类型** 下拉列表中，选择“人员”。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b046-137&quot;>In the **Type** drop-down list, select &quot;Person&quot;.</span></span>
1. <span data-ttu-id=&quot;6b046-138&quot;>在 **客户账户** 下拉列表中，选择或输入帐号（例如，“100001”）。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;6b046-138&quot;>In the **Customer account** drop-down list, select or enter an account number (for example, &quot;100001").</span></span>
1. <span data-ttu-id="6b046-139">在 **名字** 下拉列表中，选择或输入名称（例如，“默认”）。</span><span class="sxs-lookup"><span data-stu-id="6b046-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="6b046-140">在 **中间名** 下拉列表中，选择或输入名称（例如，“零售”）。</span><span class="sxs-lookup"><span data-stu-id="6b046-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="6b046-141">在 **姓氏** 下拉列表中，选择或输入名称（例如，“客户”）。</span><span class="sxs-lookup"><span data-stu-id="6b046-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="6b046-142">在 **货币** 下拉列表中，选择或输入货币（例如，“美元”）。</span><span class="sxs-lookup"><span data-stu-id="6b046-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="6b046-143">在 **货币** 下拉列表中，选择先前创建的客户组。</span><span class="sxs-lookup"><span data-stu-id="6b046-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="6b046-144">在 **地址簿** 下拉列表中，选择一个现有的客户通讯簿。</span><span class="sxs-lookup"><span data-stu-id="6b046-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="6b046-145">选择 **保存** 以保存并返回到新客户的客户详细信息屏幕。</span><span class="sxs-lookup"><span data-stu-id="6b046-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="6b046-146">不必为默认客户添加地址。</span><span class="sxs-lookup"><span data-stu-id="6b046-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="6b046-147">下图显示客户创建的示例。</span><span class="sxs-lookup"><span data-stu-id="6b046-147">The following image shows an example of customer creation.</span></span>

![默认客户创建](media/default-customer-creation.png)

<span data-ttu-id="6b046-149">下图显示了默认的客户配置。</span><span class="sxs-lookup"><span data-stu-id="6b046-149">The following image shows a default customer configuration.</span></span>

![客户配置示例](media/default-customer-configuration1.png)

<span data-ttu-id="6b046-151">客户详细信息屏幕上的大多数默认值都可以保留，但是应该更改两个值。</span><span class="sxs-lookup"><span data-stu-id="6b046-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="6b046-152">在客户详细信息屏幕上，展开 **销售订单默认值**。</span><span class="sxs-lookup"><span data-stu-id="6b046-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="6b046-153">在 **站点** 下拉列表中，选择或输入一个预配置的站点。</span><span class="sxs-lookup"><span data-stu-id="6b046-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="6b046-154">在 **仓库** 下拉列表中，选择或输入一个预配置的仓库。</span><span class="sxs-lookup"><span data-stu-id="6b046-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="6b046-155">下图显示客户配置示例。</span><span class="sxs-lookup"><span data-stu-id="6b046-155">The following image shows an example customer configuration.</span></span>

![客户配置示例](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="6b046-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="6b046-157">Additional resources</span></span>

[<span data-ttu-id="6b046-158">渠道概览</span><span class="sxs-lookup"><span data-stu-id="6b046-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6b046-159">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="6b046-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
