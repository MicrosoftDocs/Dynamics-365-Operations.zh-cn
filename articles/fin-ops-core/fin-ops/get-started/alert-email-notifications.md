---
title: 通过电子邮件发送的客户端预警通知
description: 此主题提供有关如何设置在预定义事件发生时发送电子邮件通知的规则的信息。
author: tjvass
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: fe422d645c8f2c0c564af30624090828e10ea4bf
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567244"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="72cfe-103">通过电子邮件发送的客户端预警通知</span><span class="sxs-lookup"><span data-stu-id="72cfe-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72cfe-104">您可以定义在预定义事件发生时监控筛选出的数据视图和自动发送电子邮件通知的自定义预警规则。</span><span class="sxs-lookup"><span data-stu-id="72cfe-104">You can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="72cfe-105">发送电子邮件通知的选项可用于所有支持的预警类型，也可为现有的预警规则打开。</span><span class="sxs-lookup"><span data-stu-id="72cfe-105">The option to send email notifications is available for all supported alert types and you can also turn them on for existing alert rules.</span></span>

<span data-ttu-id="72cfe-106">您可以使用内置控件创建监控筛选出的系统批处理作业视图的预警规则。</span><span class="sxs-lookup"><span data-stu-id="72cfe-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="72cfe-107">通过监视 **状态** 字段值，还可以配置在批处理作业失败时发送电子邮件的预警规则。</span><span class="sxs-lookup"><span data-stu-id="72cfe-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="72cfe-108">在创建这些预警规则后，您不必再检查报表了解对业务数据所作的更改。</span><span class="sxs-lookup"><span data-stu-id="72cfe-108">After you create these alert rules, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="72cfe-109">您可以让智能更改检测服务为您执行监控。</span><span class="sxs-lookup"><span data-stu-id="72cfe-109">Instead, you can let the intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="72cfe-110">客户端预警依靠通过与 Microsoft Office 的集成提供的电子邮件子系统。</span><span class="sxs-lookup"><span data-stu-id="72cfe-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="72cfe-111">我们建议您使用简单邮件传输协议 (SMTP) 提供程序，以使电子邮件分发不必依靠本地的邮件客户端。</span><span class="sxs-lookup"><span data-stu-id="72cfe-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="72cfe-112">若要通过电子邮件发送通知，客户必须配置集成的电子邮件服务。</span><span class="sxs-lookup"><span data-stu-id="72cfe-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="72cfe-113">电子邮件通知代表警报所有者发送到收件人。</span><span class="sxs-lookup"><span data-stu-id="72cfe-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="72cfe-114">有关如何配置电子邮件的详细信息，请参阅[配置和发送电子邮件](../organization-administration/configure-email.md)。</span><span class="sxs-lookup"><span data-stu-id="72cfe-114">For more information about how to configure email, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="72cfe-115">以下图像显示 **创建预警规则** 对话框，其现在包括 **发送电子邮件** 选项。</span><span class="sxs-lookup"><span data-stu-id="72cfe-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="72cfe-116">[![创建将“发送电子邮件”选项设置为“是”的预警规则对话框](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="72cfe-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="72cfe-117">在 **发送电子邮件** 选项设置为 **是** 时，预警通知将继续从操作中心提供。</span><span class="sxs-lookup"><span data-stu-id="72cfe-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="72cfe-118">预警通知电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="72cfe-118">Alert notification email templates</span></span>

<span data-ttu-id="72cfe-119">此服务通过使用提供预警通知基本详细信息的预定义电子邮件模板发送电子邮件通知。</span><span class="sxs-lookup"><span data-stu-id="72cfe-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span>

<span data-ttu-id="72cfe-120">以下图像显示通过电子邮件收到预警通知时预警通知的结构。</span><span class="sxs-lookup"><span data-stu-id="72cfe-120">The following image shows the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="72cfe-121">[![用户记录创建、字段更改和模板删除的基于模板的预警通知](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="72cfe-121">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]