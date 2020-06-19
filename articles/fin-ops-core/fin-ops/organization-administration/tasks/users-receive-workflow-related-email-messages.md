---
title: 使得用户能够接收工作流相关的电子邮件消息
description: 在工作流相关事件发生时，您可以配置系统将电子邮件消息发送给用户。
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40ad380c7bfb2b3fc518b0278286ae03532668ed
ms.sourcegitcommit: 4db8c30c2f26af1896938dd3ece3756577374ecb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2020
ms.locfileid: "3416545"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="a0bf1-103">使得用户能够接收工作流相关的电子邮件消息</span><span class="sxs-lookup"><span data-stu-id="a0bf1-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0bf1-104">在工作流相关事件发生时，您可以配置系统将电子邮件消息发送给用户。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="a0bf1-105">例如，当分配文档供审核时，可以将电子邮件消息发送给用户。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="a0bf1-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a0bf1-107">转到**导航窗格 > 模块 > 系统管理 > 用户 > 用户**。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="a0bf1-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a0bf1-109">在**操作窗格**上，单击**用户选项**。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="a0bf1-110">单击**工作流**选项卡。确保展开**通知**部分。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="a0bf1-111">在**通知**部分中，可以指定您希望程序如何通知用户有关工作流相关事件。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="a0bf1-112">在**行项工作流通知类型**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="a0bf1-113">分组 – 行项的通知分组到单个电子邮件消息中。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="a0bf1-114">单独 – 针对每个行项发送电子邮件消息。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="a0bf1-115">如果您希望用户在客户端中接收通知，则选中**以电子邮件形式发送通知**复选框。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="a0bf1-116">单击**保存**。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-116">Click **Save**.</span></span>
7. <span data-ttu-id="a0bf1-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="a0bf1-118">工作流电子邮件模板源自系统电子邮件模板或组织电子邮件模板，具体取决于工作流是系统级（不是公司特定）还是组织级（公司特定）工作流。</span><span class="sxs-lookup"><span data-stu-id="a0bf1-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>
