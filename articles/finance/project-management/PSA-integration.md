---
title: Project Service Automation 概览
description: 本主题提供有关 Dynamics 365 Project Service Automation 到 Dynamics 365 Finance 集成解决方案的信息。
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250545"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="da66a-103">Project Service Automation 概览</span><span class="sxs-lookup"><span data-stu-id="da66a-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="da66a-104">Project Service Automation 到 Finance 集成解决方案使用数据集成功能，通过 Common Data Service 跨 Dynamics 365 Finance 和 Dynamics 365 Project Service Automation 的实例同步数据。</span><span class="sxs-lookup"><span data-stu-id="da66a-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="da66a-105">可通过数据集成功能提供的集成模板将项目、项目合同、项目合同行、项目合同行里程碑、项目任务、费用交易记录类别、工时估计值和费用估计值从 Project Service Automation 传输到 Finance。</span><span class="sxs-lookup"><span data-stu-id="da66a-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="da66a-106">如果在使用版本 7.3.0，则必须安装 KB 4074835。</span><span class="sxs-lookup"><span data-stu-id="da66a-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="da66a-107">然后就可以集成固定价格项目。</span><span class="sxs-lookup"><span data-stu-id="da66a-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="da66a-108">如果在使用版本 7.3.0，并从 Project Service Automation 导入免费交易记录，则必须安装 KB 4345320，以便将这些费用添加到该项目发票中。</span><span class="sxs-lookup"><span data-stu-id="da66a-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="da66a-109">如果您正在使用版本 8.0，则可以使用项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="da66a-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="da66a-110">如果您正在使用版本 8.0.1 或更高版本，则可以同步实际值。</span><span class="sxs-lookup"><span data-stu-id="da66a-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="da66a-111">必须先配置 Project Service Automation 集成参数，才能将 Project Service Automation 与 Finance 集成。</span><span class="sxs-lookup"><span data-stu-id="da66a-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="da66a-112">有关详细信息，请参阅 [Project Service Automation 集成参数](PSA-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="da66a-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="da66a-113">以下情况下，可通过集成解决方案直接同步：</span><span class="sxs-lookup"><span data-stu-id="da66a-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="da66a-114">在 Project Service Automation 中维护项目合同，并将其直接从 Project Service Automation 同步到 Finance。</span><span class="sxs-lookup"><span data-stu-id="da66a-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="da66a-115">在 Project Service Automation 中创建项目，并将其直接从 Project Service Automation 同步到 Finance。</span><span class="sxs-lookup"><span data-stu-id="da66a-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="da66a-116">在 Project Service Automation 中维护项目合同行，并将其直接从 Project Service Automation 同步到 Finance。</span><span class="sxs-lookup"><span data-stu-id="da66a-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="da66a-117">在 Project Service Automation 中维护项目合同行里程碑，并将其直接从 Project Service Automation 同步到 Finance。</span><span class="sxs-lookup"><span data-stu-id="da66a-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="da66a-118">在 Project Service Automation 中维护项目任务，并将其直接从 Project Service Automation 同步到 Finance。</span><span class="sxs-lookup"><span data-stu-id="da66a-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="da66a-119">在 Finance 中维护费用交易记录类别，并将其直接从 Finance 同步到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="da66a-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="da66a-120">在 Project Service Automation 中创建项目工时估计值，并将其直接从 Project Service Automation 同步到 Finance。</span><span class="sxs-lookup"><span data-stu-id="da66a-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="da66a-121">在 Project Service Automation 中创建项目费用估计值，并将其直接从 Project Service Automation 同步到 Finance。</span><span class="sxs-lookup"><span data-stu-id="da66a-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="da66a-122">在 Project Service Automation 中创建项目时间、费用和费用实际值，并在 Project Service Automation 集成日记帐中创建项目交易记录，以便在 Finance 中过帐。</span><span class="sxs-lookup"><span data-stu-id="da66a-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="da66a-123">数据同步</span><span class="sxs-lookup"><span data-stu-id="da66a-123">Data synchronization</span></span>

<span data-ttu-id="da66a-124">下图显示 Project Service Automation 与 Finance 之间的集成中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="da66a-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="da66a-125">并非所有模板当前都可用。</span><span class="sxs-lookup"><span data-stu-id="da66a-125">Not all templates are currently available.</span></span> <span data-ttu-id="da66a-126">模板将在准备好后发布。</span><span class="sxs-lookup"><span data-stu-id="da66a-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="da66a-127">[![Project Service Automation 与 Finance 集成](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="da66a-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="da66a-128">Finance 的系统要求</span><span class="sxs-lookup"><span data-stu-id="da66a-128">System requirements for Finance</span></span>

<span data-ttu-id="da66a-129">若要使用 Project Service Automation 到 Finance 集成解决方案，必须安装带平台更新 12 或更高版本的 Enterprise Edition 7.3。</span><span class="sxs-lookup"><span data-stu-id="da66a-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="da66a-130">Project Service Automation 的系统要求</span><span class="sxs-lookup"><span data-stu-id="da66a-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="da66a-131">若要使用 Project Service Automation 到 Finance 集成解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="da66a-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="da66a-132">Dynamics 365 Project Service Automation 版本 9.0.0.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="da66a-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="da66a-133">Dynamics 365 Sales 版本 1.14.0.0 (v14) 或更高版本的从目标客户到现金解决方案</span><span class="sxs-lookup"><span data-stu-id="da66a-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="da66a-134">适用于 Dynamics 365 Project Service Automation 版本 1.0.0.0 或更高版本的 Project Service Automation 到 Finance 解决方案</span><span class="sxs-lookup"><span data-stu-id="da66a-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="da66a-135">在 Project Service Automation 中安装 Project Service Automation 到 Finance 集成解决方案</span><span class="sxs-lookup"><span data-stu-id="da66a-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="da66a-136">从 [Microsoft 下载中心](https://www.microsoft.com/download/details.aspx?id=57016)下载 Project Service Automation 到 Finance 集成解决方案，然后按照该解决方案随附的说明操作。</span><span class="sxs-lookup"><span data-stu-id="da66a-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
