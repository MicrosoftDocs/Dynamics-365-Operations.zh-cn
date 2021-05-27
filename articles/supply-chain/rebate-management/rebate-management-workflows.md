---
title: 返点管理交易工作流
description: 本主题说明如何设置返点管理交易工作流以审核和激活交易。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020371"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="3391b-103">返点管理交易工作流</span><span class="sxs-lookup"><span data-stu-id="3391b-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3391b-104">若要审核返点交易，返点管理使用与其他 Finance and Operations 应用相同的工作流平台。</span><span class="sxs-lookup"><span data-stu-id="3391b-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="3391b-105">每个工作流关联了两个作业流程：</span><span class="sxs-lookup"><span data-stu-id="3391b-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="3391b-106">工作流的一个元素用于激活交易，以便用户或工作流程可以审核交易记录。</span><span class="sxs-lookup"><span data-stu-id="3391b-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="3391b-107">工作流的另一个元素用于审核交易。</span><span class="sxs-lookup"><span data-stu-id="3391b-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="3391b-108">返点交易必须在 **返点管理** 模块中处于活动状态，然后才可供使用。</span><span class="sxs-lookup"><span data-stu-id="3391b-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="3391b-109">若要激活交易，必须首先创建和配置 *返点管理交易工作流*。</span><span class="sxs-lookup"><span data-stu-id="3391b-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="3391b-110">为返点管理激活工作流后，用户无法手动审核交易。</span><span class="sxs-lookup"><span data-stu-id="3391b-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="3391b-111">必须始终使用工作流。</span><span class="sxs-lookup"><span data-stu-id="3391b-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="3391b-112">创建和管理返点管理交易工作流</span><span class="sxs-lookup"><span data-stu-id="3391b-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="3391b-113">若要使用返点管理交易工作流，请转到 **返点管理 \> 设置 \> 返点管理工作流**。</span><span class="sxs-lookup"><span data-stu-id="3391b-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="3391b-114">在此处，您可以根据需要查看、创建和更新工作流。</span><span class="sxs-lookup"><span data-stu-id="3391b-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="3391b-115">一次只能激活此类型的一个工作流。</span><span class="sxs-lookup"><span data-stu-id="3391b-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="3391b-116">有关工作流的详细信息、如何使用 **返点管理工作流** 页面以及如何创建工作流，请参阅[工作流系统概述](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)及其相关主题。</span><span class="sxs-lookup"><span data-stu-id="3391b-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="3391b-117">使用工作流激活交易</span><span class="sxs-lookup"><span data-stu-id="3391b-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="3391b-118">若要通过工作流激活交易，请打开交易（例如，在 **所有返点管理交易** 页面上）。</span><span class="sxs-lookup"><span data-stu-id="3391b-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="3391b-119">然后，在操作窗格上，选择 **工作流 \> 提交**。</span><span class="sxs-lookup"><span data-stu-id="3391b-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="3391b-120">通过工作流处理和审核新交易后，它将处于活动状态并且可供使用。</span><span class="sxs-lookup"><span data-stu-id="3391b-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="3391b-121">激活交易后，您将无法更改其设置。</span><span class="sxs-lookup"><span data-stu-id="3391b-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="3391b-122">如果您必须更改活动的交易，请取消激活它，然后创建新交易。</span><span class="sxs-lookup"><span data-stu-id="3391b-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="3391b-123">如果新交易类似于旧交易，则可以通过复制旧交易来创建它。</span><span class="sxs-lookup"><span data-stu-id="3391b-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
