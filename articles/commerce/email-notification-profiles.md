---
title: 设置电子邮件通知配置文件
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建电子邮件通知配置文件。
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7504b2b36f6869f90de196bf32c09e7bdd51e7b5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792649"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="fc93d-103">设置电子邮件通知配置文件</span><span class="sxs-lookup"><span data-stu-id="fc93d-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fc93d-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建电子邮件通知配置文件。</span><span class="sxs-lookup"><span data-stu-id="fc93d-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fc93d-105">创建渠道时，可以设置电子邮件通知配置文件。</span><span class="sxs-lookup"><span data-stu-id="fc93d-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="fc93d-106">这样，就可以针对各种交易事件（例如，订单创建、订单运送状态和付款失败）给客户发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="fc93d-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="fc93d-107">有关其他电子邮件配置信息，请参阅[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="fc93d-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="fc93d-108">创建电子邮件通知配置文件</span><span class="sxs-lookup"><span data-stu-id="fc93d-108">Create an email notification profile</span></span>

<span data-ttu-id="fc93d-109">要创建电子邮件通知配置文件，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="fc93d-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="fc93d-110">在导航窗格中，转到 **模块 \> Retail and Commerce \> 总部设置 \> Commerce 电子邮件通知配置文件**。</span><span class="sxs-lookup"><span data-stu-id="fc93d-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="fc93d-111">在操作窗格中，单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="fc93d-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="fc93d-112">在 **电子邮件通知配置文件** 字段中，输入名称以标识配置文件。</span><span class="sxs-lookup"><span data-stu-id="fc93d-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="fc93d-113">在 **描述** 字段中，输入相关描述。</span><span class="sxs-lookup"><span data-stu-id="fc93d-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="fc93d-114">将 **有效** 开关设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="fc93d-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="fc93d-115">创建电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="fc93d-115">Create an email template</span></span>

<span data-ttu-id="fc93d-116">必须先在 Commerce Headquarters 中创建组织电子邮件模板，然后才能启用电子邮件通知类型。</span><span class="sxs-lookup"><span data-stu-id="fc93d-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="fc93d-117">该模板针对您要支持的每种语言定义电子邮件主题、发件人、默认语言和电子邮件正文。</span><span class="sxs-lookup"><span data-stu-id="fc93d-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="fc93d-118">若要创建电子邮件模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fc93d-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="fc93d-119">在导航窗格中，转到 **模块 \> Retail and Commerce \> 总部设置 \> 参数 \> 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="fc93d-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="fc93d-120">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="fc93d-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fc93d-121">在 **电子邮件 ID** 字段中，输入 ID 以帮助识别此模板。</span><span class="sxs-lookup"><span data-stu-id="fc93d-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="fc93d-122">在 **发件人名称** 字段中，输入发件人姓名。</span><span class="sxs-lookup"><span data-stu-id="fc93d-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="fc93d-123">在 **电子邮件描述** 中，输入有意义的描述。</span><span class="sxs-lookup"><span data-stu-id="fc93d-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="fc93d-124">在 **发件人电子邮件** 中，输入发件人电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="fc93d-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="fc93d-125">在 **常规** 部分，为电子邮件模板选择默认语言。</span><span class="sxs-lookup"><span data-stu-id="fc93d-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="fc93d-126">当指定语言的本地化模板不存在时，将使用默认语言。</span><span class="sxs-lookup"><span data-stu-id="fc93d-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="fc93d-127">展开 **电子邮件内容** 部分并选择 **新建** 以创建模板内容。</span><span class="sxs-lookup"><span data-stu-id="fc93d-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="fc93d-128">对于每个内容项，选择语言并提供电子邮件主题行。</span><span class="sxs-lookup"><span data-stu-id="fc93d-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="fc93d-129">如果电子邮件有正文，请确保选中 **有正文** 框。</span><span class="sxs-lookup"><span data-stu-id="fc93d-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="fc93d-130">在操作窗格上，选择 **电子邮件** 以提供电子邮件正文模板。</span><span class="sxs-lookup"><span data-stu-id="fc93d-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="fc93d-131">下图显示了一些示例电子邮件模板设置。</span><span class="sxs-lookup"><span data-stu-id="fc93d-131">The following image shows some example email template settings.</span></span>

![电子邮件模板设置](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="fc93d-133">创建电子邮件事件</span><span class="sxs-lookup"><span data-stu-id="fc93d-133">Create an email event</span></span>

<span data-ttu-id="fc93d-134">若要创建电子邮件事件，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fc93d-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="fc93d-135">在导航窗格中，转到 **模块 \> Retail and Commerce \> 总部设置 \> Commerce 电子邮件通知配置文件**。</span><span class="sxs-lookup"><span data-stu-id="fc93d-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="fc93d-136">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="fc93d-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="fc93d-137">从 **电子邮件 ID** 下拉列表中选择电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="fc93d-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="fc93d-138">从下拉列表中选择合适的 **电子邮件通知类型**。</span><span class="sxs-lookup"><span data-stu-id="fc93d-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="fc93d-139">选中 **有效** 复选框。</span><span class="sxs-lookup"><span data-stu-id="fc93d-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="fc93d-140">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="fc93d-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fc93d-141">下图显示了一些示例事件通知设置。</span><span class="sxs-lookup"><span data-stu-id="fc93d-141">The following image shows some example event notification settings.</span></span>

![事件通知设置](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="fc93d-143">后续步骤</span><span class="sxs-lookup"><span data-stu-id="fc93d-143">Next steps</span></span>

<span data-ttu-id="fc93d-144">必须先配置出站邮件服务和设置批处理作业，然后才能发送邮件。</span><span class="sxs-lookup"><span data-stu-id="fc93d-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="fc93d-145">有关详细信息，请参阅[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)。</span><span class="sxs-lookup"><span data-stu-id="fc93d-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="fc93d-146">其他资源</span><span class="sxs-lookup"><span data-stu-id="fc93d-146">Additional resources</span></span>

[<span data-ttu-id="fc93d-147">配置和发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="fc93d-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="fc93d-148">渠道概览</span><span class="sxs-lookup"><span data-stu-id="fc93d-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="fc93d-149">渠道设置先决条件</span><span class="sxs-lookup"><span data-stu-id="fc93d-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="fc93d-150">组织和组织层次结构概览</span><span class="sxs-lookup"><span data-stu-id="fc93d-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
