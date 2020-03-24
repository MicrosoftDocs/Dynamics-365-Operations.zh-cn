---
title: 设置电子邮件通知配置文件
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建电子邮件通知配置文件。
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
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113797"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="c0f9e-103">设置电子邮件通知配置文件</span><span class="sxs-lookup"><span data-stu-id="c0f9e-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c0f9e-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建电子邮件通知配置文件。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c0f9e-105">概览</span><span class="sxs-lookup"><span data-stu-id="c0f9e-105">Overview</span></span>

<span data-ttu-id="c0f9e-106">在创建渠道之前，您需要设置一个配置文件，以确保可以针对各种事件发送电子邮件通知，例如订单创建、订单运送状态和付款失败。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="c0f9e-107">有关其他电子邮件配置信息，请参阅[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="c0f9e-108">创建电子邮件通知配置文件</span><span class="sxs-lookup"><span data-stu-id="c0f9e-108">Create an email notification profile</span></span>

<span data-ttu-id="c0f9e-109">要创建电子邮件通知配置文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="c0f9e-110">在导航窗格中，转到**模块 \> Retail and Commerce \> 总部设置 \> Commerce 电子邮件通知配置文件**。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="c0f9e-111">在操作窗格中，单击**新建**。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="c0f9e-112">在**电子邮件通知配置文件**字段中，输入名称以标识配置文件。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="c0f9e-113">在**描述**字段中，输入相关描述。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="c0f9e-114">将**有效**开关设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="c0f9e-115">创建电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="c0f9e-115">Create an email template</span></span>

<span data-ttu-id="c0f9e-116">在创建电子邮件通知之前，您必须创建一个组织电子邮件模板，其中包含发件人电子邮件信息和电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="c0f9e-117">若要创建电子邮件模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="c0f9e-118">在导航窗格中，转到**模块 \> Retail and Commerce \> 总部设置 \> 参数 \> 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="c0f9e-119">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c0f9e-120">在**电子邮件 ID** 字段中，输入 ID 以帮助识别此模板。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="c0f9e-121">在**发件人名称**字段中，输入发件人姓名。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="c0f9e-122">在**电子邮件描述**中，输入有意义的描述。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="c0f9e-123">在**发件人电子邮件**中，输入发件人电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="c0f9e-124">在**常规**部分中，填写所需的所有可选信息（例如电子邮件优先级）。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="c0f9e-125">展开**电子邮件内容**部分并选择**新建**以创建模板内容。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="c0f9e-126">对于每个内容项，选择语言并提供电子邮件主题行。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="c0f9e-127">如果电子邮件有正文，请确保选中**有正文**框。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="c0f9e-128">在操作窗格上，选择**电子邮件**以提供电子邮件正文模板。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="c0f9e-129">下图显示了一些示例电子邮件模板设置。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-129">The following image shows some example email template settings.</span></span>

![电子邮件模板设置](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="c0f9e-131">创建电子邮件事件</span><span class="sxs-lookup"><span data-stu-id="c0f9e-131">Create an email event</span></span>

<span data-ttu-id="c0f9e-132">若要创建电子邮件事件，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="c0f9e-133">在导航窗格中，转到**模块 \> Retail and Commerce \> 总部设置 \> Commerce 电子邮件通知配置文件**。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="c0f9e-134">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="c0f9e-135">从**电子邮件 ID** 下拉列表中选择电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="c0f9e-136">从下拉列表中选择合适的**电子邮件通知类型**。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="c0f9e-137">选中**有效**复选框。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="c0f9e-138">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c0f9e-139">下图显示了一些示例事件通知设置。</span><span class="sxs-lookup"><span data-stu-id="c0f9e-139">The following image shows some example event notification settings.</span></span>

![事件通知设置](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="c0f9e-141">其他资源</span><span class="sxs-lookup"><span data-stu-id="c0f9e-141">Additional resources</span></span>

[<span data-ttu-id="c0f9e-142">配置和发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="c0f9e-142">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c0f9e-143">渠道概览</span><span class="sxs-lookup"><span data-stu-id="c0f9e-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c0f9e-144">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="c0f9e-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="c0f9e-145">组织和组织层次结构概览</span><span class="sxs-lookup"><span data-stu-id="c0f9e-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
