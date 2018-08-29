--- 
title: "配置系统以向用户发送与工作流有关的电子邮件"
description: "在工作流相关事件发生时，您可以配置系统将电子邮件消息发送给用户。"
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a><span data-ttu-id="f438d-103">配置系统以向用户发送与工作流有关的电子邮件</span><span class="sxs-lookup"><span data-stu-id="f438d-103">Configure the system to send workflow-related email to users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f438d-104">在工作流相关事件发生时，您可以配置系统将电子邮件消息发送给用户。</span><span class="sxs-lookup"><span data-stu-id="f438d-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="f438d-105">例如，当分配文档供审核时，可以将电子邮件消息发送给用户。</span><span class="sxs-lookup"><span data-stu-id="f438d-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="f438d-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="f438d-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="f438d-107">转到“系统管理”>“用户”>“用户”。</span><span class="sxs-lookup"><span data-stu-id="f438d-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="f438d-108">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="f438d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f438d-109">单击“用户选项”。</span><span class="sxs-lookup"><span data-stu-id="f438d-109">Click User options.</span></span>
4. <span data-ttu-id="f438d-110">单击“工作流”选项卡。</span><span class="sxs-lookup"><span data-stu-id="f438d-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="f438d-111">确保已展开“通知”部分。</span><span class="sxs-lookup"><span data-stu-id="f438d-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="f438d-112">在“通知”部分中，可以指定您希望程序如何通知用户有关工作流相关事件。</span><span class="sxs-lookup"><span data-stu-id="f438d-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="f438d-113">在“行项工作流通知类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f438d-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="f438d-114">分组 – 行项的通知分组到单个电子邮件消息中。</span><span class="sxs-lookup"><span data-stu-id="f438d-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="f438d-115">单独 – 针对每个行项发送电子邮件消息。</span><span class="sxs-lookup"><span data-stu-id="f438d-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="f438d-116">如果您希望用户在客户端中接收通知，则选中“以电子邮件形式发送通知”复选框。</span><span class="sxs-lookup"><span data-stu-id="f438d-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="f438d-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f438d-117">Click Save.</span></span>
7. <span data-ttu-id="f438d-118">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f438d-118">Close the page.</span></span>


