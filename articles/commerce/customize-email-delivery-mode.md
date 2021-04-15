---
title: 按交货方式自定义事务电子邮件
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中为特定的通知类型和交货方式设置自定义电子邮件模板。
author: stuharg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 411e694b33e0443a336f6a8cdad78714630e4bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799365"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a><span data-ttu-id="0c5a4-103">按交货模式自定义事务电子邮件</span><span class="sxs-lookup"><span data-stu-id="0c5a4-103">Customize transactional emails by mode of delivery</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c5a4-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中为特定的通知类型和交货方式设置自定义电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-104">This topic describes how to set up custom email templates for specific notification types and modes of delivery in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0c5a4-105">现在可以自定义事务电子邮件，以将通知类型（例如，**订单已创建**、**订单已包装** 或 **订单已开票**）和交货方式（例如，隔夜、店内提货或路边提货）结合在一起。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-105">Transactional emails can now be customized for a combination of a notification type (for example, **Order created**, **Order packed**, or **Order invoiced**) and a mode of delivery (for example, overnight, in-store pickup, or curbside pickup).</span></span> <span data-ttu-id="0c5a4-106">通过自定义事务电子邮件，零售商可以为客户订单提供专为订单交货方式定制的履行体验。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-106">Custom transactional emails let retailers provide their customers order with fulfillment experiences that are tailored to the order's mode of delivery.</span></span> <span data-ttu-id="0c5a4-107">例如，可以自定义“订单已包装”事件，以便为选择路边提货的客户提供路边提货说明。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-107">For example, the "order packed" event can be customized so that it provides curbside pickup instructions for customers who choose curbside pickup.</span></span> <span data-ttu-id="0c5a4-108">或者，可以为选择装运订单的客户提供装运承运人和交货信息。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-108">Alternatively, it can provide shipping carrier and delivery information for customers who choose to have their order shipped.</span></span>

> [!NOTE]
> <span data-ttu-id="0c5a4-109">若要使用自定义事务电子邮件的功能，首先必须通过在 Commerce 总部中转到 **工作区 \> 功能管理** 来打开 **按交货方式自定义事务电子邮件模板** 功能。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-109">To use the functionality for customized transactional emails, you first must turn on the **Customize transactional email templates by mode of delivery** feature by going to **Workspaces \> Feature management** in Commerce headquarters.</span></span>

<span data-ttu-id="0c5a4-110">可以针对以下通知类型按交货方式自定义电子邮件：</span><span class="sxs-lookup"><span data-stu-id="0c5a4-110">Emails can be customized by mode of delivery for the following notification types:</span></span>

- <span data-ttu-id="0c5a4-111">**订单取消** – 此电子邮件通知类型是新的。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-111">**Order cancellation** – This email notification type is new.</span></span>
- <span data-ttu-id="0c5a4-112">**订单已创建**</span><span class="sxs-lookup"><span data-stu-id="0c5a4-112">**Order created**</span></span>
- <span data-ttu-id="0c5a4-113">**订单已确认**</span><span class="sxs-lookup"><span data-stu-id="0c5a4-113">**Order confirmed**</span></span>
- <span data-ttu-id="0c5a4-114">**订单已开票** – 此电子邮件通知类型是新的。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-114">**Order invoiced** – This email notification type is new.</span></span> <span data-ttu-id="0c5a4-115">它可以代替 **订单已装运** 通知类型，该类型将针对具有已装运交货方式（而不是提货、自提或电子交货方式）的任何发票事件发送通知。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-115">It can be used instead of the **Order shipped** notification type that will send a notification for any invoice event that has a shipped mode of delivery (not a pickup, carry out, or electronic mode of delivery).</span></span>
- <span data-ttu-id="0c5a4-116">**订单已领料**</span><span class="sxs-lookup"><span data-stu-id="0c5a4-116">**Order picked**</span></span>
- <span data-ttu-id="0c5a4-117">**订单已包装**</span><span class="sxs-lookup"><span data-stu-id="0c5a4-117">**Order packed**</span></span>
- <span data-ttu-id="0c5a4-118">**订单可提货** – 仅在打开 **支持多个提货交货方式** 功能时才按提货方式自定义此通知类型。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-118">**Order ready for pickup** – This notification type can be customized by mode of delivery only if the **Support for multiple pickup delivery modes** feature is turned on.</span></span> <span data-ttu-id="0c5a4-119">在这种情况下，此通知类型在功能上等同于 **订单已包装** 通知类型。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-119">In that case, this notification type is functionally equivalent to the **Order packed** notification type.</span></span>
- <span data-ttu-id="0c5a4-120">**付款失败**</span><span class="sxs-lookup"><span data-stu-id="0c5a4-120">**Payment failed**</span></span>
- <span data-ttu-id="0c5a4-121">**已创建更换单**</span><span class="sxs-lookup"><span data-stu-id="0c5a4-121">**Replacement order created**</span></span>

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a><span data-ttu-id="0c5a4-122">为特定的交货方式配置电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="0c5a4-122">Configure email templates for specific modes of delivery</span></span>

<span data-ttu-id="0c5a4-123">对于此过程，假设您已创建新的自定义电子邮件模板并将其添加到 **组织电子邮件模板** 页面。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-123">For this procedure, the assumption is that you've already created your new, custom email templates and added them to the **Organization email templates** page.</span></span> <span data-ttu-id="0c5a4-124">有关如何创建和上传电子邮件模板的信息，请参阅[创建交易事件的电子邮件模板](email-templates-transactions.md)。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-124">For information about how to create and upload email templates, see [Create email templates for transactional events](email-templates-transactions.md).</span></span>

<span data-ttu-id="0c5a4-125">若要在 Commerce 总部为特定交货方式配置电子邮件模板，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-125">To configure email templates for specific modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0c5a4-126">转到 **Commerce 电子邮件通知配置文件**。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-126">Go to **Commerce email notification profile**.</span></span>
1. <span data-ttu-id="0c5a4-127">在 **零售事件通知设置** 下，选择一个现有的通知类型。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-127">Under **Retail event notification settings**, select an existing notification type.</span></span>
1. <span data-ttu-id="0c5a4-128">在通知类型保持选中时，选择 **配置交货方式**。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-128">While the notification type is still selected, select **Configure modes of delivery**.</span></span>
1. <span data-ttu-id="0c5a4-129">在 **交货方式** 对话框中，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-129">In the **Modes of delivery** dialog box, select **New**.</span></span>
1. <span data-ttu-id="0c5a4-130">在新行中，在 **交货方式** 字段中，选择交货方式。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-130">In the new row, in the **Mode of delivery** field, select a mode of delivery.</span></span>
1. <span data-ttu-id="0c5a4-131">在 **电子邮件 ID** 字段中，选择要映射到交货方式的电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-131">In the **Email ID** field, select the email template to map to the mode of delivery.</span></span>
1. <span data-ttu-id="0c5a4-132">选中 **有效** 复选框。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-132">Select the **Active** check box.</span></span>
1. <span data-ttu-id="0c5a4-133">重复步骤 4 到 7 以添加更多交货方式。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-133">Repeat steps 4 through 7 to add more modes of delivery.</span></span>
1. <span data-ttu-id="0c5a4-134">当您完成时，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-134">When you've finished, select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="0c5a4-135">如果销售订单的各行之间存在多种交货方式，将使用默认模板。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-135">When more than one mode of delivery is present across lines in a sales order, the default template will be used.</span></span> <span data-ttu-id="0c5a4-136">默认模板是在 **Commerce 电子邮件通知配置文件** 页面上映射到通知类型的模板。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-136">The default template is the template that is mapped to the notification type on the **Commerce email notification profile** page.</span></span>
> - <span data-ttu-id="0c5a4-137">如果销售订单的交货方式尚未为自定义电子邮件模板配置，将使用默认电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="0c5a4-137">If a sales order has a mode of delivery that hasn't been configured for a custom email template, the default email template will be used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c5a4-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="0c5a4-138">Additional resources</span></span>

[<span data-ttu-id="0c5a4-139">创建呼叫中心订单</span><span class="sxs-lookup"><span data-stu-id="0c5a4-139">Create call center orders</span></span>](tasks/create-call-center-orders.md)

[<span data-ttu-id="0c5a4-140">在 POS 上更改交货方式</span><span class="sxs-lookup"><span data-stu-id="0c5a4-140">Change mode of delivery in POS</span></span>](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]