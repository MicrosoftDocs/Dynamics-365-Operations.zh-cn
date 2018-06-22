---
title: Project Service Automation
description: "此解决方案使用数据集成功能，通过 Common Data Service (CDS) 跨 Microsoft Dynamics 365 for Finance and Operations 和 Microsoft Dynamics 365 for Project Service Automation 的实例同步数据。"
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: zh-cn
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="9f329-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9f329-103">Project Service Automation</span></span>

<span data-ttu-id="9f329-104">Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能，通过 Common Data Service (CDS) 跨 Microsoft Dynamics 365 for Finance and Operations 和 Microsoft Dynamics 365 for Project Service Automation 的实例同步数据。</span><span class="sxs-lookup"><span data-stu-id="9f329-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="9f329-105">可通过数据集成功能提供的集成模板将项目、项目合同、项目合同行、项目合同行里程碑、项目任务、费用交易记录类别、工时估计值和费用估计值从 Project Service Automation 传输到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9f329-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="9f329-106">如果您正在使用 Dynamics 365 for Finance and Operations Enterprise Edition 7.300，您必须安装 KB 4074835。</span><span class="sxs-lookup"><span data-stu-id="9f329-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="9f329-107">这样就可以集成固定价格项目。</span><span class="sxs-lookup"><span data-stu-id="9f329-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="9f329-108">如果您正在使用 Dynamics 365 for Finance and Operations 版本 8.0，则可以使用项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="9f329-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="9f329-109">如果您正在使用 Dynamics 365 for Finance and Operations 版本 8.0.1，则可以同步实际值。</span><span class="sxs-lookup"><span data-stu-id="9f329-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="9f329-110">如果您正在使用 Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。</span><span class="sxs-lookup"><span data-stu-id="9f329-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="9f329-111">如果必须重置会计分配，建议也安装 KB 4131710。</span><span class="sxs-lookup"><span data-stu-id="9f329-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="9f329-112">必须先配置 Project Service Automation 集成参数，才能将 Project Service Automation 与 Finance and Operations 集成。</span><span class="sxs-lookup"><span data-stu-id="9f329-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="9f329-113">有关详细信息，请参阅“Project Service Automation 集成参数”。</span><span class="sxs-lookup"><span data-stu-id="9f329-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="9f329-114">以下情况下，可通过集成解决方案直接同步：</span><span class="sxs-lookup"><span data-stu-id="9f329-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="9f329-115">在 Project Service Automation 中维护项目合同，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9f329-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9f329-116">在 Project Service Automation 中创建项目，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9f329-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9f329-117">在 Project Service Automation 中维护项目合同行，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9f329-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9f329-118">在 Project Service Automation 中维护项目合同行里程碑，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9f329-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9f329-119">在 Project Service Automation 中维护项目任务，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9f329-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9f329-120">在 Finance and Operations 中维护费用交易记录类别，并将其直接从 Finance and Operations 同步到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="9f329-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="9f329-121">在 Project Service Automation 中创建项目工时估计值，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9f329-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="9f329-122">在 Project Service Automation 中创建项目支出估计值，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9f329-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="9f329-123">数据同步</span><span class="sxs-lookup"><span data-stu-id="9f329-123">Data synchronization</span></span>
<span data-ttu-id="9f329-124">下图显示 Project Service Automation 与 Finance and Operations 之间的集成中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="9f329-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="9f329-125">并非所有模板当前都可用。</span><span class="sxs-lookup"><span data-stu-id="9f329-125">Not all templates are currently available.</span></span> <span data-ttu-id="9f329-126">模板将在准备好后发布。</span><span class="sxs-lookup"><span data-stu-id="9f329-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="9f329-127">[![Project Service Automation 与 Finance and Operations 集成](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="9f329-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="9f329-128">Finance and Operations 的系统要求</span><span class="sxs-lookup"><span data-stu-id="9f329-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="9f329-129">若要使用 Project Service Automation 到 Finance and Operations 集成解决方案，必须安装带平台更新 12 或更高版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3。</span><span class="sxs-lookup"><span data-stu-id="9f329-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="9f329-130">Project Service Automation 的系统要求</span><span class="sxs-lookup"><span data-stu-id="9f329-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="9f329-131">若要使用 Project Service Automation 到 Finance and Operations 集成解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="9f329-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="9f329-132">Microsoft Dynamics 365 for Project Service Automation 版本 9.0.0.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="9f329-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="9f329-133">Dynamics 365 for Sales 版本 1.14.0.0 (v14) 或更高版本的从目标客户到现金解决方案。</span><span class="sxs-lookup"><span data-stu-id="9f329-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="9f329-134">适用于 Dynamics 365 for Project Service Automation 的 Project Service Automation 到 Operations 解决方案版本 1.0.0.0 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="9f329-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="9f329-135">在 Project Service Automation 中安装 Project Service Automation 到 Finance and Operations 集成解决方案</span><span class="sxs-lookup"><span data-stu-id="9f329-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



