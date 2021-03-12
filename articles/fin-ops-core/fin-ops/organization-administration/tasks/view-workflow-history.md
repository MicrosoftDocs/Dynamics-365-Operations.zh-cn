---
title: 查看工作流历史记录
description: 本主题介绍用于查看提交给工作流系统进行处理和审核的单据的状态的步骤。
author: jasongre
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowStatus
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 325478ed89b9c650899001dd08d1c98550fce520
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798972"
---
# <a name="view-workflow-history"></a><span data-ttu-id="e8bdb-103">查看工作流历史记录</span><span class="sxs-lookup"><span data-stu-id="e8bdb-103">View workflow history</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8bdb-104">本主题介绍用于查看提交给工作流系统进行处理和审核的单据的状态的步骤。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-104">This topic describes the steps to view the status of a document that was submitted to the workflow system for processing and approval.</span></span> <span data-ttu-id="e8bdb-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="e8bdb-106">转到 **导航窗格 > 模块 > 常用 > 查询 > 工作流 > 工作流历史记录**。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-106">Go to **Navigation pane > Modules > Common > Inquiries > Workflow > Workflow history**.</span></span>
    - <span data-ttu-id="e8bdb-107">使用此窗体可以查看提交给工作流系统进行处理和审核的单据的状态。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-107">Use this form to view the status of a document that was submitted to the workflow system for processing and approval.</span></span>  
    - <span data-ttu-id="e8bdb-108">**实例 ID** 是正在处理或已经处理单据的工作流实例的标识代码。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-108">The **Instance ID** is the identification code of the workflow instance that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="e8bdb-109">**状态** 是单据的工作流状态。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-109">The **Status** is the workflow status of the document.</span></span>  
    - <span data-ttu-id="e8bdb-110">**工作流 ID** 是正在处理或已经处理单据的工作流的标识代码。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-110">The **Workflow ID** is the identification code of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="e8bdb-111">**单据** 是单据的标识代码。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-111">The **Document** is the identification code of the document.</span></span>  
    - <span data-ttu-id="e8bdb-112">**单据类型** 是提交以处理的单据的类型。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-112">The **Document type** is the type of document that was submitted for processing.</span></span>  
    - <span data-ttu-id="e8bdb-113">**工作流** 是正在处理或已经处理单据的工作流的名称。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-113">The **Workflow** is the name of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="e8bdb-114">**版本** 是正在处理或已经处理单据的工作流的版本号。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-114">The **Version** is the version number of the workflow that is processing, or has processed the document.</span></span>  
    - <span data-ttu-id="e8bdb-115">**创建日期和时间** 是是提交单据的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-115">The **Created date and time** is the date and time that the document was submitted.</span></span>  
    - <span data-ttu-id="e8bdb-116">**占用时间** 是自单据提交后经过的时间。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-116">The **Elapsed time** is the time that has passed since the document was submitted.</span></span>  
    - <span data-ttu-id="e8bdb-117">可通过 **恢复** 按钮恢复所选单据的工作流。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-117">The **Resume** button allows you to resume the workflow process for the selected document.</span></span>  
    - <span data-ttu-id="e8bdb-118">可通过 **撤消** 按钮撤消所选单据，以便不处理该单据。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-118">The **Recall** button allows you to recall the selected document so that it is not processed.</span></span>   
2. <span data-ttu-id="e8bdb-119">在列表中，选择所需行中的链接。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-119">In the list, select the link in the desired row.</span></span>
    - <span data-ttu-id="e8bdb-120">确保已展开 **工作项** 部分。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-120">Make sure the **Work items** section is expanded.</span></span> <span data-ttu-id="e8bdb-121">在此部分中，可以查看与所选单据关联的工作项。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-121">In this section you can view the work items that are associated with the selected document.</span></span> <span data-ttu-id="e8bdb-122">例如，可能必须完成某项任务，或者可能必须审核单据。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-122">For example, a task may have to be completed, or the document may have to be approved.</span></span>  
    - <span data-ttu-id="e8bdb-123">**重新分配** 按钮将打开一个对话框，从中可向其他用户重新分配工作项。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-123">The **Reassign** button will open a dialog box where you can reassign a work item to another user.</span></span>  
    - <span data-ttu-id="e8bdb-124">确保已展开 **跟踪详细信息** 部分。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-124">Make sure the **Tracking details** section is expanded.</span></span> <span data-ttu-id="e8bdb-125">在此部分中，可以查看所选单据的工作流历史记录。</span><span class="sxs-lookup"><span data-stu-id="e8bdb-125">In this section you can view the workflow history of the selected document.</span></span>  

